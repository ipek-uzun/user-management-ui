# User Management Screen Specification

## Overview

This document outlines the user interface specification for the User Management screen. It is intended for software developers responsible for implementing the interface.

The UI provides functionalities to:

- View the list of users.
- Add a new user.
- Edit existing users.
- Filter and manage user records.
- Layout and Components

## Main Components

### User Table

- **Columns**:
    -  **ID**: Displays the unique identifier of each user.
    - **User Name**: Displays the username.
    - **Email**: Displays the user's email address.
    - **Enabled**: Indicates whether the user is active or disabled (Boolean value).
- **Sorting**: Each column can be sorted in ascending or descending order by clicking on the arrow icon.

- **Filtering**: Users can filter data in columns using the filter icon.

### **Hide Disabled User Checkbox**
    - **Purpose**: Toggles visibility of disabled users in the table.
    - **Default Behavior**: Checked by default, hiding disabled users.

## New User Form

- **Fields**:

    - **Username (required)**: Input for the user's unique identifier.

    - **Display Name (optional)**: Input for the user's display name.

    - **Phone (optional)**: Input for the user's phone number.

    - **Email (required)**: Input for the user's email address.

    - **User Roles (required)**: Dropdown to select one or multiple roles (e.g., Guest, Admin, SuperAdmin).

    - **Enabled (checkbox)**: Checkbox to indicate whether the user is active.

- **Validation**:

    - Required fields must not be empty.

    - Email field should validate a proper email format.

    - Phone number (if entered) should only allow numeric values.

- **Buttons**:

    - **New User**: Opens the form to create a new user.
    - **Save User**: Saves the new or edited user.

## Page Behavior

### **Initial State**

- The user table loads with all active users displayed.

 - The "Hide Disabled User" checkbox is checked by default.

- The "New User" form is hidden until triggered by the "New User" button.

### User Actions

- **Viewing Users**:

    - Users can scroll through the table to view records.

    - Sorting and filtering are dynamic, with results updated in real-time.

- **Adding a New User**:

    - Clicking the "New User" button displays the empty form.

    - The form must validate inputs before submission.

    - Upon successful addition, the new user is displayed in the table.

- **Editing an Existing User**:

    - Clicking a row in the table populates the form with the selected user’s details for editing.

    - Save changes with the "Save User" button after validation.

- **Filtering and Sorting**:

    - Filters apply to visible columns only.

    - Sorting persists across actions until manually reset.

### Error Handling**

- **Form Validation**:

    - Display error messages below invalid fields.

- **System Errors**:

    - Show a toast notification at the top-right corner with error details (e.g., "Failed to load user data.").

- **Responsive Design**

   - The layout should adjust to fit smaller screens.

    - The table should support horizontal scrolling if columns exceed the screen width.

## **Requirements**

- **UI Framework**: Use a standard component-based library (e.g., React, Angular, or Vue).

- **Styling**: Follow existing design guidelines for color, typography, and spacing.

- **Backend Integration**:

    - The table must dynamically fetch data from the backend API.

    - Ensure proper API endpoints for user creation, updates, and retrieval.

- **Accessibility**:

    - Ensure all form fields and buttons are accessible via keyboard navigation.

    - Add appropriate ARIA labels for screen readers.

- **Testing**:

    - Perform unit tests on components.

    - Conduct end-to-end testing to validate functionality and behavior.

