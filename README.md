# ParaBank Registration Test Automation

## Overview
This project contains automated test scripts for the ParaBank website registration functionality using Selenium, pytest, and webdriver-manager.

## Test Cases

### 1. Positive Test Case
**Test: User successfully registers with valid credentials**
- Tests successful registration with all valid information
- Verifies that the user can complete registration flow
- Expected: Registration should be successful

### 2. Negative Test Case 1
**Test: Registration fails with empty required fields**
- Tests registration with empty First Name (required field)
- Verifies proper error handling for missing required fields
- Expected: Registration should fail with error message

### 3. Negative Test Case 2
**Test: Registration fails with mismatched passwords**
- Tests registration when password and confirm password don't match
- Verifies password validation
- Expected: Registration should fail with password mismatch error

### 4. Negative Test Case 3
**Test: Registration fails with invalid SSN format**
- Tests registration with invalid SSN format (letters instead of numbers)
- Verifies SSN format validation
- Expected: Registration should fail with SSN validation error

## Requirements
- Python 3.7+
- Selenium 4.15.2
- pytest 7.4.3
- webdriver-manager 4.0.1

## Installation

1. Clone the repository
2. Create a virtual environment (optional):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Running Tests

Execute all tests:
```bash
pytest test_parabank_registration.py -v -s
```

Run a specific test:
```bash
pytest test_parabank_registration.py::TestParaBankRegistration::test_positive_case_successful_registration -v
```

## Test Results
Screenshots of test results are saved to the `test_results/` directory.

## Project Structure
```
se_automation/
├── test_parabank_registration.py
├── requirements.txt
├── README.md
└── test_results/
    ├── positive_case_result.png
    ├── negative_case_1_result.png
    ├── negative_case_2_result.png
    └── negative_case_3_result.png
```

## Test Execution Flow

1. WebDriver setup (Chrome)
2. Navigate to ParaBank registration page
3. Fill registration form with test data
4. Click Register button
5. Capture screenshot of result
6. Verify expected behavior
7. Generate test report

## Notes
- Tests use Chrome WebDriver (automatically managed by webdriver-manager)
- Screenshots are automatically captured for each test
- Tests include both positive and negative scenarios
- All test cases use Gherkin syntax as comments within the test script

## Author
QA Automation Team
