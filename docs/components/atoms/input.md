# Input

## Overview

Input fields allow the user to enter any combination of letters, numbers, or symbols of their choosing (unless otherwise restricted).

`<input>` elements are used within a `<form>` element to declare input controls allow users enter data.

An input field can be specified what data type to accept with its type attribute.

## Usage

### Variations with different data types

| **Visual** | **Input Type** | **Description & Usage** |
| :--- | :--- | :--- |
| ![](../../.gitbook/assets/form_input_text.png) | Text | Text input allows the user to enter any combination of letters, numbers, or symbols of their choosing (unless otherwise restricted). |
| ![](../../.gitbook/assets/form_input_text_number.png) | Number | Number input is used to let the user enter a number. It includes built-in validation to reject non-numerical entries. Browsers that don't support type "number" fall back to using a standard "text" input.  |
| ADD SCREENSHOT | Telephone | Telephone input to let the user enter a telephone number. Unlike `<input type="email">` and `<input type="url">` , the input value is not automatically validated to a particular format before the form can be submitted, because formats for telephone numbers vary so much around the world.  Browsers that don't support type "email" fall back to being a standard "text" input.|
| ADD SCREENSHOT | Email | Email input lets the user to enter and edit an email address. The input value is automatically validated to ensure that it's either empty or a properly-formatted email address before the form can be submitted. Browsers that don't support type "email" fall back to being a standard "text" input. |
| ADD SCREENSHOT | URL | URL input lets the user enter a URL. The input value is automatically validated to ensure that it's either empty or a properly-formatted URL before the form can be submitted. Browsers that don't support type "email" fall back to being a standard "text" input. |
| ADD SCREENSHOT | Password | Password input provides a way for the user to securely enter a password. Entered text is obscured so that it cannot be read, usually by replacing each character with a symbol such as the asterisk ("*") or a dot ("•"). This character will vary depending on the user agent and OS. |
| ![](../../.gitbook/assets/form_input_date.png) | Date | Date input lets the user enter a date, either using a text box that automatically validates the content, or using a special date picker interface. The resulting value includes the year, month, and day, but not the time. In unsupported browsers, the control degrades gracefully a standard "text" input. |

### Other input types:
 
- File Upload

### Accessibility & Best Practices

The label and the text field have to be paired to identify the text field.

`<label>` requires `for` attribute to establish the association with the text field and describe the field. So, users can understand what this text field is for.

The `for` attribute share the same value with its paired `<input>`'s `id` to establish their association.

`id` is required to `<input>` for the paring.  Ensure its value is unique in the page.

Assistive technologies use this association to identify the field to the user.

## Code

### Text


### Number


### Telephone


### Email


### URL


### Password


### Date