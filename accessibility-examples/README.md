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

## Image Descriptions Example

This example demonstrates proper alt text and ARIA labels for images and icons in an admin dashboard.

### File

**image-descriptions.html**
- Shows a PMI admin dashboard with various image types
- Demonstrates proper text alternatives for different image contexts
- Includes company logo, functional icons, and decorative icons

### Image Types and Descriptions

| Image Type | Text Description | Implementation |
|------------|-----------------|----------------|
| Company logo | "PMI - Project Management Institute" | `aria-label` on logo container |
| Edit icon (functional) | "Edit user [Name]" | `aria-label` on button, icon marked `aria-hidden="true"` |
| Delete icon (functional) | "Delete user [Name]" | `aria-label` on button, icon marked `aria-hidden="true"` |
| Close icon (functional) | "Close dialog" | `aria-label` on button, icon marked `aria-hidden="true"` |
| Decorative icons | Not announced | `aria-hidden="true"` on icon, parent element has accessible text |

### Key Features

- **Functional icons**: Have descriptive `aria-label` on the interactive element (button/link)
- **Decorative icons**: Marked with `aria-hidden="true"` so screen readers skip them
- **Context-specific descriptions**: Icons include context (e.g., "Edit user Sarah Johnson" not just "Edit")
- **Logo accessibility**: Company logo announced with full name
- **Dashboard cards**: Icon is decorative, card title provides the accessible name
- **Consistent patterns**: Similar icons use similar description patterns

### Key Insight

**Icons need text alternatives only when they convey unique information.** When an icon is paired with visible text or when the parent element has an accessible name, mark the icon as decorative with `aria-hidden="true"`. For functional icon-only buttons, provide a descriptive `aria-label` that includes context.

## Informative Images Example

This example demonstrates proper alt text for informative images that convey meaningful content.

### File

**informative-images.html**
- Shows a project portfolio page with various informative images
- Each image conveys important information that must be accessible
- Demonstrates detailed, descriptive alt text

### Image Types and Alt Text

| Image Type | Alt Text |
|------------|----------|
| Company logo | "PMI - Project Management Institute" |
| Team photo | "Product design team at 2025 offsite in Denver" |
| Certification badge | "PMP certification badge", "PMI-ACP certification badge", "CSM certification badge" |
| Chart/graph | "Bar chart showing project completion rates by quarter: Q1 85%, Q2 92%, Q3 88%, Q4 95%" |

### Key Features

- **Descriptive alt text**: Each image has meaningful description of what it shows
- **Complete information**: Alt text includes all important data (like chart values)
- **Context provided**: Images describe what, where, and when relevant
- **Certification badges**: Each badge identified by certification type
- **Data visualization**: Chart alt text includes all data points and labels

### Key Insight

**Informative images require descriptive alt text that conveys the same information as the image.** For charts and graphs, include the data in the alt text. For photos, describe what's in the image and provide relevant context. The alt text should allow someone who can't see the image to understand the same information.


