# SQA Manual Testing & API Automation Portfolio

Welcome to my Software Quality Assurance (SQA) repository! This space showcases my practical, hands-on work in manual software testing, test case design, defect logging, and API manual & automated testing.

---

## 📂 Featured Projects

### 1. YouTube Search & Playback Testing Suite
*   [**Test Plan**](./YouTube_Search_Test_Plan.md): Defines the scope, environment, testing types, and risk mitigations for the search and playback features.
*   [**Test Cases**](./YouTube_Search_Test_Cases.md): 10 detailed manual test cases executing the scenarios defined in the test plan.

### 2. [Papertrace Web App Bug Reports](./Papertrace_Bug_Reports.md)
*   **Description:** A set of 3 formal, detailed bug reports identifying UI, functional, and input-limit defects discovered during testing of the Papertrace web application.
*   **Skills Demonstrated:** Defect investigation, clear step-by-step reproduction instructions, severity/priority assessment, and visual bug reporting.

### 3. [ReqRes API Manual & Automated Testing](./API%20Testing.postman_collection.json)
*   **Description:** A complete API testing suite verifying CRUD (Create, Read, Update, Delete) operations using both manual endpoint inspection and automated JavaScript post-response assertions in Postman.
*   **Skills Demonstrated:** Manual endpoint verification, custom header configuration (`x-api-key`), automated status and schema assertions, and JSON error debugging.

---

## 📌 API Test Project Deep Dive (Manual & Automated)

The objective of this project was to verify the behavior, structure, and reliability of core REST API endpoints on the ReqRes sandbox, transitioning from manual verification to automated post-response scripting.

### 🛠️ Manual Testing Scope & Scenarios Covered
Before writing scripts, I manually constructed and executed requests to verify CRUD behavior:
1.  **GET (Read) - Retrieve Users:** Manually checked user listing behavior. Verified custom headers, query parameters, and inspected the JSON structure to confirm a `200 OK` status.
2.  **POST (Create) - Register User:** Sent a raw JSON request body containing profile parameters (`name: "Mawa"`, `job: "QA Specialist"`). Verified resource creation, inspected the returned schema, and confirmed the `201 Created` status.
3.  **PUT (Update) - Update Profile:** Transmitted modified payload details to verify data update handling. Confirmed response headers and `200 OK` status.
4.  **DELETE (Delete) - Remove User:** Tested resource teardown mechanisms. Manually verified the standard empty response and `204 No Content` status.
5.  **Error Handling & Security:** Configured headers to pass authorization credentials (`x-api-key`) and handled a `401 Unauthorized` debugging scenario to test access restrictions.

---

###  JavaScript Test Automation Scripts
To optimize testing efficiency, I transitioned the manual verification steps into automated assertions inside Postman's **Scripts (Post-response)** tab. These scripts execute automatically the millisecond a response is returned:

*   **Status Code Validation (GET & POST):**
    ```javascript
    pm.test("Status code is 200", function () {
        pm.response.to.have.status(200);
    });
    ```
    *(And verified `201 Created` for POST creation and `204 No Content` for DELETE paths).*

*   **Payload Validation (Checking GET list elements):**
    ```javascript
    pm.test("Response contains data", function () {
        var jsonData = pm.response.json();
        pm.expect(jsonData.data.length).to.be.above(0);
    });
    ```

*   **Payload Integrity Checks (Verifying POST response fields):**
    ```javascript
    pm.test("Response contains correct name", function () {
        var jsonData = pm.response.json();
        pm.expect(jsonData.name).to.eql("Mawa");
    });
    ```

### ⚠️ Critical SQA Lesson: The "JSON Parsing" Bug
During automation scripting, a test verifying array lengths on the POST endpoint failed with: 
`TypeError: Cannot read properties of undefined (reading 'length')`

*   **The Cause:** Relational APIs return unique JSON schemas depending on the HTTP method. The GET response contained a parent key `"data"` containing an array, whereas the POST response directly returned the newly created user's properties at the JSON's root level without a `"data"` block.
*   **The Fix:** Adjusted assertion targets to align with the unique structural schema of each endpoint payload. 
*   **The Takeaway:** Verification assertions must be carefully customized to match the expected JSON structure of each specific endpoint to avoid false-failing scripts.

### How to Run the Collection
1. Download or clone this repository.
2. Open **Postman**.
3. Click **Import** in the top left and upload the `API Testing.postman_collection.json` file.
4. Provide your own `x-api-key` in the request headers if required, and run the collection via the Collection Runner.

---

## 🛠️ Core Testing Skills Applied

Throughout these projects, I have practiced and applied the following software testing fundamentals:
*   **Requirement Analysis:** Reviewing user-facing features (like search bars, filters, and auth modals) to identify potential edge cases and logic gaps.
*   **Test Design:** Writing detailed, repeatable manual test cases with clear pre-conditions, step-by-step actions, specific test data, and predictable expected results.
*   **API Testing (Manual & Automated):** Executing manual HTTP request validations and authoring JavaScript post-response assertions in Postman to validate data models.
*   **Bug Reporting:** Documenting defect lifecycles using industry-standard attributes (Environment, Severity, Priority, Steps to Reproduce, Expected vs. Actual results, and Visual attachments).
*   **Testing Types:** Functional Testing, Non-Functional Testing, Negative Testing, Smoke Testing, and Exploratory Testing.

---

## About Me

I am an aspiring Software Quality Assurance Engineer dedicated to delivering reliable, user-friendly software. I enjoy diving deep into applications, finding edge cases, and collaborating with developers to resolve defects early in the Software Development Life Cycle (SDLC).

*   **LinkedIn:** https://www.linkedin.com/in/jannatul-mawa-2b0144392/
*   **Email:** jmawa7803@gmail.com
