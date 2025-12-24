# Vyapari AI Terminal - Retro Edition

A retro-styled, web-based terminal interface for interacting with **Mistral AI Agents** and analyzing files. Built with a nostalgic 80s/90s hacker aesthetic featuring a cyberpunk green terminal theme.

![Version](https://img.shields.io/badge/version-2.5.0-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Status](https://img.shields.io/badge/status-stable-success)

## ✨ Features

- **Retro Terminal UI**: Classic CRT scanline effects, blinking cursors, and authentic hacker vibes
- **Mistral AI Integration**: Seamlessly interact with Mistral AI Agents for intelligent file analysis
- **File Context**: Upload PDFs, text files, code, and more for AI-powered analysis
- **Credit System**: OTP-based authentication and credit management for API access
- **Markdown Rendering**: Beautiful formatting of AI responses with code blocks and styling
- **PDF Support**: Built-in PDF.js integration for parsing multi-page documents
- **Mobile Responsive**: Fully functional on mobile with sidebar menu toggle
- **No Backend Required**: Runs entirely in the browser - pure client-side JavaScript

## 🚀 Quick Start

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- A Mistral AI API Key (get one at [console.mistral.ai](https://console.mistral.ai/api-keys))
- A Mistral Agent ID (create agents in your Mistral console)

### Deployment

1. **GitHub Pages Hosting** (Recommended)
   - Fork this repository
   - Go to Settings → Pages
   - Enable GitHub Pages from the `main` branch
   - Your site will be live at `https://yourusername.github.io/coder`

2. **Local Development**
   - Clone the repository
   - Open `index.html` in your browser
   - Start interacting!

3. **Alternative Hosting**
   - Deploy to Vercel, Netlify, or Railway (all free options)
   - Simply upload the files to your hosting service

## 🔐 Security & API Keys

### Important: Protecting Your API Keys

⚠️ **NEVER commit your API keys to the repository!**

The `.gitignore` file already protects common secret file patterns. To add your API key:

1. **Option 1: Environment Variables (Recommended)**
   ```bash
   # Create a .env file (it's in .gitignore, so it won't be committed)
   MISTRAL_API_KEY=your_key_here
   AGENT_ID=your_agent_id
   ```

2. **Option 2: Browser Input**
   - The app provides a secure modal dialog in the UI
   - Click "./configure_api" in the sidebar
   - Enter your API key when prompted
   - It's stored in your browser's session (not persisted)

3. **Option 3: Local Storage (Advanced)**
   - Modify `index.html` to load from localStorage
   - The user provides the key on first use
   - Browser stores it locally on their machine

## 📁 File Structure

```
coder/
├── index.html          # Main application (all-in-one file)
├── README.md           # This file
├── .gitignore          # Protects API keys and sensitive data
└── assets/             # (Optional) For future styling/images
```

## 🎮 Usage

1. **Upload a File**
   - Click `[upload_new.file]` in the sidebar
   - Select a PDF, text file, code file, etc.
   - The file content is loaded into memory

2. **Add Credits**
   - Click `auth_module.exe` in the sidebar
   - Click `./generate_otp.sh` to get a token
   - (This would normally send to a Discord webhook)
   - Enter the code to add credits

3. **Configure API**
   - Click `api_keys.conf` or wait for an auth error
   - Enter your Mistral API Key
   - Key is stored in your browser session

4. **Chat with AI**
   - Type your query in the terminal input
   - The AI analyzes your uploaded file context
   - Responses appear in the terminal output

## 🛠️ Customization

### Changing the Color Scheme
Edit the CSS variables in the `<style>` section of `index.html`:
```javascript
colors: {
  term: {
    bg: '#0c0c0c',        // Background
    green: '#4af626',     // Primary accent
    blue: '#3b82f6',      // Secondary accent
    red: '#ef4444',       // Error color
    yellow: '#eab308'     // Warning color
  }
}
```

### Replacing the Webhook
If using the OTP Discord webhook feature:
1. Open `index.html`
2. Find `const WEBHOOK_URL = ...`
3. Replace with your Discord webhook URL (or disable the feature)

### Agent Configuration
Update the Agent ID in the code:
```javascript
const AGENT_ID = "your_agent_id_here";
```

## 🌐 Hosting Recommendations

### GitHub Pages (Free, Recommended)
- Built into your GitHub repository
- Automatically updates with new commits
- No configuration needed

### Vercel (Free)
- Instant deployments
- Automatic HTTPS
- Global CDN
- [Deploy with Vercel](https://vercel.com/new)

### Netlify (Free)
- Drag-and-drop deployment
- Form handling (optional)
- [Deploy with Netlify](https://app.netlify.com/start)

### Railway (Free Tier)
- Easy setup
- Good for experiments
- [Deploy with Railway](https://railway.app)

## 🔒 Privacy & Data

- **No Server**: This app runs 100% in your browser
- **No Tracking**: No analytics, no cookies, no telemetry
- **File Privacy**: Files are never stored - only processed in memory
- **API Keys**: Only you see your Mistral API key
- **HTTPS**: Always use HTTPS when deploying (automatic on GitHub Pages)

## 📝 License

MIT License - Feel free to fork, modify, and use this project!

## 🤝 Contributing

Found a bug? Have a feature idea? Open an issue or submit a pull request!

## 💡 Ideas for Enhancement

- [ ] Multiple file context support
- [ ] Chat history export
- [ ] Custom themes/color picker
- [ ] Keyboard shortcuts guide
- [ ] Agent selection dropdown
- [ ] Response copy-to-clipboard
- [ ] Rate limiting visualization

## 👨‍💻 Author

**Anish Vyapari** - AI/ML Developer | Discord Bot Enthusiast | Full-Stack Web Developer

- GitHub: [@AnishVyapari](https://github.com/AnishVyapari)
- Skills: Python, JavaScript, TypeScript, Discord.py, React, Cloud Deployment

## 🙏 Acknowledgments

- [Mistral AI](https://mistral.ai) for the powerful API
- [Tailwind CSS](https://tailwindcss.com) for styling
- [Font Awesome](https://fontawesome.com) for icons
- [PDF.js](https://mozilla.github.io/pdf.js/) for PDF parsing
- [Google Fonts](https://fonts.google.com) - Fira Code for that authentic terminal look

---

**Remember**: Always protect your API keys! Use `.gitignore` and never commit secrets to version control.
