# Playwright Setup & CodeGen

Barakah TechLabs internship, Task 1: Playwright Setup & CodeGen.

## What this project does
- Sets up Playwright with TypeScript.
- Uses `npx playwright codegen` to record a login flow on https://www.saucedemo.com.
- Turns the recording into a clean baseline test with assertions.

## Tests
- Valid login: the user reaches the inventory page and sees "Products".
- Invalid password: an error message is shown.

## Tech stack
Playwright, TypeScript, Trace Viewer, Browser Contexts

## How to run
```bash
npm install
npx playwright install
npx playwright test
npx playwright show-report
```

## How the test was created
```bash
npx playwright codegen https://www.saucedemo.com
```
CodeGen recorded my clicks and typing. I then removed the extra steps and added assertions.

## Results
6 tests passed (2 tests across Chromium, Firefox and WebKit). Traces are enabled, so every step can be inspected in Trace Viewer.

## Why TypeScript over JavaScript?
- **Type safety:** mistakes are caught before the tests run.
- **Autocomplete:** better suggestions in the editor.
- **Safe refactoring:** renaming across many files is easier.
- **Maintainability:** clear contracts for helper functions and page objects in large teams.

## Note
The Chromium project uses the installed Google Chrome (`channel: 'chrome'`).