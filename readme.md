# Facility UI Tests

End-to-end and API test automation project built with **Playwright** and **TypeScript**.
The goal is to provide reliable, maintainable UI tests with clear setup and execution steps.

---

## Installation

### Prerequisites

Make sure you have installed:

- Node.js **v22 or higher**
- npm
- Git

Verify installation:
```bash
node -v
npm -v
```
### Clone the Repository
```bash
git clone <REPO_URL>
cd <PROJECT_FOLDER>
```

### Install Dependencies
```bash
npm install
```

### Install Playwright Browsers
```bash
npx playwright install
```
### On Linux, Playwright may require additional system dependencies:
```bash
npx playwright install-deps
```
### Running Tests

Run all tests
```bash
npx playwright test
```
Run tests in headed mode
```bash
npx playwright test --headed
```
Run a specific test file
```bash
npx playwright test tests/e2e/login.spec.ts
```
⚡ Parallel Execution
Playwright runs tests in parallel by default.

To control workers:
```bash
npx playwright test --workers=4
```
Re-running Tests Multiple Times
To repeat tests multiple times:
```bash
npx playwright test --repeat-each=5
```

### Reporting
After test execution, an HTML report is generated automatically.

To open the report:
```bash
npx playwright show-report
🧹 Linting (Code Quality)
```

Install ESLint (optional but recommended)
```bash

npm install --save-dev eslint
```

Run lint check:
```bash
npx eslint .
```

Fix lint issues automatically:
```bash
npx eslint . --fix
```

### Project Structure
.
├── tests/
│   ├── e2e/                       # UI end-to-end tests
│   └── api/                       # API tests
│
├── pages/                        # Page Object Model (POM)
├── playwright-report/            # Reports
├── utils/                        # Helpers and test data
├── playwright.config.ts
├── package.json
└── README.md