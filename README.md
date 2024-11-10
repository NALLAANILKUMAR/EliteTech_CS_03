
Password Complexity Checker
# Password Complexity Checker 🔐

A simple Python tool that assesses the strength of a password based on multiple criteria, such as length, presence of uppercase and lowercase letters, numbers, and special characters. This tool provides feedback on the password's strength level, helping users create more secure passwords.

## Features

- **Password Strength Levels**:
  - **Very Weak**: Fails most criteria
  - **Weak**: Meets at least two criteria
  - **Moderate**: Meets at least three criteria
  - **Strong**: Meets at least four criteria
  - **Very Strong**: Meets all five criteria

- **Feedback**:
  - Detailed guidance on improving password strength.

## Criteria for Password Strength

1. **Length**: Minimum of 8 characters.
2. **Uppercase Letters**: At least one uppercase letter.
3. **Lowercase Letters**: At least one lowercase letter.
4. **Numbers**: At least one digit.
5. **Special Characters**: At least one special character (e.g., `!@#$%^&*()`).

## Installation

To use this tool, you’ll need to have Python installed. You can download Python from [python.org](https://www.python.org/downloads/).

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/password-complexity-checker.git
    ```

2. Navigate to the project directory:
    ```bash
    cd password-complexity-checker
    ```

## Usage

1. Run the `password_checker.py` file:
    ```bash
    python password_checker.py
    ```

2. Enter the password you’d like to check when prompted. Example:

    ```plaintext
    Enter a password to check: Password1!
    Password Strength: Very Strong
    ```

3. If the password is weak, you’ll receive suggestions for improvement:

    ```plaintext
    Enter a password to check: pass123
    Password Strength: Weak
    - Password should be at least 8 characters long.
    - Password should include at least one uppercase letter.
    - Password should include at least one special character.
    ```

## Code Explanation

The `check_password_strength` function evaluates password complexity by using Python's `re` (regular expressions) module to:
- Verify length (>= 8 characters)
- Check for uppercase and lowercase letters
- Check for digits and special characters

The tool returns a **strength level** and **feedback** on missing criteria, if applicable.

## Example

For a quick demonstration, see below:

```python
password = "Password1!"
strength, feedback = check_password_strength(password)
print(f"Password Strength: {strength}")
for comment in feedback:
    print(f"- {comment}")
