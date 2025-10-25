# Task 1.1 Script Report

### `validateUsername(username)`

This function validates the username input field. It uses a regular expression to ensure the username is alphanumeric and between 4 and 20 characters in length. If the validation fails, it calls `showError`; otherwise, it calls `clearError`.

### `validateEmail(email)`

This function validates the email input field. It employs a regular expression to check for a valid email format (e.g., `user@example.com`). It provides feedback by calling `showError` for invalid formats or `clearError` for valid ones.

### `validatePassword(password)`

This function checks the password for complexity requirements. The password must be at least 8 characters long and contain at least one uppercase letter and one number. It uses `showError` to display the requirements if they are not met.

### `validatePasswordMatch(pass1, pass2)`

This function ensures that the entered passwords in the password and confirm password fields are identical. It is crucial for preventing user typos during password creation. It shows an error if the passwords do not match.

### `showError(fieldId, message)`

This utility function is responsible for displaying validation errors to the user. It adds a red border to the invalid input field and displays a descriptive error message below it. This provides clear, immediate feedback.

### `clearError(fieldId)`

This function is the counterpart to `showError`. It removes the error styling and message from a form field when the input becomes valid. It also adds a green border to indicate a valid field.

### `validateForm()`

This function serves as the central validator for the entire form. It calls all the individual validation functions and checks their return values. The "Sign Up" button is enabled only when all fields are valid.
