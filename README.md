# Instagram Login Clone

A lightweight front-end replica of Instagram's login screen built with vanilla HTML, CSS, and JavaScript. The page gathers form input and uses EmailJS to forward submissions to a configured inbox—useful for demos that showcase client-side form handling with a third-party email service.

## Features

- **Responsive layout** that mimics Instagram's login panel across desktop and mobile widths.
- **EmailJS integration** to relay username/password fields to a designated email template.
- **Store badge links** that redirect to the real App Store and Google Play pages for Instagram.
- **Lightweight stack**: no bundlers or dependencies beyond EmailJS' CDN script.

## Project Structure

```
index.html   # Static markup and EmailJS loader
style.css    # Instagram-inspired styling
script.js    # Form handling + EmailJS submission logic
```

## Prerequisites

- EmailJS account with a service ID, template ID, and public key.
- Static HTTP server (optional) if you prefer to avoid `file://` testing quirks.

## Setup

1. Open `index.html` and replace `emailjs.init("YOUR_EMAILJS_PUBLIC_KEY")` with your EmailJS public key.
2. In `script.js`, swap the `serviceID` and `templateID` constants with the values from your EmailJS dashboard.
3. Ensure the EmailJS template expects the fields defined in `templateParams` (`from_name`, `to_name`, `message`, `reply_to`, `username`, `password`).

## Running Locally

- Double-click `index.html`, or
- Serve the folder with any static server, e.g. `npx serve .` or Python's `python -m http.server` (requires Python installed).

## Customization Tips

- Update `style.css` to tweak typography, colors, or spacing while keeping the original layout.
- Swap badge images (`fb.png`, `appstore.png`, `playstore.png`) to match your branding.
- Adjust the alert messaging in `script.js` to better guide users after submissions.

## Security & Ethics

This project is for educational demonstrations only. Never collect credentials or any sensitive information without explicit user consent. When experimenting with EmailJS or similar tooling, make sure you comply with all applicable policies, laws, and platform terms of service.
