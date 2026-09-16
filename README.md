# My Password Generator

A simple command-line tool written in Python that generates secure, random passwords and rates their strength.

## Features

- Generates a random password using a cryptographically secure random source (`secrets` module)
- Combines uppercase and lowercase letters, digits, and special symbols
- Guarantees every password contains at least one letter, one digit, and one symbol
- Validates user input for password length
- Rates the generated password as **Weak**, **Medium**, or **Strong** based on length and character variety

## Requirements

- Python 3.6 or higher (no external libraries needed — uses only the standard library)

## Usage

1. Save the script as `hello.py`
2. Run it from your terminal:

   python hello.py


3. Enter the desired password length when prompted (minimum 4):

   --- MY PASSWORD GENERATOR ---
   Enter password length (e.g., 8 or 12): 12

4. View your generated password and its strength rating:

   Your secure password is: xT9#mQ2!vLk8
   Status: Strong Password! (Very secure)


## How It Works

1. **Input validation** — the script loops until it receives a valid integer of at least 4.
2. **Character pools** — letters (`a-z`, `A-Z`), digits (`0-9`), and symbols (`string.punctuation`) are combined into one pool.
3. **Guaranteed variety** — one character is drawn from each of the letter, digit, and symbol pools first, then the rest of the password is filled randomly from the combined pool.
4. **Shuffling** — all characters are shuffled so the guaranteed ones aren't always in the same position.
5. **Strength check** — the script checks for lowercase, uppercase, digit, and symbol presence, then combines that with password length to rate the password as Weak, Medium, or Strong.


