# REST API Testing Portfolio

A practical REST API Testing portfolio project using Postman and JavaScript. This project demonstrates API testing techniques, automated response validation, positive and negative testing, and test documentation.

## Project Overview

The project uses JSONPlaceholder, a free REST API, to practise and demonstrate API testing skills.

## Tools & Technologies

- Postman
- REST API
- JavaScript
- JSON
- GitHub

## API Under Test

**JSONPlaceholder**

https://jsonplaceholder.typicode.com

## Test Coverage

| HTTP Method | Test Scenario | Expected Status |
|---|---|---|
| GET | Retrieve all posts | 200 OK |
| GET | Retrieve a single post | 200 OK |
| GET | Retrieve a non-existing post | 404 Not Found |
| POST | Create a new post | 201 Created |
| PUT | Update an existing post | 200 OK |
| PATCH | Partially update a post | 200 OK |
| DELETE | Delete an existing post | 200 OK |

## Automated Validations

- HTTP status code validation
- Response time validation
- JSON response structure validation
- Required field validation
- Data type validation
- Response body validation
- Positive and negative test scenarios

## Project Structure

```text
rest-api-testing-portfolio/
├── postman/
│   └── collections/
│       ├── README.md
│       └── JSONPlaceholder_API_Testing.postman_collection.json
├── test-cases/
├── test-evidence/
└── README.md
```

## How to Run the Tests

1. Download and install Postman.
2. Download the exported JSON collection from this repository.
3. Open Postman.
4. Import the JSON collection.
5. Select a request and click Send.
6. Review the automated assertions under Test Results.

## Project Status

The complete Postman collection was executed successfully using the Postman Collection Runner.

| Metric | Result |
|---|---:|
| Requests executed | 7 |
| Assertions passed | 31 |
| Failed assertions | 0 |

**Execution status:** PASS

All seven API requests completed successfully, and all 31 test assertions passed.
Completed initial API testing collection with positive and negative scenarios and automated JavaScript assertions.

**Note:** JSONPlaceholder simulates data creation, updates, and deletion. These operations do not permanently modify the sample data.
