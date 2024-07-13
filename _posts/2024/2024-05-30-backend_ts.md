---
layout: post
title: "Setting up a Typescript backend using Express"
date: 2024-05-30 09:00:00 -0500
categories: Typescript
tags: express
---

## Install Express

Typically I use express-generator so I can reduce the boilerplate setup I need to do.

`$ npm install -g express-generator`

I initialize a new project named backend. I add the flag `--no-view` because I typically use **React** for the frontend.

There are additional options that can be used see [express-generator options](https://www.npmjs.com/package/express-generator#command-line-options)

`$ express --no-view backend`

Because I am using Typescript, I need to install @types/... for the various packages. For example the generator uses morgan for logging, I need to install

`npm i -D @types/morgan`

I also install dotenv, to read process files

`npm i dotenv`

    **NOTE:** Node +20.6 supports .env files when passed as an ARG
    when initializing a file ex. `node --env-file .env`

## Folder Structure

I create a src directory and place the `routes/` directory and the `app.js` which is renamed to `index.ts` into `src/`.

## Add Typescript

In the terminal run the following commands

```bash
npm i -D typescript @types/express @types/node
```

This added the Typescript compiler, types for express and node

Next we want to initiate the compiler, which will generate the `tsconfig.json` file.

In the terminal run the following commands

```bash
npx tsc --init
```

Next we want to edit `tsconfig.json` and uncomment `"outDir" : "./dist"` or add it inside of the compilerOption
This will place on the compiled js into this directory for distribution online

```bash
{
  "compilerOptions": {
    ...
    "outDir": "./dist"
    ...
  }
}
```

## Express server

Lets edit the index.ts file

```Typescript
import express, { Application, Request, Response, NextFunction } from 'express';
import path from 'path';
import logger from 'morgan';
import router from './routes/index';
import dotenv from 'dotenv';
dotenv.config();

// edit this to use .env Variables
const PORT = 3000

const app: Application = express();

app.use(logger('dev'));
app.use(express.json());
app.use(express.urlencoded({ extended: false }));

// this will eventually serve next.js build files
app.use(express.static(path.join(__dirname, '../../frontend/dist')));

app.use('/', router);

// Global error handler
app.use((err: Error, req: Request, res: Response, next: NextFunction) => {
  console.error(err.stack);
  res.status(500).send('Something went wrong!');
});

app.listen(PORT, () => {
  console.log(`Server listening on http://localhost:${PORT}`);
});

export default app;
```

## Running Typescript

If you were to excute `npm run dev` you would get an `SyntaxError` this is because we haven't told node we want to execute TS. So we need to install ts-node to do that. We will also be installing nodemon to help with live refreshing during development.

In the terminal execute the command

```zsh
npm i -D nodemon ts-node
```

After installing the dependencies update **scripts** in the `package.json` to the following:

```json
{
  "scripts": {
    "build": "npx tsc",
    "start": "node dist/index.js",
    "dev": "nodemon src/index.ts"
  }
}
```

And that is it!

## Sources

[LogRocket - How to set up TypeScript with Node.js and Express](https://blog.logrocket.com/how-to-set-up-node-typescript-express/)
