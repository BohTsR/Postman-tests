# Postman API Testing Project

This repository contains automated API tests for the `strip.strip.serve.vdm` endpoint, designed and executed using [Postman](https://www.postman.com/) and documented for review.

## Contents

- `postman_collection.json` – Exported Postman collection including all test cases
- `postman_test_run` – Summary of test results (structure, validation, error handling)
- `README.md` – Project overview and setup instructions

## Test Scenarios

The collection includes validation for the following scenarios:

| Scenario              | Status Code | Description                            |
|----------------------|-------------|----------------------------------------|
| Structure validation | 200         | Validates presence and structure of response fields |
| Invalid parameters   | 200         | Tests with incorrect parameter types or values       |
| Validation error     | 200         | Missing required fields (e.g. `slug`)  |
| Strip not found      | 200         | Invalid `slug` value                   |
| Parse error          | 500         | Malformed JSON (invalid syntax)        |
| Unexpected parameter | 200         | Injection/masking test with extra param |

## Requirements

- [Postman](https://www.postman.com/downloads/)

## How to Use

### Run in Postman
1. Import `postman_collection.json` into Postman
2. Open the collection and select a request
3. Click **Send** to execute, or use **Collection Runner** for full test suite


## Test Report
Refer to `test-report.xlsx` or `test-report.md` for structured results including:
- Expected vs Actual behavior
- Pass/Fail outcomes
- Notes on each test scenario
