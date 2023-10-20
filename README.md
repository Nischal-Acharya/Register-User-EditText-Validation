# User Registration with EditText Validation (Kotlin)

This is a simple Android application that demonstrates user registration with EditText validation in Kotlin.

## Features

- Register a user with a full name, email, password, and password confirmation.
- Validate the input fields for:
  - Empty fields
  - Matching passwords
  - Valid email format
  - Strong password criteria (at least 8 characters, uppercase, lowercase, numbers, special characters)

## Getting Started

To use this code in your Android project, follow these steps:

1. Clone this repository to your local machine.
2. Open the project in Android Studio.
3. Customize the layout, colors, and error messages to match your application's design and requirements.
4. Implement the registration logic for your app, such as sending data to a server and creating user accounts.

## Usage

You can use this code as a starting point for building registration functionality in your Android app. Customize it and integrate it into your project as needed.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- This code is a basic example and should be extended and customized for a production application.

---
   val fullname = fullnameid.text.toString()
    val email = emailid.text.toString()
    val password = passwordid.text.toString()
    val repassword = repasswordid.text.toString()

    if (fullname == "" || email == "" || password == "" || repassword == "") {
        errmsg.setTextColor(forgotpassred)
        errmsg.text = "Please fill all the fields!"
    } else if (password != repassword) {
        errmsg.setTextColor(forgotpassred)
        errmsg.text = "Confirm password is not valid!"
    } else {
        val emailPattern = "[a-zA-Z0-9._-]+@[a-z]+\\.+[a-z]+"
        val passwordPattern = "^(?=.*[A-Za-z])(?=.*\\d)(?=.*[\$@\$!%*?&])[A-Za-z\\d\$@\$!%*?&]{8,}$"

        if (!email.matches(emailPattern.toRegex())) {
            errmsg.setTextColor(forgotpassred)
            errmsg.text = "Invalid email address"
        } else if (!password.matches(passwordPattern.toRegex())) {
            errmsg.setTextColor(forgotpassred)
            errmsg.text = "Password must contain at least 8 characters, including a mix of uppercase, lowercase letters, numbers, and special characters."
        } else {
            // Email and password are valid, continue with your registration logic
            // For example, send the registration data to your server, create an account, etc.
        }
    }
}
'''
Feel free to fork this repository and adapt the code for your specific needs.

For questions or support, please contact [Your Name](mailto:nismsg1@gmail.com).
