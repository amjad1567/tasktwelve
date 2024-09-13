# Registration Form

This repository contains a simple, responsive registration form created using HTML, CSS, and JavaScript. The form includes validation for password matching and is designed to be mobile-friendly.

## Files

- `index.html`: The main HTML file containing the registration form.
- `submit.html`: A simple confirmation page that displays a message after form submission.
- `style.css`: External CSS file used for styling and making the form responsive.
- `script.js`: External JavaScript file used to validate password matching before form submission.

## Features

### 1. **HTML Form (index.html)**

The `index.html` page includes a form with the following fields:

- First Name
- Last Name
- Email ID
- Phone Number
- Password
- Confirm Password
- A Submit button

When the user submits the form, the data is sent to `submit.html` using the GET method, where the user is informed that they have been registered.

### 2. **Form Submission (submit.html)**

The `submit.html` file displays the following message:

You've been registered. Please check your email for details.

This is the page where the form redirects upon successful submission.

### 3. **Styling (style.css)**

The `style.css` file is responsible for:

- Making the form responsive and centered on the page using Flexbox.
- Styling input fields and buttons for a clean and modern look.
- Adjusting layout and font size for smaller screens using media queries.

Key Features:
- **Responsive**: The form adjusts to different screen sizes using CSS media queries.
- **Centered Layout**: Flexbox is used to center the form on the page.
- **Styled Inputs and Buttons**: Input fields and buttons are styled to be user-friendly and visually appealing.

### 4. **Password Validation (script.js)**

The `script.js` file includes a function that checks whether the password and confirm password fields match before allowing the form to be submitted. If the passwords do not match, an alert is shown, and the form submission is blocked.

#### Example of the JavaScript function:

```javascript
function checkPassword() {
    var password = document.getElementById("password").value;
    var confirmPassword = document.getElementById("confirmPassword").value;

    if (password !== confirmPassword) {
        alert("Passwords do not match!");
        return false;
    }
    return true;
}  


5. How to Run
Clone this repository to your local machine.
Open index.html in a web browser or use the Live Server feature in VSCodium to run it locally.
Fill out the form and click Submit.
If the passwords match, you'll be redirected to submit.html. If they do not match, you'll see an error message.
6. How to Move CSS and JavaScript to External Files
CSS: The CSS was initially inside the index.html file but was moved to a separate style.css file. This was done by:

Creating a style.css file.
Moving all the CSS code from the <style> tag in index.html to style.css.
Linking the CSS file in the <head> section of index.html using:

<link rel="stylesheet" href="style.css">

JavaScript: Similarly, the JavaScript was initially written inside the HTML page but was moved to script.js by:

Creating a script.js file.
Moving the JavaScript function from the <script> tag in index.html to script.js.
Linking the external JS file just before the closing </body> tag using:


<script src="script.js"></script>


