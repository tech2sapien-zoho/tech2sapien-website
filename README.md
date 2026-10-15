# Tech2Sapien Website — Beginner Guide

This folder contains a responsive, static website for Tech2Sapien.

## 1. What is in this folder?

- `index.html` — the content and structure of the website.
- `style.css` — the visual design and responsive layout for desktop, laptop, tablet and mobile.
- `script.js` — small interactive behaviours, including the mobile navigation menu.
- `assets/` — images, your company logo and the browser tab icon (`favicon.svg`).
- `README.md` — these instructions.

You do not need to understand the code before following the steps below.

## 2. First: download and extract

1. Download `tech2sapien-website-starter.zip`.
2. In Windows File Explorer, find the ZIP file (usually in Downloads).
3. Right-click it and choose **Extract All**.
4. Click **Extract**.
5. Open the extracted `tech2sapien-website` folder.
6. Confirm that `index.html`, `style.css`, `script.js`, and this `README.md` are visible. Keep the `assets` folder too.

Do not upload the ZIP file itself to GitHub. Upload the files and the `assets` folder inside it.

## 3. Preview on your computer (optional but useful)

1. Open the extracted folder.
2. Double-click `index.html`.
3. Your browser should open the website.
4. Make the browser window wide, then narrow it to check how the layout adapts.

Note: the local preview can show the layout, but the enquiry form needs to be published and activated before you can rely on email delivery.

## 4. Create your GitHub repository

1. Sign in at https://github.com/.
2. Visit https://github.com/new.
3. Repository name: `tech2sapien-website`.
4. Choose **Public** for the simplest GitHub Free Pages setup.
5. Click **Create repository**.

If a repository with this name already exists in your account, open it instead of creating another one.

## 5. Upload the website files to GitHub

1. Open your `tech2sapien-website` repository.
2. Click **Add file** → **Upload files**.
3. Open the extracted folder on your computer.
4. Select the files inside the folder: `index.html`, `style.css`, `script.js`, `README.md`, and the `assets` folder.
5. Drag them into the GitHub upload area. Make sure `assets/` and its files are included.
6. Scroll down to **Commit changes**.
7. Enter a short message such as `Add Tech2Sapien website`.
8. Click **Commit changes**.

Important: `index.html` must be in the top level of the repository. It must not be inside a second nested `tech2sapien-website` folder.

## 6. Publish using GitHub Pages

1. In the repository, click **Settings**.
2. In the left menu, choose **Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select branch `main`.
5. Select folder `/(root)`.
6. Click **Save**.
7. Wait a few minutes, then refresh the Pages settings page.
8. Open the website URL GitHub shows you. It usually looks like `https://YOUR-USERNAME.github.io/tech2sapien-website/`.

Replace `YOUR-USERNAME` with your GitHub username. If you see a 404 page, wait a little, confirm `index.html` is at the repository root, and check the Pages settings.

## 7. Connect the Hostinger domain

Do this only after the GitHub Pages URL is working.

### A. Set the custom domain in GitHub

1. Open repository **Settings** → **Pages**.
2. Under **Custom domain**, enter `tech2sapien.com`.
3. Click **Save**.

### B. Add DNS records in Hostinger

1. Sign in to https://hpanel.hostinger.com/.
2. Open **Domains** and select `tech2sapien.com`.
3. Open **DNS / Nameservers** or **DNS records** (the exact label can vary).
4. Before changing anything, take a screenshot of the current DNS records.
5. Check for existing conflicting `A`, `AAAA` or `CNAME` records for `@` and `www`.
6. Add the four GitHub Pages `A` records for the root domain:

   - Type `A`, Name `@`, Value `185.199.108.153`
   - Type `A`, Name `@`, Value `185.199.109.153`
   - Type `A`, Name `@`, Value `185.199.110.153`
   - Type `A`, Name `@`, Value `185.199.111.153`

7. Add the `www` CNAME:

   - Type `CNAME`, Name `www`, Value `YOUR-USERNAME.github.io`

   Replace `YOUR-USERNAME` with your actual GitHub username. Do not add the repository name to this CNAME target.

8. Save the records. DNS updates can take time, sometimes up to 24 hours.
9. Do not delete MX or mail-related TXT records. They may be needed for business email. If your domain uses custom nameservers, update DNS at the provider that manages those nameservers.

### C. Enable HTTPS

1. Return to GitHub **Settings** → **Pages**.
2. Wait until GitHub verifies the domain and prepares the certificate.
3. Turn on **Enforce HTTPS** when that option becomes available.

## 8. Contact form email setup

The form is set up to send enquiries to `tech2sapien@gmail.com` using FormSubmit, a third-party form relay.

1. Publish the site first.
2. Open the live website and submit a test enquiry using an email address you can access.
3. Check `tech2sapien@gmail.com` for a FormSubmit activation email.
4. Click the activation link.
5. Submit another test enquiry and confirm the email arrives. Check Spam/Junk if needed.

Until the recipient is activated and a successful test is received, do not assume the form is sending leads correctly. Review FormSubmit's privacy and retention terms before launch. Never ask visitors to submit passwords or sensitive information through this form.

## 9. Add your company logo

The logo is not included yet because it has not been uploaded in this chat.

1. Upload the logo image in the ChatGPT conversation.
2. We can prepare a web-ready copy named `logo.png` or `logo.svg`.
3. Put it inside `assets/`.
4. Then update the header, footer and browser icon to use the real logo.

Do not rename your logo to `favicon.svg` unless the file really is SVG content.

## 10. How to update the website later

For a small text change:
1. Open `index.html` in a text editor such as Notepad or Visual Studio Code.
2. Edit the text carefully and save the file.
3. Upload the changed file to the same GitHub repository, or edit it directly in GitHub.
4. Commit the change.
5. GitHub Pages automatically republishes the site after the update.

For design changes, edit `style.css`. For interactive behaviour, edit `script.js`.

## 11. Before launch checklist

- [ ] Company logo added and displayed correctly.
- [ ] Website checked at desktop, laptop, tablet and mobile widths.
- [ ] Company phone, email, office address and social links verified.
- [ ] Services and platform claims reviewed for accuracy.
- [ ] Contact form activated and tested end to end.
- [ ] Custom domain opens successfully.
- [ ] HTTPS works.
- [ ] Privacy notice is available before collecting enquiries at scale.

## Helpful official links

- GitHub: https://github.com/
- Create repository: https://github.com/new
- GitHub Pages guide: https://docs.github.com/en/pages/quickstart
- Hostinger: https://hpanel.hostinger.com/


### Company logo
The supplied transparent Tech2Sapien symbol is saved as `assets/tech2sapien-logo.png` and used in the header. Keep this image in the `assets` folder when uploading the website to GitHub.
