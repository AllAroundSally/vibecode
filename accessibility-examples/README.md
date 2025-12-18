# Accessibility Annotation UI Examples

This directory contains UI examples created for annotating designs for accessibility presentations, following the principles from TetraLogical's article on annotating designs using common language.

## Email Validation Error Examples

These examples demonstrate a registration form with different email validation error states, styled to match PMI (Project Management Institute) design patterns.

### Files

1. **email-validation-blank.html**
   - Error state: Empty email field
   - Error message: "Enter your email"
   - Scenario: User submits the form without entering an email address

2. **email-validation-missing-at.html**
   - Error state: Email missing "@" character
   - Error message: "Your email must include an '@' character"
   - Example value: "johndoeemail.com"
   - Scenario: User enters email without the @ symbol

3. **email-validation-missing-dot.html**
   - Error state: Email missing "." character
   - Error message: "Your email must include a '.' character"
   - Example value: "johndoe@emailcom"
   - Scenario: User enters email without a period in the domain

### Accessibility Features

Each error example includes:
- `aria-invalid="true"` on the input field to indicate validation error
- `aria-describedby` linking to the error message ID
- `role="alert"` on error messages for screen reader announcements
- Visual error indicators (red border, background tint, warning icon)
- Clear, specific error messaging using common language
- Proper color contrast for error states

### Usage

Open any of the HTML files in a web browser to view the error states. These can be used as:
- Design annotation examples for presentations
- Reference for implementing accessible error messaging
- Visual aids for training on accessibility best practices

### Styling

The forms use PMI-inspired styling with:
- Purple primary color (#3d2e7c)
- Clean, modern typography
- Rounded buttons and form fields
- Proper spacing and visual hierarchy
- Responsive design principles

## Dialog Focus Sequence Example

This example demonstrates proper keyboard navigation order in a delete confirmation dialog.

### File

**dialog-focus-sequence.html**
- Demonstrates correct focus order for keyboard navigation
- Shows a modal dialog with delete confirmation
- Focus sequence: Close button → Cancel button → Delete button (destructive action last)

### Key Features

- **Proper focus order**: Destructive actions (Delete) are placed last in the tab sequence for safety
- **Destructive action styling**: Delete button is styled in red to indicate danger
- **Focus management**: Tab key cycles through interactive elements in the correct order
- **Focus trap**: Keyboard focus stays within the modal dialog
- **Visual focus indicators**: Clear visual feedback shows which element has focus
- **Focus annotations**: Purple labels show the focus order sequence (1, 2, 3)
- ARIA attributes: `role="dialog"`, `aria-modal="true"`, `aria-labelledby`
- Escape key support for closing the dialog

### Key Insight

**Place destructive actions last in focus order for safety.** This prevents users from accidentally triggering dangerous actions when navigating with a keyboard. The natural tab order should guide users from safe actions (close, cancel) to destructive actions (delete) last.
