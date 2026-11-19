# Automation Exercise - API Testing

## Overview

This project contains API tests for the [Automation Exercise](https://automationexercise.com/) website using Postman.

The collection covers positive and negative test scenarios. Postman test scripts include assertions to validate API responses and expected behavior.

## Tools & Technologies

- Postman
- JavaScript (Postman Test Scripts)
- Newman

## Prerequisites

- [Postman](https://www.postman.com/downloads/)
- [Node.js and npm](https://nodejs.org/) (required for Newman)

## Project Setup

1. Clone or download this repository.
2. Open Postman and click **Import**.
3. Import the exported Collection JSON file.
4. Import the exported Environment JSON file.
5. Select **Automation Exercise - Environment** from the environment selector.
6. Make sure the required environment variables are configured.

**Base URL:**

```text
https://automationexercise.com/api
```

## Running the Collection

### 1. Using Postman Collection Runner

1. Open the imported collection in Postman.
2. Select **QA/Test** from the environment selector.
3. Click **Run** to open the Collection Runner.
4. Click **Run Collection** to execute all requests and test scripts.
5. Review the collection execution results.

### 2. Using Newman CLI

Newman allows you to execute Postman collections directly from the command line.

**Step 1: Install Newman**

```bash
npm install -g newman
```

**Step 2: Run the Collection**

From the project root directory, execute:

```bash
newman run postman/automation-exercise-api-testing.postman_collection.json -e postman/automation-exercise-environment.postman_environment.json
```

Make sure the file paths match your actual exported file names and locations.

## Test Results

After execution, you can review:

- Passed and failed assertions.
- Request execution results.
- Total number of executed tests.

Postman displays the results in Collection Runner, while Newman displays them directly in the terminal.

## API Documentation

For more information about the available endpoints, refer to the [Automation Exercise API Documentation](https://automationexercise.com/api_list).
