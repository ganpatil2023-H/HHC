# HomeHealth AI Login Page

A responsive, Netlify-ready login page for a Home Health Coding & OASIS AI platform.

## Run locally
Open `index.html` in a browser.

## Deploy to Netlify
1. Create a new GitHub repository.
2. Upload `index.html`, `styles.css`, and `script.js`.
3. In Netlify, choose "Add new site" → "Import an existing project".
4. Select the GitHub repository.
5. Build command: leave blank.
6. Publish directory: `/`
7. Deploy.

## Important
This project currently performs client-side form validation and is a UI/MVP login page.
It does NOT authenticate users against a real database.

For production healthcare use, connect the form to a secure authentication provider/backend and implement appropriate access control, MFA, audit logging, encryption, session management, and HIPAA/security requirements before handling PHI.
