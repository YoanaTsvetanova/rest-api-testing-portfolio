# API Test Cases

## Project Information

- **Project:** REST API Testing Portfolio
- **API Under Test:** [JSONPlaceholder](https://jsonplaceholder.typicode.com)
- **Tool:** Postman
- **Test Type:** API Functional Testing
- **Execution Status:** Completed

---

## API-TC-001: Retrieve All Posts

**Request:** GET `/posts`

**Objective:** Verify that the API returns a list of posts.

**Test Steps:**
1. Send a GET request to `/posts`.
2. Verify the HTTP response status.
3. Validate the response body.
4. Check that the response contains 100 posts.

**Expected Result:**
- Status code: `200 OK`
- Response body is a JSON array.
- The array contains 100 posts.
- Each post contains `userId`, `id`, `title`, and `body`.

**Actual Result:** API returned `200 OK` with an array of 100 posts.

**Status:** PASS

---

## API-TC-002: Retrieve a Single Post

**Request:** GET `/posts/1`

**Objective:** Verify that a specific post can be retrieved.

**Test Steps:**
1. Send a GET request to `/posts/1`.
2. Verify the response status.
3. Validate the response fields.
4. Check that the returned post ID is `1`.

**Expected Result:**
- Status code: `200 OK`
- Response body is a JSON object.
- The post ID equals `1`.
- `userId` is a number.
- `title` and `body` are not empty.

**Actual Result:** API returned `200 OK` with the expected post data.

**Status:** PASS

---

## API-TC-003: Retrieve a Non-Existing Post

**Request:** GET `/posts/9999`

**Objective:** Verify API behavior when requesting a post that does not exist.

**Test Steps:**
1. Send a GET request to `/posts/9999`.
2. Verify the response status.
3. Check that the response time is below 2000 ms.

**Expected Result:**
- Status code: `404 Not Found`.
- Response time is below 2000 ms.

**Actual Result:** API returned `404 Not Found`.

**Status:** PASS

---

## API-TC-004: Create a New Post

**Request:** POST `/posts`

**Test Data:**
- title: `QA Testing Practice`
- body: `This is a test post created using Postman.`
- userId: `1`

**Objective:** Verify that a new post can be submitted.

**Test Steps:**
1. Send a POST request with the JSON test data.
2. Verify the response status.
3. Validate the returned post fields.
4. Verify that the response contains an ID.

**Expected Result:**
- Status code: `201 Created`.
- Response contains `id`, `title`, `body`, and `userId`.
- Returned values match the submitted data.

**Actual Result:** API returned `201 Created` with the expected fields and an ID.

**Status:** PASS

---

## API-TC-005: Update an Existing Post

**Request:** PUT `/posts/1`

**Objective:** Verify that an existing post can be updated.

**Test Steps:**
1. Send a PUT request with the updated JSON data.
2. Verify the response status.
3. Validate the returned fields.
4. Check that the returned values match the request data.

**Expected Result:**
- Status code: `200 OK`.
- Response contains the updated post data.
- The returned ID is `1`.

**Actual Result:** API returned `200 OK` with the expected updated fields.

**Status:** PASS

---

## API-TC-006: Partially Update a Post

**Request:** PATCH `/posts/1`

**Test Data:**
- title: `Partially Updated QA Post`

**Objective:** Verify that a single field can be partially updated.

**Test Steps:**
1. Send a PATCH request with the updated title.
2. Verify the response status.
3. Validate the response body.
4. Check that the returned title matches the submitted value.
5. Verify that the response contains only the updated title field.

**Expected Result:**
- Status code: `200 OK`.
- Response contains the updated title.
- Response contains only the `title` field.

**Actual Result:** API returned `200 OK` with only the updated title field.

**Status:** PASS

---

## API-TC-007: Delete an Existing Post

**Request:** DELETE `/posts/1`

**Objective:** Verify that a delete request is processed successfully.

**Test Steps:**
1. Send a DELETE request to `/posts/1`.
2. Verify the response status.
3. Check that the response body is empty or contains an empty JSON object.
4. Verify that the response time is below 2000 ms.

**Expected Result:**
- Status code: `200 OK`.
- Response body is empty or `{}`.
- Response time is below 2000 ms.

**Actual Result:** API returned `200 OK` with an empty response body or empty JSON object.

**Status:** PASS

---

## Test Execution Summary

| Metric | Result |
|---|---:|
| Total test cases | 7 |
| Passed | 7 |
| Failed | 0 |
| Not executed | 0 |

## Notes

JSONPlaceholder is a fake online REST API for testing and prototyping. POST, PUT, PATCH, and DELETE requests simulate write operations; changes are not permanently saved to the server.

The results documented above reflect the individual Postman request executions.
