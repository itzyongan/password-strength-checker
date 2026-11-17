# Password Strength Checker

A simple, responsive, browser-based tool that evaluates password strength and displays an estimated time it could take to crack a password.

**Live Demo:** https://password-strength-checker-v1.vercel.app/

## Features

- **Instant strength feedback** — Updates as you type.
- **Five strength levels** — Very weak, Weak, Fair, Strong, and Very strong.
- **Visual strength indicator** — Color-coded progress bar and status label.
- **Show/hide password** — Toggle password visibility while typing.
- **Estimated cracking time** — Displays a rough estimate based on password length and character types.
- **Lightweight and dependency-free** — Built with plain HTML, CSS, and JavaScript.

## How Strength Is Evaluated

The checker awards one point for each condition met:

| Condition | Point |
|---|---:|
| At least 8 characters | 1 |
| At least 12 characters | 1 |
| Contains lowercase and uppercase letters | 1 |
| Contains at least one number | 1 |
| Contains at least one special character | 1 |

The total score maps to the following levels:

| Score | Strength |
|---:|---|
| 1 | Very weak |
| 2 | Weak |
| 3 | Fair |
| 4 | Strong |
| 5 | Very strong |

An empty input has no strength rating. A non-empty password that meets none of the conditions is assigned the lowest level.

## Estimated Cracking Time

The displayed estimate uses a simplified calculation:

1. Builds an assumed character pool based on the character types present:
   - Lowercase letters: 26 characters
   - Uppercase letters: 26 characters
   - Digits: 10 characters
   - Special characters: 33 characters
2. Estimates the number of guesses as half of the possible combinations:

   `pool size ^ password length / 2`

3. Divides the estimated guesses by an assumed rate of 10 billion guesses per second.
4. Displays the result as a readable duration.

**Important:** This is an illustrative estimate, not a security guarantee. Actual cracking time depends on password hashing algorithms, hardware, attack methods, rate limits, and password predictability. The estimate does not account for dictionary attacks, common passwords, or compromised credentials.

## Technologies

- **HTML5** — Page structure and password input.
- **CSS3** — Layout, styling, responsive sizing, and strength indicator.
- **Vanilla JavaScript** — Password evaluation, visibility toggle, and cracking-time estimation.
- **Vercel** — Application deployment.

## Getting Started

No build step or package installation is required.

### 1. Clone the repository

```bash
git clone https://github.com/itzyongan/password-strength-checker.git
```

### 2. Navigate to the project directory

```bash
cd password-strength-checker
```

### 3. Run the application

Open `index.html` directly in your browser.

Alternatively, start a local development server:

```bash
python -m http.server 8000
```

Visit:

```text
http://localhost:8000
```

## Project Structure

```text
password-strength-checker/
├── index.html   # Application markup, styles, and JavaScript
└── README.md    # Project documentation
```

## Deployment

This project is a static website and can be deployed using Vercel or any static hosting provider.

### Deploy with Vercel

1. Import the GitHub repository into Vercel.
2. Configure the project as a static website.
3. No build command is required.
4. Deploy the project.

## Privacy

Password-strength checks and cracking-time calculations are performed locally in the browser using JavaScript. The application code does not send entered passwords to a backend or API.

The page does load font files from an external font host.

For sensitive accounts, use a trusted password manager to generate and store unique passwords. Do not treat a strength score or cracking-time estimate as proof that a password is secure.

## Contributing

Contributions and suggestions are welcome!

1. Fork this repository.
2. Create a feature branch.
3. Make and test your changes.
4. Submit a pull request describing your improvements.

## License

No license is currently specified in this repository. Unless a license is added, the code should not be assumed to be available for unrestricted reuse.
