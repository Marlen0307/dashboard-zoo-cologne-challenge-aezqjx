# Cologne Zoo Dashboard

## Table of Contents

- [Description](#description)
- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Development](#development)
- [Scripts](#scripts)
- [Linting](#linting)
- [Testing](#testing)
- [Dependencies](#dependencies)

## Description

This project is a web dashboard whose purpose is to provide to the zookeepers information about tha animals that are living in the zoo. This application is built using Typescript.

## Features

- Listing of animals in the zoo
- Providing health info for all of the animals in the zoo

## Getting Started

### Prerequisites

Make sure you have the following software installed:

- Node.js (recommended version: 16.14.2)
- npm (recommended version: 8.5.0)

### Installation

- Download project from the [Stackblitz project](https://stackblitz.com/edit/dashboard-zoo-cologne-challenge-aezqjx?file=TASKS.md&terminal=hello)
- Run `npm install`

### Development

To start the development server:

```bash
npm run dev
```

Visit http://localhost:3000 in your web browser to see your project in action. If you are running the project on Stackblitz, you will see the project in the right Pane.

### Scripts

- `dev`: Start the development server
- `build`: Build the project for production. Used with SSR
- `start`: Serve the production build
- `lint`: Lint the project files with eslint
- `lint:types`: Check types through app
- `lint:style`: Check style linting through the app
- `test`: Run tests in run mode
- `test:watch`: Run tests in watch mode
- `prepare`: Enable Husky git hooks
- `test-for-reviewer`: Build the appp and run the tests in run mode

### Linting

In this project we use two main linting tasks to keep code consistency, prevent errors and stick to best practices

- `lint:types`: This task performs type checking using the Nuxt Typechecker (nuxi typecheck) to ensure type correctness within the codebase.
- `lint:style`: This task uses ESLint to check code for style violations. ESLint checks for coding style issues, formatting inconsistencies, and potential errors.

If you want to run both tasks:

```bash
npm run lint
```

### Testing

This project uses `vitest` for unit testing

- To run tests
  ´´´bash
  npm run test
  ´´´

- To run tests in watch mode
  ´´´bash
  npm run test:watch
  ´´´

### Dependencies

- Nuxt
- Vue.Js
