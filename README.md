# TOTP Generator

This project is a simple, web-based Time-Based One-Time Password (TOTP) generator that functions similarly to Google Authenticator and Authy. It allows you to generate TOTP codes using secret keys stored in text files on a USB drive. Each site can have its own key file, and the application will automatically generate a new TOTP code every 30 seconds.

## Features

- Generates TOTP codes using secret keys stored in text files.
- Automatically updates TOTP codes every 30 seconds.
- Displays the current key file being used.
- Provides a user-friendly interface for loading secret keys and generating TOTP codes.

## How to Set Up

### Prerequisites

- A USB drive.
- A modern web browser (Google Chrome, Firefox, Safari, etc.).

### Step-by-Step Setup

1. **Prepare the USB Drive:**
   - Download the `index.html` file provided in this repository.
   - Save the `index.html` file to the root directory of your USB drive.

2. **Create Secret Key Files:**
   - Obtain the secret key from the website for which you want to generate TOTP codes.
   - The secret key is usually provided as a base32-encoded string during the 2FA setup process. If a QR code is provided, look for an option to display the key as text.
   - Create a text file with the name of the website (e.g., `eneba.txt`) and paste the secret key into this file.
   - Save the text file to the root directory of your USB drive.

### Example

For example, if you are setting up 2FA for the site "Eneba":

1. Go to the 2FA setup page on Eneba and copy the provided secret key (base32-encoded string).
2. Create a text file named `eneba.txt`.
3. Paste the secret key into `eneba.txt` and save the file to the USB drive.

## How to Use

1. **Insert the USB Drive:**
   - Insert the USB drive into any computer with a web browser.

2. **Open the HTML File:**
   - Navigate to the USB drive in File Explorer (Windows) or Finder (macOS).
   - Double-click the `index.html` file to open it in the default web browser.

3. **Load Secret Key and Generate OTP:**
   - Click the "Load Secret Key" button and select the appropriate secret key file (e.g., `eneba.txt`).
   - The filename of the loaded key will be displayed.
   - The OTP will be generated and displayed after the file is selected.
   - The script will automatically generate a new OTP every 30 seconds and update the countdown timer.

## Notes

- Each website will have its own secret key, which you need to save in a separate text file.
- Make sure to name the text files appropriately to easily identify which key is for which site.
- The secret keys must be base32-encoded strings.

## Security

- Keep your USB drive secure and do not share your secret key files with others.
- This tool generates OTPs locally in your browser and does not send any information over the internet.

## Compatibility

- This tool should work in any modern web browser that supports JavaScript and HTML5.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Acknowledgments

- This tool uses the [jsSHA](https://github.com/Caligatio/jsSHA) library for generating SHA-1 hashes.
