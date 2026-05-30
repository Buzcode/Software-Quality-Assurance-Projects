# SQA Manual Testing Portfolio

Welcome to my Software Quality Assurance (SQA) repository! This space showcases my practical, hands-on work in manual software testing, test case design, and defect logging.

---

## 📂 Featured Projects

### 1. YouTube Search & Playback Testing Suite
*   [**Test Plan**](./YouTube_Search_Test_Plan.md): Defines the scope, environment, testing types, and risk mitigations for the search and playback features.
*   [**Test Cases**](./YouTube_Search_Test_Cases.md): 10 detailed manual test cases executing the scenarios defined in the test plan.

### 2. [Papertrace Web App Bug Reports](./Papertrace_Bug_Reports.md)
*   **Description:** A set of 3 formal, detailed bug reports identifying UI, functional, and input-limit defects discovered during testing of the Papertrace web application.
*   **Skills Demonstrated:** Defect investigation, clear step-by-step reproduction instructions, severity/priority assessment, and visual bug reporting.

---

# ReqRes API Testing (Postman Collection)

This repository contains a complete manual API testing suite for verifying CRUD (Create, Read, Update, Delete) operations using Postman and the [ReqRes API](https://reqres.in/).

## 📌 Project Overview
The objective of this project was to verify the behavior, structure, and reliability of core API endpoints. It covers setting up custom authentication headers, constructing JSON request bodies, and validating various HTTP response status codes.

## 🛠️ Testing Scope & Scenarios Covered
1. **GET (Read) - Retrieve Users:** Checked user listing behavior. Verified headers, query parameters, and received a `200 OK` status.
2. **POST (Create) - Register User:** Sent a raw JSON request body containing user details. Successfully created a resource and verified the `201 Created` status and response payload.
3. **PUT (Update) - Update Profile:** Modified existing user details to test data update handling. Verified response headers and the `200 OK` status.
4. **DELETE (Delete) - Remove User:** Tested resource teardown. Successfully verified the standard `204 No Content` status.

## 🔑 Key Learnings
- **HTTP Status Code Verification:** Successfully handled and mapped status codes including `200 OK`, `201 Created`, `204 No Content`, and handled a `401 Unauthorized` debugging scenario.
- **Header Management:** Configured headers to pass authorization credentials (`x-api-key`).
- **CRUD Life-cycle:** Verified how state changes flow through the API from creation to deletion.

## 🚀 How to Run the Collection
1. Download or clone this repository.
2. Open **Postman**.
3. Click **Import** in the top left and upload the `ReqRes API Testing.postman_collection.json` file.
4. Provide your own `x-api-key` in the request headers if required.

## 🛠️ Core Testing Skills Applied

Throughout these projects, I have practiced and applied the following manual testing fundamentals:
*   **Requirement Analysis:** Reviewing user-facing features (like search bars, filters, and auth modals) to identify potential edge cases and logic gaps.
*   **Test Design:** Writing detailed, repeatable manual test cases with clear pre-conditions, step-by-step actions, specific test data, and predictable expected results.
*   **Bug Reporting:** Documenting defect lifecycles using industry-standard attributes (Environment, Severity, Priority, Steps to Reproduce, Expected vs. Actual results, and Visual attachments).
*   **Testing Types:** Functional Testing, Non-Functional Testing, Negative Testing, Smoke Testing, and Exploratory Testing.

---

## 🚀 About Me

I am an aspiring Software Quality Assurance Engineer dedicated to delivering reliable, user-friendly software. I enjoy diving deep into applications, finding edge cases, and collaborating with developers to resolve defects early in the Software Development Life Cycle (SDLC).

*   **LinkedIn:** https://www.linkedin.com/in/jannatul-mawa-2b0144392/
*   **Email:** jmawa7803@gmail.com
