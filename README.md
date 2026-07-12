# Gemma Chatbot

A simple static HTML chatbot that uses the Hugging Face Inference API to chat with supported instruction models such as Gemma.

## Features

- Single-page chatbot built with HTML, CSS, and JavaScript
- Hugging Face access token input
- Model dropdown for supported providers
- Markdown rendering for assistant responses
- Works as a static website on GitHub Pages or Hugging Face Spaces

## Current Models

- `google/gemma-2-2b-it:featherless-ai`
- `google/gemma-4-31B-it:cerebras`

Note: Some Hugging Face models only work when a provider is available and enabled for your account. If a model shows an error like “not supported by any provider you have enabled,” choose a provider-supported model from the dropdown.

## How to Use

1. Open `index.html` in your browser.
2. Paste your Hugging Face access token in the token field.
3. Select a model.
4. Type your message and send it.

## Hugging Face Token

Create a token from your Hugging Face account settings:

1. Go to Hugging Face.
2. Open Settings.
3. Go to Access Tokens.
4. Create a token with inference access.
5. Paste it into the chatbot page.

Do not hardcode your token inside the HTML file if you publish this project publicly.

## Deploy on GitHub Pages

1. Push this project to GitHub.
2. Open the repository on GitHub.
3. Go to Settings.
4. Open Pages.
5. Select:
   - Source: Deploy from a branch
   - Branch: `main`
   - Folder: `/root`
6. Save the settings.

Your site will be available at:

```text
https://YOUR_USERNAME.github.io/YOUR_REPOSITORY_NAME/
```

## Deploy on Hugging Face Spaces

You can also host this as a static Hugging Face Space.

For a static Space, keep the main page as:

```text
index.html
```

Then create the Space using the Static HTML SDK.

## Common Errors

### Permission denied when pushing to GitHub

If Git says permission is denied to another GitHub username, your laptop is logged in with the wrong GitHub account. Log out from Git Credential Manager and sign in again with the correct GitHub account.

### Could not resolve host: github.com

This is usually a network or DNS issue. Check your internet connection, VPN, DNS, or firewall, then try pushing again.

### Unexpected response format from API

This means the selected provider returned a response in a different format than expected. Use a supported model/provider combination from the dropdown.

## Project Files

```text
index.html   Main chatbot app
README.md    Project documentation
```

