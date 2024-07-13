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