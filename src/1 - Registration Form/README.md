# Registration Form

### Description

Create a comprehensive registration form that allows users to input their personal information, including their name, email address, and password. The form should not only validate the input data but also enhance user experience through clear feedback and responsiveness. This challenge will assess your ability to manage form state, implement client-side and server-side validation, and create an intuitive user interface.

### Challenge Requirements

#### 1. Form Fields

The registration form should consist of the following fields:

- **Name**
  - Type: Text
  - Placeholder: "Enter your full name"
  - Validation: Required field (should not be empty)
- **Email**
  - Type: Text
  - Placeholder: "Enter your email address"
  - Validation:
    - Required field (should not be empty)
    - Must follow a valid email format (e.g., `user@example.com`)
- **Password**

  - Type: Password
  - Placeholder: "Create a password"
  - Validation:
    - Required field (should not be empty)
    - Minimum length of 8 characters
    - Must contain at least one uppercase letter, one lowercase letter, one digit, and one special character (e.g., `!@#$%^&*`)

- **Confirm Password**

  - Type: Password
  - Placeholder: "Confirm your password"
  - Validation:
    - Required field (should not be empty)
    - Must match the password entered above

- **Submit Button**
  - Label: "Register"
  - Action: On click, validate all fields and, if valid, submit the form data.

#### 2. Validation

Implement both client-side and server-side validation for the form fields:

- **Client-side Validation**:

  - Use JavaScript to validate user input when the user attempts to submit the form.
  - Provide instant feedback for each field, displaying error messages inline (e.g., under the respective field) when validation fails.
  - Highlight the fields in red or another noticeable color when they contain invalid input.

- **Server-side Validation** (optional if a backend is provided):
  - Ensure that the server checks for the same validation criteria to prevent invalid data from being processed.
  - Respond with appropriate error messages if validation fails on the server.

#### 3. User Feedback

- After successful form submission:
  - Display a confirmation message (e.g., "Registration successful! Please check your email to verify your account.")
  - Optionally, redirect the user to a new page or reset the form fields.
- If validation errors occur:
  - Ensure that error messages are user-friendly and provide guidance on how to correct the mistakes (e.g., "Please enter a valid email address." or "Passwords do not match.").

#### 4. Styling

- Use CSS to style the form in a clean, modern, and visually appealing manner:
  - Ensure that the form is centered on the page and responsive, adapting to different screen sizes.
  - Style the error messages in a way that they are easily noticeable (e.g., using red text or an icon).
  - Add hover and focus effects to input fields to enhance user experience.

#### 5. Recommended Technologies

- **Frontend Framework:** React (or another framework/library of your choice)
- **CSS Framework:** Consider using Bootstrap, Tailwind CSS, or plain CSS for styling.

### Challenge Objective

This challenge is designed to assess your ability to:

- Build a fully functional registration form with multiple fields.
- Implement comprehensive input validation.
- Provide clear user feedback and error handling.
- Create a responsive and user-friendly interface.

### Tips

- Utilize libraries such as `React Hook Form` or `Formik` for efficient form management and validation.
- Leverage the HTML5 input types and attributes (like `required`, `pattern`, and `minLength`) to simplify validation.
- Test your form thoroughly to ensure all validation rules are correctly applied and that user feedback is accurate.

### Final Considerations

Remember that the focus of this challenge is on both functionality and user experience. Pay attention to code quality, maintainability, and responsiveness. Your implementation should demonstrate a clear understanding of best practices in frontend development.
