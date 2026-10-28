# ExpiryLens website

Minimal static website for ExpiryLens.

## Files
- `index.html`
- `privacy.html`
- `support.html`
- `styles.css`

## 1. Change the public developer name

Open:

`privacy.html`

Search for:

`[DEVELOPER NAME]`

Replace it with the exact developer name you want shown publicly.

Example:

`George Wang`

Use the same public developer name in your store listings where appropriate.

---

## 2. Change the logo

Right now the website uses the text logo:

`ExpiryLens`

In each HTML file, the top navigation contains:

```html
<a class="logo" href="index.html">ExpiryLens</a>
```

If you want to use an image logo later:

1. Put your logo image in the website folder, for example:
   `logo.png`

2. Replace the line above with:

```html
<a class="logo" href="index.html">
  <img src="logo.png" alt="ExpiryLens">
</a>
```

3. Add this to `styles.css`:

```css
.logo img {
  height: 28px;
  width: auto;
  display: block;
}
```

Do the same replacement in:
- `index.html`
- `privacy.html`
- `support.html`

---

## 3. Create the Formspree endpoint

The support form is visually built directly into `support.html`.

GitHub Pages cannot receive form submissions by itself, so Formspree handles the submission in the background.

Steps:

1. Go to Formspree.
2. Create an account.
3. Create a new form/project.
4. Give it a name such as:
   `ExpiryLens Support`
5. Formspree gives you an endpoint similar to:

   `https://formspree.io/f/abcdwxyz`

6. Open:

   `support.html`

7. Find:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

8. Replace it with the complete endpoint Formspree gives you.

Example:

```html
<form action="https://formspree.io/f/abcdwxyz" method="POST">
```

That is the only Formspree line you need to change.

---

## 4. Change the app/site name

The site currently uses:

`ExpiryLens`

If you rename the app later, search all files for:

`ExpiryLens`

and replace it with the final name.

The main places are:
- page titles
- top-left logo text
- homepage copy
- privacy policy
- support page
- footer

---

## 5. Publish with GitHub Pages

1. Create a GitHub repository, for example:
   `expirylens-site`
2. Upload these files to the repository root.
3. Open GitHub:
   `Repository → Settings → Pages`
4. Under Build and deployment choose:
   `Deploy from a branch`
5. Choose:
   `main`
6. Choose:
   `/(root)`
7. Save.

Your public pages will then be similar to:

- Home:
  `https://YOUR_USERNAME.github.io/expirylens-site/`
- Privacy:
  `https://YOUR_USERNAME.github.io/expirylens-site/privacy.html`
- Support:
  `https://YOUR_USERNAME.github.io/expirylens-site/support.html`

Use the privacy URL in:
- App Store Connect
- Google Play Console
- iOS app
- Android app
