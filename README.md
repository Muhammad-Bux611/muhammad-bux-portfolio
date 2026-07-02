# Muhammad Bux Portfolio

A modern personal portfolio website showcasing my projects, skills, and experience as a Java Backend Developer.

## Features

- Responsive portfolio website
- About, Skills, Projects, and Contact sections
- Smooth scrolling and modern UI
- Contact form with two available options:
  - Local Node.js backend (SMTP email)
  - Formspree integration (no backend required)

---

## Contact Form Setup

The contact form supports two methods.

### Option 1 — Node.js Server (Recommended)

#### Install dependencies

```bash
npm install
```

#### Create a `.env` file

```env
SMTP_HOST=smtp.example.com
SMTP_PORT=587
SMTP_SECURE=false
SMTP_USER=your-smtp-username
SMTP_PASS=your-smtp-password
TO_EMAIL=your@email.com
PORT=3000
```

#### Start the server

```bash
npm start
```

The form will submit to:

```
/api/contact
```

and emails will be sent using your SMTP server.

---

### Option 2 — Formspree

If you don't want to run a backend server:

1. Create a Formspree account.
2. Create a new form.
3. Copy your endpoint.

Example:

```
https://formspree.io/f/your-form-id
```

4. Replace the placeholder endpoint inside `portfolio.html`.

The website will first try the local `/api/contact` endpoint. If it isn't available, it will automatically fall back to Formspree.

---

## Project Structure

```
portfolio/
│
├── portfolio.html
├── style.css
├── script.js
├── package.json
├── server.js
├── api/
├── assets/
└── README.md
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/Muhammad-Bux611/Muhammad-Bux-Portfolio.git
```

Open the project:

```bash
cd Muhammad-Bux-Portfolio
```

Install dependencies:

```bash
npm install
```

Run the application:

```bash
npm start
```

---

## Technologies Used

- HTML5
- CSS3
- JavaScript
- Node.js
- Express.js
- Nodemailer
- Formspree

---

## Security

- Never commit your `.env` file.
- Keep SMTP credentials private.
- Consider enabling spam protection (reCAPTCHA) for production deployments.
- Validate user input on both the client and server.

---

## License

This project is for portfolio and educational purposes.
