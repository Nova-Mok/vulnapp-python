# vulnapp-python
Intentional Vulnerable Python Application - Used only for tests in AquilaX

This application includes the following vulnerabilities:

- SQL Injection: The /add_post route is vulnerable to SQL injection because it directly inserts user input into an SQL query without proper sanitization.

- XSS (Cross-Site Scripting): The /view_post/<int:id> route is vulnerable to XSS because it doesn't properly escape or sanitize user input before rendering it in the HTML template.

- Hardcoded Password: The application contains hardcoded admin credentials (ADMIN_USERNAME and ADMIN_PASSWORD), which is a security risk.

- Path Traversal: The application does not properly sanitize input in the /exec_command route, allowing an attacker to execute arbitrary commands on the server.

- Code Injection: The /exec_command route is vulnerable to code injection because it executes user-supplied input as a command without proper validation.

- XSRF (Cross-Site Request Forgery): Although not explicitly implemented, the application lacks protection against XSRF attacks, which could allow an attacker to execute unauthorized actions on behalf of a logged-in user.

Please use caution when running and testing this code, and be aware of the potential security risks involved.