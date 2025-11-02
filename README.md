# yourls-frontend

# YOURLS Modern Frontend

A beautiful, white-labelable frontend interface for [YOURLS](https://yourls.org/) (Your Own URL Shortener) with QR code generation and modern UI/UX.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## ✨ Features

- 🎨 **White Label Customization** - Customize brand name, colors, and styling
- 🔗 **URL Shortening** - Create short links with optional custom keywords
- 📱 **QR Code Generation** - Generate downloadable QR codes for any short link
- 📊 **Link Management** - View and manage all your shortened links
- 💾 **Local Storage** - Settings saved in your browser (privacy-focused)
- 🎯 **Clean UI** - Modern, responsive design built with React and Tailwind CSS
- ⚡ **No Backend Required** - Pure frontend, works with any YOURLS instance

## 🚀 Live Demo

Visit the live demo: `https://yourusername.github.io/yourls-frontend/`

> **Note:** You'll need your own YOURLS instance to actually shorten URLs. The demo allows you to configure your connection.

## 📋 Requirements

### For End Users:

- A working YOURLS installation (self-hosted or provided by your organization)
- YOURLS API signature token
- CORS plugin installed on your YOURLS server (see setup below)

### For Hosting:

- Any web server or GitHub Pages (no special requirements)
- Modern web browser (Chrome, Firefox, Safari, Edge)

## 🔧 Setup Instructions

### Step 1: Install CORS Plugin on Your YOURLS Server

This is **required** for the frontend to communicate with your YOURLS API.

1. Download the CORS plugin:
   - Go to: https://github.com/TEODE/yourls-access-control-allow-origin
   - Click "Code" → "Download ZIP"

2. Install the plugin:
   ```
   yourls/
   └── user/
       └── plugins/
           └── access-control-allow-origin/
               └── plugin.php
   ```

3. Activate the plugin:
   - Go to your YOURLS admin panel
   - Navigate to "Manage Plugins"
   - Find "Access-Control-Allow-Origin"
   - Click "Activate"

### Step 2: Get Your API Signature Token

1. Log into your YOURLS admin panel
2. Go to "Tools" → "Secure passwordless API call"
3. Copy your signature token (keep this private!)

### Step 3: Configure the Frontend

1. Open the YOURLS Modern Frontend
2. Click the ⚙️ **Settings** icon in the top right
3. Enter your details:
   - **Brand Name**: Your preferred name (e.g., "MyShortLinks")
   - **Brand Color**: Your brand color (hex code)
   - **YOURLS API URL**: `https://yourdomain.com/yourls-api.php`
   - **API Signature Token**: Your token from Step 2

4. Click outside the settings to save

### Step 4: Start Shortening!

- Enter a long URL
- Optionally add a custom keyword
- Click "Shorten URL"
- Copy or generate QR code for your new short link

## 🌐 Hosting on GitHub Pages

### Quick Deploy:

1. Fork or create a new repository
2. Upload `index.html` to the repository root
3. Go to repository Settings → Pages
4. Select "main" branch as source
5. Your site will be live at: `https://yourusername.github.io/repository-name/`

### Share with Your Team:

Anyone can use your hosted frontend by:
1. Visiting your GitHub Pages URL
2. Configuring their own YOURLS credentials
3. Each user's settings are stored locally in their browser

## 🔒 Security & Privacy

- **API tokens are stored locally** in your browser's localStorage (never transmitted to our servers)
- **No data collection** - this is a pure frontend application
- **Keep your signature token private** - treat it like a password
- **HTTPS recommended** - use HTTPS for your YOURLS instance in production

## 🛠️ Troubleshooting

### "CORS not enabled on your server"

**Solution:** Install and activate the CORS plugin on your YOURLS server (see Step 1 above)

### "404 Not Found" when shortening

**Solution:** Check your API URL is correct. It should end with `/yourls-api.php`

Common formats:
- Root install: `https://yourdomain.com/yourls-api.php`
- Subdirectory: `https://yourdomain.com/short/yourls-api.php`
- Subdomain: `https://s.yourdomain.com/yourls-api.php`

### Links not appearing in YOURLS admin

**Solution:** Make sure you're using the real API (not demo mode). The HTML file should have real API calls enabled.

### QR codes not generating

**Solution:** This uses an external QR code API (qrserver.com). Make sure you have internet connectivity.

## 📚 Technical Details

### Built With:

- **React 18** - UI framework
- **Tailwind CSS** - Styling
- **YOURLS API** - URL shortening backend
- **QR Server API** - QR code generation

### Browser Compatibility:

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

### File Structure:

```
yourls-frontend/
├── index.html          # Complete standalone application
└── README.md          # This file
```

## 🎨 Customization

### White Label Settings:

All customization is done through the UI:
- Brand name
- Brand colors (hex codes)
- Logo (via icon color)

### Advanced Customization:

To modify the HTML/CSS/JS:
1. Edit `index.html`
2. Look for the React component code
3. Modify styling via Tailwind classes
4. Icons are inline SVG (easily replaceable)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

### Development:

The entire application is in a single HTML file for simplicity. To make changes:

1. Edit `index.html`
2. Test locally by opening in a browser
3. Test with a real YOURLS instance
4. Submit a pull request

## 📄 License

MIT License - feel free to use this for personal or commercial projects.

## 🙏 Credits

- Built for the [YOURLS](https://yourls.org/) community
- CORS plugin by [TEODE](https://github.com/TEODE/yourls-access-control-allow-origin)
- QR codes powered by [QR Server](https://goqr.me/api/)
- Icons inspired by [Lucide](https://lucide.dev/)

## 📞 Support

### For YOURLS Issues:
- YOURLS Documentation: https://yourls.org/docs
- YOURLS GitHub: https://github.com/YOURLS/YOURLS

### For Frontend Issues:
- Open an issue in this repository
- Check the Troubleshooting section above

## 🗺️ Roadmap

Potential future features:
- [ ] Bulk URL shortening
- [ ] Analytics dashboard
- [ ] Link editing capabilities
- [ ] Export links to CSV
- [ ] Custom QR code styling
- [ ] Multiple YOURLS account support
- [ ] Dark mode
- [ ] API stats tracking

## 📊 Version History

### v1.0.0 (2025-11-02)
- Initial release
- URL shortening with custom keywords
- QR code generation and download
- White label customization
- Link management interface
- Local settings storage

---

**Made with ❤️ for the YOURLS community**

Need help? Open an issue or check the [YOURLS forums](https://discourse.yourls.org/)