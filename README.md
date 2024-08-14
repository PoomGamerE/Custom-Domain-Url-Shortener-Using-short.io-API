# Custom Domain URL Shortener Web (Using short.io API)

This is a simple and user-friendly URL shortener web application that allows users to shorten URLs and generate QR codes. The design is clean and minimal, similar to popular URL shortener services like Bitly and TinyURL.

## Features

- **Shorten URLs:** Users can shorten any valid URL.
- **Custom Paths:** Optionally, users can specify a custom path for their shortened URL.
- **URL Title:** Users can provide a title for their shortened URL.
- **QR Code Generation:** Automatically generates a QR code for the shortened URL.
- **Copy to Clipboard:** Users can easily copy the shortened URL to the clipboard.
- **Responsive Design:** The interface is designed to work well on both desktop and mobile devices.

## Getting Started

### Prerequisites

To run this project, you need a web browser and internet connection. No additional software or server setup is required.

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/PoomGamerE/shorturl-public.git
    cd shorturl-public
    ```

2. Open `index.html` in your browser to start using the URL shortener.

### Configuration

Before using the application, you need to update the domain and API key to your own.

1. **Replace the `domain` variable** in the JavaScript section with your own custom domain.
2. **Replace the `Authorization` header** with your own Public API Key from Short.io.

   ```javascript
   const domain = 'your-custom-domain';
   const options = {
       method: 'POST',
       headers: {
           accept: 'application/json',
           'content-type': 'application/json',
           Authorization: 'your-public-api-key'
       },
       body: JSON.stringify(data)
   };
   ```

**Note:** This application uses the public API for generating short URLs, which means it can be used by anyone. If you need to create private links, you should use the [Short.io](https://short.io) Secret API keys with the `https://api.short.io/links` endpoint instead of the public API.

### Usage

1. Enter the original URL you want to shorten in the **Original URL** field.
2. Optionally, you can provide a custom path and a title for the shortened URL.
3. Click the **Shorten URL** button.
4. The shortened URL and QR code will be displayed below the form.
5. You can copy the shortened URL by clicking the **Copy Link** button.

### Customization

You can customize the appearance and functionality of the application by modifying the `index.html` file.

- **Styles:** Adjust the CSS in the `<style>` section to change the look and feel.
- **JavaScript:** Modify the script section to change the behavior, such as how the URL shortening API is called.

### API

This project uses the [Short.io](https://short.io) API to shorten URLs. You can replace the API key with your own by modifying the `Authorization` header in the JavaScript code.

### Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an issue to discuss potential changes.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Acknowledgements

- [Short.io](https://short.io) for the URL shortening API.
- [QRCode.js](https://github.com/davidshimjs/qrcodejs) for the QR code generation library.
