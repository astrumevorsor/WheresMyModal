To demonstrate a basic XSS attack, we will create a simple form that takes user input and displays it on the page without proper sanitization. This will allow us to inject a script tag into the input field, which will then be executed by the browser. We will use the 'sanitize-html' library to demonstrate how to prevent such attacks by sanitizing the user input before displaying it. The steps are as follows:
1. Create a state variable to store the user input.
2. Create an input field that updates the state variable on change.
3. Create a button that, when clicked, displays the user input on the page.
4. Initially, display the input without sanitization to demonstrate the XSS vulnerability.
5. Then, add the 'sanitize-html' library to sanitize the input and show how it prevents the attack.
