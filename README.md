# Dao Journey Privacy Policy site

This folder is a small, standalone GitHub Pages site for the Dao Journey (道友日记) iOS app. It contains a bilingual privacy policy in `index.html` and does not require a build step.

## Before you publish

1. Open `index.html` and replace **`[ADD A PUBLIC SUPPORT EMAIL BEFORE PUBLISHING]`** in both language sections with an email address where users can send privacy questions and requests.
2. Review the policy against the exact app build and service-provider settings you are releasing. In particular, confirm the app's speech-recognition behavior and OpenAI API data controls. The policy describes the current source code: entries and media are saved on the device; submitted text and selected images are sent to the backend for analysis; voice recordings can be sent for server transcription when needed; the backend forwards relevant content to OpenAI and does not write request content to an app database.
3. Commit this folder's **contents** (`index.html` and `README.md`) to the root of a new GitHub repository. For example, create a repository named `dao-journey-privacy` and upload these two files directly, rather than uploading the enclosing folder as a nested directory.

## Publish with GitHub Pages

1. In the new GitHub repository, open **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch **`main`** and folder **`/(root)`**, then click **Save**.
4. Wait for GitHub Pages to finish publishing. The project site URL will normally be `https://YOUR-GITHUB-USERNAME.github.io/dao-journey-privacy/`.
5. Open the URL in a private/incognito browser window and confirm that the page loads in both English and Chinese and that the contact address is correct.
6. In App Store Connect, open **App Privacy → Privacy Policy → Edit**, paste the public HTTPS page URL, and save.

GitHub Pages sites are public. Do not add API keys, private user records, or other secrets to this repository. Apple also requires accurate App Privacy answers in App Store Connect; publishing this page does not complete those disclosures.

## Details reflected in this draft

- Journal entries, generated reflections, progress, preferences, selected images, and saved audio are stored locally in the app.
- There is no sign-in account or cloud journal sync in the current app.
- When an entry is submitted for analysis, its text and selected images go to the DigitalOcean-hosted backend and are forwarded to the OpenAI API.
- Speech recognition uses Apple's Speech framework when available. If the app needs server transcription, the recording is sent to the backend and forwarded to OpenAI. Voice audio is also kept in the app's local journal when the entry is saved.
- The backend source has no database write for request content. This statement does not describe provider-side operational logs or provider retention; those are governed by the linked providers' current terms and policies.

This is a product-specific draft, not legal advice. Keep it current when the app, backend, or providers change.
