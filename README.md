<<<<<<< HEAD

=======
# Contact form — local server and Formspree fallback

This repository includes two ways to make the contact form on `portfolio.html` work:

- Run the included Node server (`/api/contact`) which sends email using SMTP (recommended if you want full control).
- Use Formspree by setting the form `data-formspree` attribute to your Formspree endpoint (no server needed).

## Option A — Run the included Node server

1. Install dependencies:

```bash
npm install
```

2. Create a `.env` file in the repository root with these variables:

```env
SMTP_HOST=smtp.example.com
SMTP_PORT=587
SMTP_SECURE=false # true if using SMTPS (465)
SMTP_USER=your-smtp-username
SMTP_PASS=your-smtp-password
TO_EMAIL=your@inbox.example.com
PORT=3000
```

3. Start the server:

```bash
npm start
```

4. Open `portfolio.html` in your browser (or host it). The form posts to `/api/contact` and the server will send the email.

## Option B — Use Formspree (no server)

1. Create a form endpoint at https://formspree.io and copy the endpoint ID (example: `https://formspree.io/f/abcdxyz`).
2. In `portfolio.html` set the `data-formspree` attribute on the form to your endpoint (it is already present as a placeholder).

The page will attempt the local `/api/contact` endpoint first; if that fails and you provided a valid Formspree endpoint it will try Formspree automatically.

## Security notes

- Keep SMTP credentials secret. Do not commit `.env` to source control.
- Consider rate-limiting, spam protection (reCAPTCHA), and server-side validation in production.
>>>>>>> 1e48a9e (initial commit)
