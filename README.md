# My Password Generator

A simple command-line tool written in Python that generates random passwords and rates their strength based on length.

## Features

- Generates a random password using Python's built-in `random` module
- Combines uppercase and lowercase letters with digits
- Guarantees every password contains at least one letter and one digit
- Validates user input for password length
- Rates the generated password as **Weak**, **Medium**, or **Strong** based on length

## Requirements

- Python 3.6 or higher (no external libraries needed — uses only the standard library)

## Usage

1. Save the script as `password_generator.py`
2. Run it from your terminal:

   python password_generator.py

3. Enter the desired password length when prompted (minimum 4):

   --- Password Generator ---
   Enter password length (min 4): 12

4. View your generated password and its strength rating:

   Your password: aB3kLp9xTqR2
   Status: Strong

## How It Works

1. **Input validation** — the script loops until it receives a valid integer of at least 4.
2. **Character pool** — letters (`a-z`, `A-Z`) and digits (`0-9`) are combined into one pool.
3. **Guaranteed variety** — one character is drawn from the letters and one from the digits first, then the rest of the password is filled randomly from the combined pool.
4. **Shuffling** — all characters are shuffled using `random.SystemRandom()` so the guaranteed ones aren't always in the same position.
5. **Strength check** — the script rates the password as Weak (under 8 characters), Medium (8–11 characters), or Strong (12 or more characters) based purely on length.

## Notes

This version doesn't include symbols and rates strength by length alone. For stronger, production-grade passwords, consider adding symbol support and switching from `random` to Python's `secrets` module.



