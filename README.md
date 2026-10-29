# Password Strength Checker

A lightweight, browser-based password strength checker with a clean, minimal interface. Enter a password to see an instant strength rating, and toggle visibility when you want to inspect what you typed.

## Live Demo

**Try it here:** https://password-strength-checker-v1.vercel.app/

## Features

- **Real-time feedback** — the strength meter updates as you type.
- **Five strength levels** — Very weak, Weak, Fair, Strong, and Very strong.
- **Visual strength indicator** — a progress bar and label show the current rating.
- **Show/hide password** — toggle password visibility with the eye button.
- **Responsive layout** — works across desktop and mobile screen sizes.
- **Minimal design** — dark interface with no installation or dependencies required.

## How Strength Is Estimated

The checker uses a simple, rule-based score. It awards points for these characteristics:

- At least 8 characters
- At least 12 characters
- Both lowercase and uppercase letters
- At least one digit
- At least one special character

The resulting score maps to one of the five strength labels displayed by the interface.

> **Note:** This is a basic educational estimate, not a comprehensive security audit. It does not check passwords against breached-password databases or detect every common word, repeated pattern, or predictable sequence. A high rating does not guarantee that a password is secure.

## Getting Started

No package manager, build step, or external dependency is required.

### Run locally

1. Clone the repository:

   ```bash
   git clone https://github.com/itzyongan/password-strength-checker.git
   cd password-strength-checker
   ```

2. Open `index.html` in your browser.

   You can also start a simple local HTTP server if you prefer:

   ```bash
   python -m http.server 8000
   ```

   Then visit http://localhost:8000.

## Project Structure

```text
password-strength-checker/
└── index.html   # HTML structure, CSS styling, and JavaScript logic
```

## Built With

- **HTML5** — page structure
- **CSS3** — layout, styling, and strength-meter transitions
- **Vanilla JavaScript** — password input handling, scoring, and visibility toggle

## Privacy

The current implementation evaluates the password in the browser and contains no code that sends the entered password to a server. For sensitive use, you should still review the source code and avoid entering a real password into any tool you do not trust.

## Contributing

Suggestions and improvements are welcome:

1. Fork this repository.
2. Create a feature branch: `git checkout -b feature/your-improvement`
3. Commit your changes: `git commit -m "Add your improvement"`
4. Push the branch: `git push origin feature/your-improvement`
5. Open a pull request.

## License

No license file is currently included in this repository. Unless a license is added, the default copyright rules apply; please contact the repository owner before redistributing or reusing the code.
