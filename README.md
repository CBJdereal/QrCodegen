# QR Code Generator

## Overview

This project is a simple QR Code Generator built using HTML, CSS, and JavaScript. It allows users to input URLs or any text to generate a corresponding QR code. The generated QR code can be used for various purposes such as sharing links, contact information, or other data.

## Features

- User-friendly interface for generating QR codes.
- Ability to input any text or URL to create a QR code.
- Responsive design for better user experience on different devices.

## Installation

To use this QR Code Generator, follow these steps:

1. Clone the repository or download the project files.
2. Open the `index.html` file in your web browser.

## Usage

1. Open `index.html` in your web browser.
2. Enter the URL or text you want to convert into a QR code in the input field.
3. Click the "Generate QR" button.
4. The generated QR code will be displayed below the input field.

## Project Structure

- `index.html`: The main HTML file containing the structure of the QR Code Generator.
- `style.css`: The CSS file containing the styles for the QR Code Generator.
- `script.js`: The JavaScript file containing the functionality to generate the QR code (embedded in `index.html`).

## Code Overview

### index.html

The HTML file contains the structure and layout of the QR Code Generator, including the input field, button, and the area where the QR code is displayed.

### style.css

The CSS file contains the styling for the QR Code Generator. It uses the Poppins font and has a simple, clean design with a responsive layout.

### JavaScript

The JavaScript functionality is embedded in the `index.html` file. It handles the click event on the "Generate QR" button, retrieves the input value, and uses the QRServer API to generate the QR code.

```javascript
const wrapper = document.querySelector(".wrapper");
const generateBtn = document.querySelector(".form button");
const qrInput = document.querySelector(".form input");
const qrImg = document.querySelector(".qr-code img");
const qrError = document.querySelector(".qr-code h2");

generateBtn.addEventListener("click", () => {
    let qrValue = qrInput.value;
    
    if(!qrValue) return;
    qrImg.src = `https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=${qrValue}`;
    wrapper.classList.add("active");
});
```

## Dependencies

- [QRServer API](https://goqr.me/api/): Used to generate the QR codes.

## Acknowledgements

- Font: [Google Fonts - Poppins](https://fonts.google.com/specimen/Poppins)

