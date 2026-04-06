# Test Strategy – Student Task Manager

## 1. System Overview

**System Purpose:**
The Student Task Manager is a web-based application that allows students to create, organize, and track their academic assignments and deadlines. The system enables users to add tasks with due dates and priority levels, mark tasks as complete, and view upcoming deadlines in a simple dashboard interface.

**Primary Users:**
- College and high school students managing coursework and assignments

**Major Features:**
- User registration and login
- Create, edit, and delete tasks
- Set due dates and priority levels (High, Medium, Low)
- Mark tasks as complete
- Dashboard view showing upcoming and overdue tasks

---

## 2. Testing Approach

**Unit Testing:**
Each individual component of the system will be tested in isolation. For example, the function that validates a due date input will be tested independently to confirm it correctly rejects past dates and accepts future ones. Similarly, the task creation function will be tested to verify it correctly stores all required fields. Unit tests will be written for all core backend logic including input validation, data formatting, and task status updates.

**Integration Testing:**
Integration testing will verify that the frontend and backend components communicate correctly. For example, when a user submits a new task through the form, integration tests will confirm that the data is correctly received by the server, stored in the database, and returned to the frontend as expected. The connection between the authentication system and the task management system will also be tested to ensure only logged-in users can create or modify tasks.

**System Testing:**
System testing will evaluate the entire application end-to-end as a complete product. A full user workflow will be simulated: registering an account, logging in, creating a task, editing it, marking it complete, and deleting it. System testing will also verify that the dashboard correctly reflects real-time task status and that the application behaves consistently across different browsers.

**User Acceptance Testing (UAT):**
UAT will be conducted by having a small group of actual students use the application and complete a set of predefined tasks without assistance. Testers will be asked to register, add three tasks with different priority levels, and mark one complete. Their feedback will be used to verify that the interface is intuitive and that the system meets the original requirements as defined in the SRS.

---

## 3. Test Environment

- **Local Development Environment:** All unit and integration tests will be run locally using a development build of the application running on localhost. A local database instance will be used to avoid affecting any production data.
- **Staging Environment:** Before any release, the full application will be deployed to a staging server that mirrors the production environment. System testing will be performed here to catch any environment-specific issues.
- **Browser Testing:** The application will be tested across Chrome, Firefox, and Safari to ensure cross-browser compatibility. Each major feature will be manually verified in each browser.
- **Simulated User Interactions:** UAT scenarios will be scripted as step-by-step walkthroughs given to test users, simulating realistic usage patterns such as adding tasks before a deadline or logging in from a new device.
