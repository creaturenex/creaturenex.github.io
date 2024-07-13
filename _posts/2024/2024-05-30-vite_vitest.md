---
layout: post
title:  "Setting up a React Frontend with Vite, TS, Vitest, Testing-Library "
date:   2024-05-30 08:00:00 -0500
categories: react, tests, vite
---

## Install Vitest & JSDOM

```bash
npm install --save-dev vitest jsdom
```

## Update Files

After installing vitest, **add a script** to the package.json file to run the tests.

```JSON
{
  "scripts": {
    "test": "vitest"
  }
}
```

After installing jsdom, I have to include jsdom in the Vite configuration file `vite.config.js`

```Typescript
// This was added for typing
/// <reference types="vitest" />

import path from 'path' 
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
  resolve: {
    alias: {
      "@": path.resolve(__dirname, "./src")
    }
  },
  // this section was added for testing
  test: {
    globals: true,
    environment: 'jsdom',
    setupFiles: ['./vitest.setup.ts'], 
    exclude: ["node_modules"]
  },
})
```

## Install Testing-Library and dependancies
```bash
npm install --save-dev @testing-library/jest-dom @testing-library/react @testing-library/user-event
```
    Note **user-event** might not be needed

## Add vitest setup file
There are many opinions but I am adding it to the root folder as all the other configuration files are there.

`mkdir vitest.setup.ts`

Add the following
```typescript
import '@testing-library/jest-dom/vitest'
import { cleanup } from '@testing-library/react'
import { afterEach, expect } from 'vitest'
import * as matchers from '@testing-library/jest-dom/matchers'

// add additional matchers from jest-dom to vitest
expect.extend(matchers);

//to remove any running processes after each test
afterEach(() => {
  cleanup()
});
```
