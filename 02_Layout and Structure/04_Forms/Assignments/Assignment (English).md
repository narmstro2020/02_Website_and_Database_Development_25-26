# Assignment 1: Simple Login Form - Template

## Objective
Create a basic login form that collects a username and password from the user.

## Requirements

Your login form must include:

1. A form element with an id of "loginForm"
2. A username field:
   - Use appropriate input type
   - Include a label
   - Make it required
   - Add placeholder text "Enter username"
3. A password field:
   - Use appropriate input type
   - Include a label  
   - Make it required
   - Add placeholder text "Enter password"
4. A "Remember me" checkbox with a label
5. A submit button with the text "Log In"
6. A reset button with the text "Clear"
7. Proper HTML structure with DOCTYPE, html, head, title, and body
8. JavaScript to handle form submission and log the values to console

## Starting Code

```html
<!DOCTYPE html>
<html>
<head>
    <title>Login Form</title>
    <meta charset="UTF-8">
</head>
<body>
    <header>
        <h1>Welcome Back!</h1>
    </header>
    
    <main>
        <!-- Create your form here -->
        
        
        
    </main>
    
    <footer>
        <p>Don't have an account? Sign up today!</p>
    </footer>
    
    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();

            const formData = new FormData(this);

            console.log('Login form submitted:');
            for (let [key, value] of formData.entries()) {
                console.log(key + ': ' + value);
            }
        });
    </script>
</body>
</html>
```

## Hints

- Remember that password inputs should hide the text as users type
- The `for` attribute in labels should match the `id` of the input
- Use `type="checkbox"` for the remember me option
- The form needs an id to attach the JavaScript event listener
- Use `FormData` to get all form values in the JavaScript

## Expected Output

When the user fills in the form and clicks "Log In", the console should show something like:
```
Login form submitted:
username: johndoe
password: mypassword123
remember: on
```

## Submission Checklist

- [ ] Form has proper id attribute
- [ ] Username field with label
- [ ] Password field with label  
- [ ] Remember me checkbox with label
- [ ] Submit button
- [ ] Reset button
- [ ] Required attributes on username and password
- [ ] Placeholder text on both text inputs
- [ ] JavaScript prevents actual form submission
- [ ] JavaScript logs all form data to console
- [ ] Proper HTML document structure