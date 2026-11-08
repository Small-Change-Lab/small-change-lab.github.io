# Small Change Lab landing page

Static, no build step. Open `index.html` in a browser. Files: `index.html`, `styles.css`, `assets/` (copies of `creative/brand/dp.svg` and `banner.svg`).

## Signup form (Brevo)
The form in `index.html` posts to a Brevo subscription form (Marketing > Forms > "Free 30-Day Tracker"). It sends `EMAIL`, a hidden honeypot `email_address_check` (must stay empty) and `locale`. Brevo uses double opt-in, so people join the list only after clicking the confirmation email. To change the form, copy the new `action` URL from Brevo's Share step (Simple HTML tab).

After submitting, visitors see Brevo's default pages. To use pages on this site, set them in the form's Settings step (confirmation page after submitting, and after clicking the validation link).

reCAPTCHA v2 (checkbox) is enabled: the script is in the `<head>` and the `g-recaptcha` div with the site key is in the form in `index.html`. The secret key lives only in the Brevo form settings. To change keys, update both places. Google is disclosed in `privacy.html`.

## Before launch
- Verify your phone in Brevo so confirmation emails can send.
- Add the tracker link to the confirmation email or a confirmation page.
- Review `privacy.html` against the laws that apply to you; it is a generic template, not legal advice.
- Pillar and series copy is paraphrased from `creative/channel-identity.md`.
