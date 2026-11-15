# Playwright Setup & CodeGen

Barakah TechLabs internship, Task 1: Playwright Setup & CodeGen.

## What this project does
- Sets up Playwright with TypeScript.
- Uses `npx playwright codegen` to record a login flow on https://www.saucedemo.com.
- Turns the recording into a clean baseline test with assertions.

## Tests
- **Valid login:** the user reaches the inventory page and sees "Products".
- **Invalid password:** an error message is shown.

## Tech stack
Playwright, TypeScript, Trace Viewer, Browser Contexts

## Project structure
- `tests/login.spec.ts`: the login tests
- `playwright.config.ts`: browser settings, with trace and screenshots turned on

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
4 tests passed (2 tests on Google Chrome and Microsoft Edge). Traces are enabled, so every step can be inspected in Trace Viewer.

## Why