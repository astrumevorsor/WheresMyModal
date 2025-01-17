# XSS attacks
[Read about XSS attacks here](https://owasp.org/www-community/attacks/xss/)

This project demonstrates various types of Cross-Site Scripting (XSS) vulnerabilities using Node.js and Express. **Please note:** This is for educational purposes only. Never deploy such vulnerable code to a production environment.

## Overview

- **Reflected XSS**: Shows how user input can be reflected back to the user, potentially executing scripts.
- **Stored XSS**: Illustrates how stored user input can lead to persistent XSS vulnerabilities.
- **DOM-based XSS**: Demonstrates vulnerabilities where the DOM is manipulated based on user-controlled input.

## Setup

1. **Prerequisites**:
   - Node.js installed on your system.
   - Express installed (`npm install express`).

2. **Installation**:
   - Clone this repository or download the files (`app.js`, `views/index.html`):
     ```sh
     git clone [your-repo-url]
     cd xss-demo
     npm install
     ```

3. **Running the Demo**:
   - Run the Express application:
     ```sh
     node app.js
     ```
   - Navigate to `http://localhost:3000` in your browser.

## Usage

### Reflected XSS
- Enter `<script>alert('XSS');</script>` into the input field and submit. 
- Note: By default, this is sanitized to prevent script execution. Adjust the code to see the vulnerability.

### Stored XSS (Simulated)
- This demo simulates storing data in an array, which is then displayed. Adjust the code to see vulnerabilities without sanitization.

### DOM-based XSS
- Modify the URL in your browser to include `?userInput=<script>alert('DOM XSS');</script>`. 
- The script will execute because it's directly inserted into the DOM without sanitization in the JavaScript code.

## Files

- **app.js**: The Express server handling server-side logic.
- **views/index.html**: The HTML template with embedded JavaScript for client-side interaction.

## Important Notes

- **Security**: This code is intentionally insecure to demonstrate vulnerabilities. **Do not use this in any real-world application without implementing proper security measures.**
- **Sanitization**: Always sanitize user inputs before outputting them or using them in scripts.
- **Education**: This demo should be used to learn about security vulnerabilities, not to exploit them.

## Prevention

- **Input Validation**: Only accept expected input formats.
- **Output Encoding**: Use Node.js/Express methods or libraries to escape special characters.
- **Content Security Policy**: Implement CSP to control which scripts can be executed.
- **Regular Security Audits**: Check your code regularly for vulnerabilities.

## License

This project is open-sourced under the [MIT License](LICENSE).

## Contact

If you have questions or suggestions, feel free to reach out:

- [Your Email]
- [Your GitHub Profile]

---
