# MSM Sports

> **Football Career Mentorship** — Building careers across borders.
>
> [![Live Site](https://img.shields.io/badge/Live%20Site-msmsports.site-c8a55c?style=flat-square)](https://msmsports.site)
> [![Status](https://img.shields.io/badge/Status-Accepting%20New%20Players-5cb85c?style=flat-square)](#contact)
>
> ---
>
> ## Overview
>
> MSM Sports is a UK-based football career mentorship agency. This repository contains the source code for the [msmsports.site](https://msmsports.site) website — a single-page application that presents the agency's services, markets, and contact form.
>
> The site is designed to be clean, dark-themed, and professional, targeting ambitious football players looking for cross-border career opportunities across Scandinavia, the UK, and Europe.
>
> ---
>
> ## Tech Stack
>
> - **Frontend:** Vanilla HTML, CSS, JavaScript (single `index.html`)
> - - **Backend / API:** Node.js serverless function (`/api/contact.js`) via Vercel
>   - - **Email:** [Nodemailer](https://nodemailer.com/) with SMTP
>     - - **Fonts:** Cormorant Garamond (serif) + Outfit (sans-serif) via Google Fonts
>       - - **Hosting:** Vercel (Production deployments)
>        
>         - ---
>
> ## Project Structure
>
> ```
> msmsports/
> ├── index.html       # Main single-page application
> ├── favicon.svg      # Site icon (MSM monogram)
> ├── package.json     # Node.js dependencies
> └── api/
>     └── contact.js   # Serverless function — contact form email handler
> ```
>
> ---
>
> ## Pages
>
> The site uses client-side JS to switch between sections (no page reloads):
>
> | Page | Description |
> |------|-------------|
> | **Home** | Hero banner, key stats, and "What Sets Us Apart" feature cards |
> | **About Us** | Agency background, values, and founder quote |
> | **Services** | Six core services and a 4-step process overview |
> | **Markets** | 10 active football markets across Europe and Scandinavia |
> | **Contact** | Contact details and an email contact form |
>
> ---
>
> ## API — Contact Form
>
> **`POST /api/contact`**
>
> Handles contact form submissions and sends an email via SMTP using Nodemailer.
>
> **Request body (JSON):**
>
> ```json
> {
>   "name": "string",
>   "email": "string",
>   "country": "string",
>   "level": "string",
>   "message": "string"
> }
> ```
>
> **Responses:**
>
> - `200 OK` — `{ "success": true }`
> - - `405 Method Not Allowed` — non-POST requests
>   - - `500 Internal Server Error` — email send failure
>    
>     - ---
>
> ## Environment Variables
>
> To run the contact form API locally or in production, set the following environment variables:
>
> | Variable | Description |
> |----------|-------------|
> | `SMTP_HOST` | SMTP server hostname |
> | `SMTP_PORT` | SMTP server port (e.g. `587`) |
> | `SMTP_USER` | SMTP authentication username |
> | `SMTP_PASS` | SMTP authentication password |
> | `SMTP_FROM` | Sender email address |
> | `CONTACT_TO` | Recipient email address for form submissions |
>
> ---
>
> ## Local Development
>
> ```bash
> # Install dependencies
> npm install
>
> # Run locally with Vercel CLI
> npx vercel dev
> ```
>
> The site is static (single HTML file), so `index.html` can also be opened directly in a browser for frontend-only development. The `/api/contact` endpoint requires the Vercel CLI or a deployed environment to function.
>
> ---
>
> ## Deployment
>
> The site is deployed on **Vercel**. Pushes to the `main` branch trigger automatic production deployments.
>
> 16+ deployments have been made to production. The live site is available at [msmsports.site](https://msmsports.site).
>
> ---
>
> ## Markets Covered
>
> Norway · England · Ireland · Sweden · Denmark · Finland · Iceland · Scotland · Spain · Italy
>
> ---
>
> ## Contact
>
> 📧 [hello@msmsports.site](mailto:hello@msmsports.site)
> 🌐 [msmsports.site](https://msmsports.site)
>
> ---
>
> © 2026 MSM Sports
