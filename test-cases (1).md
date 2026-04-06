# Test Cases – Student Task Manager

## Overview

The following test cases validate the key functional requirements of the Student Task Manager application. Each test case is linked to a requirement defined in the SRS.

---

## Test Case Table

| Test Case ID | Requirement | Test Description | Expected Result |
|---|---|---|---|
| TC-01 | User registration | User enters a valid name, email, and password and submits the registration form | Account is created and user is redirected to the dashboard |
| TC-02 | Email validation | User enters an improperly formatted email address (e.g., "userATmail.com") during registration | System rejects submission and displays "Please enter a valid email address" |
| TC-03 | Required field validation | User attempts to create a new task without entering a task name | Error message displayed: "Task name is required" |
| TC-04 | Task creation | User fills in all required fields (task name, due date, priority) and submits | Task appears in the dashboard task list with correct details |
| TC-05 | Due date validation | User enters a due date that is in the past | System rejects the date and displays "Due date must be today or a future date" |
| TC-06 | Task completion | User clicks the "Mark Complete" button on an existing task | Task is moved to the completed section and marked with a checkmark |
| TC-07 | Task deletion | User clicks the "Delete" button on a task and confirms the action | Task is permanently removed from the task list |
| TC-08 | Authentication gate | User attempts to access the dashboard URL without being logged in | User is redirected to the login page |
