# 🧠 Hybrid AI Assistant

> A minimalist, ChatGPT-style web application combining Chrome Built-in AI (Gemini Nano) and Google Gemini API for powerful hybrid AI capabilities

[![Chrome Built-in AI Challenge 2025](https://img.shields.io/badge/Challenge-Chrome%20AI%202025-blue)](https://googlechromeai.devpost.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🌟 Overview

Hybrid AI Assistant is a versatile web application that seamlessly switches between **offline (Chrome Built-in AI)** and **online (Google Gemini API)** modes, providing users with the best of both worlds: privacy-first on-device processing and powerful cloud-based AI capabilities.

## ✨ Key Features

### 🔄 Hybrid AI System
- **Offline Mode**: Uses Chrome Built-in AI APIs (Gemini Nano) for privacy and speed
- **Online Mode**: Uses Google Gemini API for advanced capabilities
- **One-Click Toggle**: Switch between modes instantly
- **Smart Processing**: Automatic fallback and error handling

### 🛠️ AI Tools

**Offline Mode (6 Tools):**
1. **Prompt** - Refine and improve prompts
2. **Proofreader** - Fix grammar, spelling, punctuation
3. **Write** - Generate original content
4. **Rewrite** - Improve and rephrase text
5. **Summarise** - Create concise summaries
6. **Translate** - Multi-language translation

**Online Mode (9 Tools - All Above Plus):**
7. **Ask** - General Q&A with Gemini AI
8. **Create Image** - Image generation (integration ready)
9. **Create Video** - Video generation (integration ready)

### 🎨 Modern UI/UX
- **Minimalist Design** - Clean, distraction-free interface
- **Dark/Light Mode** - Theme toggle for comfort
- **Responsive** - Works on desktop, tablet, and mobile
- **ChatGPT-Style** - Familiar conversation interface
- **Smooth Animations** - Professional transitions
- **Multi-language Support** - Works with all languages

## 🚀 Live Demo

https://lucifertkod.github.io/Chrome-built-in-hackathon-project-/

## 📹 Demo Video

https://youtu.be/MokqK4kkp08?si=QndIrZ0bX8gHVe0C

## 🏗️ Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript ES6+
- **Offline AI**: Chrome Built-in AI APIs (Gemini Nano)
- **Online AI**: Google Gemini API (gemini-pro)
- **Architecture**: Single-file application (no build tools needed)
- **Icons**: Font Awesome 6
- **Storage**: LocalStorage for preferences

## 📋 Prerequisites

### For Offline Mode:
1. **Chrome Dev/Canary** (Version 127+)
   - Download: [Chrome Dev](https://www.google.com/chrome/dev/)
   - Or: [Chrome Canary](https://www.google.com/chrome/canary/)

2. **Enable Chrome Flags** in `chrome://flags`:
   - `#optimization-guide-on-device-model` → Enabled BypassPerfRequirement
   - `#prompt-api-for-gemini-nano` → Enabled
   - `#summarization-api-for-gemini-nano` → Enabled
   - `#translation-api` → Enabled
   - `#rewriter-api` → Enabled
   - `#writer-api` → Enabled

3. **Download Gemini Nano Model**:
   - Go to `chrome://components`
   - Find "Optimization Guide On Device Model"
   - Click "Check for update"
   - Wait for download (~1.7GB)

### For Online Mode:
- Active internet connection
- Google Gemini API key (already configured in code)

## 🔧 Installation & Setup

### Quick Start (No Installation Required!)

1. **Download the project**:
```bash
git clone https://github.com/yourusername/hybrid-ai-assistant.git
cd hybrid-ai-assistant
```

2. **Open in Chrome Dev/Canary**:
   - Simply open `index.html` in Chrome Dev/Canary
   - That's it! No npm install, no build process

### Using Local Server (Recommended)

**Python:**
```bash
python -m http.server 8000
# Open http://localhost:8000
```

**Node.js:**
```bash
npx live-server
# Opens automatically
```

**PHP:**
```bash
php -S localhost:8000
```

## 📖 How to Use

### 1. Choose Your Mode
- **Online Mode** (default): Toggle is ON (right side)
  - Uses Google Gemini API
  - Requires internet
  - More powerful for complex tasks
  
- **Offline Mode**: Toggle is OFF (left side)
  - Uses Chrome Built-in AI
  - Works without internet
  - Private and fast

### 2. Select a Tool (Optional)
- Click the **+** button to open tool selector
- Choose from available tools
- Tool selection is shown as a badge with your message

### 3. Type Your Message
- Enter your query in the input field
- Press **Enter** or click the arrow button
- Wait for AI response

### 4. View Response
- Your message appears on the right with tool badge
- AI response appears below in a card
- Scroll through conversation history

### 5. Additional Features
- **New Chat**: Click hamburger menu → New Chat
- **Theme Toggle**: Switch between dark/light mode
- **Chat History**: Access previous conversations (sidebar)

## 🎯 Use Cases

### Students
- Fix grammar in essays
- Summarize long research papers
- Translate study materials
- Generate study prompts

### Content Creators
- Write blog posts and articles
- Rewrite content for different audiences
- Generate social media captions
- Improve existing content

### Professionals
- Draft professional emails
- Summarize meeting notes
- Translate business documents
- Create product descriptions

### Developers
- Refine AI prompts
- Generate documentation
- Rewrite code comments
- Translate error messages

## 🔐 Privacy & Security

### Offline Mode Benefits:
- ✅ All processing happens on your device
- ✅ No data sent to external servers
- ✅ Works without internet
- ✅ Complete privacy

### Online Mode:
- ⚠️ Data sent to Google Gemini API
- ⚠️ Subject to Google's privacy policy
- ✅ Secure HTTPS connection
- ✅ No data stored by application

### API Key Security:
- 🔒 API key is embedded in client-side code
- ⚠️ For production, use server-side proxy
- 💡 Consider environment variables for deployment

## 🏆 Chrome Built-in AI Challenge 2025

This project is submitted for:
- **Best Hybrid AI Application - Web Application** ($9,000 prize)
- **Most Helpful - Web Application** ($14,000 prize)

### Why This Project Stands Out:

1. **True Hybrid Architecture**: Seamlessly combines offline and online AI
2. **User Choice**: Lets users decide between privacy and power
3. **Practical Tools**: Solves real problems for real users
4. **Excellent UX**: Minimalist, intuitive, familiar interface
5. **Multi-language**: Supports all languages in input and output
6. **No Dependencies**: Single-file, works anywhere
7. **Production Ready**: Fully functional, polished application

## 📊 API Usage

### Offline Mode - Chrome AI APIs

```javascript
// Example: Using Prompt API
const session = await window.ai.languageModel.create({
    systemPrompt: 'You are a helpful assistant.'
});
const result = await session.prompt('Your message here');
session.destroy();
```

### Online Mode - Gemini API

```javascript
// Example: Using Gemini API
const response = await fetch(
    `https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent?key=${API_KEY}`,
    {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({
            contents: [{
                parts: [{ text: 'Your message here' }]
            }]
        })
    }
);
```

## 🔮 Future Enhancements

- [ ] Actual video generation integration
- [ ] Voice input/output
- [ ] Export chat history
- [ ] User authentication
- [ ] Cloud sync for chat history
- [ ] Custom tool creation
- [ ] Batch processing
- [ ] Chrome Extension version
- [ ] Mobile app version (PWA)
- [ ] Collaborative features
- [ ] Advanced prompt templates

## 🐛 Troubleshooting

### Issue: Offline mode not working

**Solution:**
1. Verify Chrome version: `chrome://version` (must be 127+)
2. Check all flags enabled: `chrome://flags`
3. Download model: `chrome://components`
4. Restart Chrome completely
5. Check console for errors (F12)

### Issue: Online mode not working

**Solution:**
1. Check internet connection
2. Verify API key is correct
3. Check browser console for errors
4. Try in incognito mode
5. Check API quota limits

### Issue: "APIs not available" error

**Solution:**
```javascript
// Open browser console (F12)
// Run this to check:
console.log('Chrome AI:', window.ai);
console.log('Language Model:', window.ai?.languageModel);
```

### Issue: Slow responses

**Cause:** First request loads the AI model
**Solution:** Subsequent requests will be faster

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see [LICENSE](LICENSE) file.

## 🙏 Acknowledgments

- Google Chrome Team for Built-in AI APIs
- Google AI for Gemini API
- Chrome Built-in AI Challenge 2025
- Font Awesome for icons
- Open source community

## 📧 Contact

**Developer**: Abhinav Anand
**Email**: lucifertkod2007aa@gmail.com
**GitHub**: https://github.com/lucifertkod
**Project**:https://github.com/lucifertkod/Chrome-built-in-hackathon-project-

## 🌟 Star This Project

If you find this project helpful, please give it a ⭐ on GitHub!

---

**Built with ❤️ for Chrome Built-in AI Challenge 2025**