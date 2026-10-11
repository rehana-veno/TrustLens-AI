# TrustLens AI — Detection Lab

TrustLens AI is a browser-based student hackathon prototype that helps users double-check suspicious screenshots and message text. It looks for common warning patterns and explains what deserves a closer look.

## Run locally
Open `index.html` in a modern browser with an internet connection, or publish this folder using GitHub Pages. Tesseract.js and English OCR data are loaded from a CDN. The first image analysis may take longer while the OCR engine/data downloads.

## Prototype features
- Mysterious welcome gate with demo sign-up, demo login, and guest access.
- Image upload and preview (PNG, JPG, WEBP, BMP; 8 MB max).
- Fast OCR strategy: one main pass and at most one contrast-enhanced retry.
- Pasted-text checker, fictional demo sample, warning-signal explanations, and copyable result summary.
- Recent scan summaries stored in local browser storage; raw images and scanned message text are not stored by TrustLens.
- Mobile/tablet responsive layout.

## Authentication limitation
Sign-up/login are front-end demo flows only. They do not create or verify secure accounts, and passwords are never stored. Do not enter a real password. Production authentication and secure accounts require a backend.

## AI/OCR limitation
This version uses OCR plus explainable keyword/rule matching. It is **not a trained image classifier** and does not prove whether an image or message is genuine or fraudulent. Its score is a weighted warning-signal score, not a probability of fraud. A clean result does not mean a message is safe. Verify requests independently with official contact information.

## Privacy note
Image processing runs in the browser, and this prototype has no TrustLens image-upload server. The OCR library/language data are downloaded from a CDN. Avoid uploading private documents or sensitive personal information.

## Built with
HTML, CSS, JavaScript, Tesseract.js OCR.
