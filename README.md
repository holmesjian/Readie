s# Readie 🚀

> **Stop prepping. Start Readie.**

Readie reads your week for you. It spots the risks, frames the decisions, anticipates the pushback, and generates tailored briefs for every meeting type — 1:1s, team syncs, project reviews, customer calls — in seconds.

**Your week, already translated.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Built with Claude](https://img.shields.io/badge/built%20with-Claude%20API-blue)](https://www.anthropic.com)
[![Single File](https://img.shields.io/badge/deployment-single%20file-orange)](https://github.com/holmesjian/Readie)
[![Hackathon](https://img.shields.io/badge/hackathon-Push%20to%20Prod%202026-ff69b4)](https://github.com/holmesjian/Readie)

## 🎯 Try It Now

**[📥 Download readie.html](https://github.com/holmesjian/Readie/raw/main/readie.html)** - Open in your browser and start prepping!

**[🌐 Live Demo on GitHub Pages](https://holmesjian.github.io/Readie/readie.html)** - Try it without downloading

---

## ✨ Features

- **🤖 AI-Powered Brief Generation** - Uses Claude Sonnet 4 to analyze your emails, docs, and messages
- **🎯 Context-Aware Adaptation** - Same data → 4 different briefs for different audiences
- **📧 Gmail Integration** - Pull emails directly from your inbox (when used in claude.ai)
- **📄 Multiple Input Sources** - Email, Teams, Slack, Docs, PDFs, Excel
- **📋 Professional PDF Export** - Download meeting briefs as formatted PDFs
- **⚡ Zero Setup** - Single HTML file, works in any browser

## 🎯 Meeting Types

Readie adapts the same information for different contexts:

| Meeting Type | Audience | Style |
|--------------|----------|-------|
| **1:1 with Manager** | Your manager | Candid, complete, includes all internal details |
| **Team Sync** | Full team | Collaborative, surfaces blockers and decisions |
| **Stakeholder Review** | Executives | Business language, no technical jargon |
| **Customer Call** | Customers | Customer-first framing, no internal details |

## 🚀 Quick Start

### Option 1: Use in claude.ai (Recommended for Full Features)

1. Go to [claude.ai](https://claude.ai)
2. Upload `readie.html` 
3. Click to open the artifact
4. **Gmail integration works automatically** ✅

### Option 2: Run Locally

1. Download `readie.html`
2. Open in Chrome
3. Get your Anthropic API key:
   - Visit [console.anthropic.com](https://console.anthropic.com)
   - Create an API key (starts with `sk-ant-...`)
4. Paste API key in the input field at top-left
5. Click "Regenerate brief"

**Note:** Gmail integration requires MCP servers and only works in claude.ai. Use file uploads when running locally.

## 📖 How It Works

1. **Add Sources**: Upload emails, docs, or connect Gmail
2. **Select Meeting**: Choose your meeting type (1:1, Team Sync, etc.)
3. **Generate Brief**: AI analyzes sources and creates a tailored agenda
4. **Download PDF**: Get a professional PDF for your meeting

## 🎨 Example Output

```
1 [WIN] Wins & Momentum                                    5 min
  - Design phase completed on schedule [TEAMS]
  - Engineering team at full capacity [EMAIL]

2 [RISK] Delivery Timeline - Decision Required           15 min
  - API integration 8 days behind due to dependency gap [EMAIL]
  
  OPTION A: Descope reporting → ship May 1
  OPTION B: Keep full scope → push to May 15

3 Next Steps                                               5 min
  - OWNER: Me - Notify stakeholders of decision [EMAIL]
  - OWNER: Manager - Sign off on scope today [TEAMS]
```

## 🏗️ Architecture

- **Frontend**: React (via Babel in-browser transpilation)
- **AI**: Anthropic Claude Sonnet 4 API
- **PDF Export**: jsPDF library
- **File Parsing**: SheetJS (XLSX), native browser APIs
- **Deployment**: Single self-contained HTML file (no build step!)

## 🔧 Technical Details

### Key Features

- **Single File Architecture**: Entire app in one HTML file (~2100 lines)
- **No Build Process**: Uses Babel Standalone for in-browser JSX compilation
- **Offline Capable**: Once loaded, works without internet (except AI calls)
- **No Backend Required**: Direct API calls to Anthropic

### API Usage

The app makes POST requests to `https://api.anthropic.com/v1/messages`:

```javascript
// When used locally
headers: {
  "x-api-key": "your-api-key",
  "anthropic-version": "2023-06-01"
}

// When used in claude.ai
headers: {
  "anthropic-dangerous-direct-browser-calls": "true"
}
```

### Character Encoding

The PDF export automatically converts emoji to ASCII-safe alternatives:
- ✅ → `[WIN]`
- ⚠️ → `[RISK]`
- ⛔ → `[ALERT]`

This ensures professional, readable PDFs across all viewers.

## 💰 Cost

When using your own API key:
- ~$0.003 per brief generation
- 100 briefs = ~$0.30
- Demo with 50+ generations = under $1

## 🎯 Use Cases

- **Product Managers**: Prep for stakeholder reviews, 1:1s, sprint planning
- **Engineering Leads**: Team syncs, technical reviews, project updates
- **Executives**: Board meetings, investor calls, strategic planning
- **Sales**: Customer calls, QBRs, deal reviews

## 🤝 Contributing

This was built for the **Push-to-Prod Hackathon**. Contributions welcome!

### Ideas for Enhancement

- [ ] Connect to Calendar (Google Calendar, Outlook)
- [ ] Add more meeting types (Stand-ups, Retrospectives, All-hands)
- [ ] Export to Notion, Confluence, Google Docs
- [ ] Add Slack bot integration
- [ ] Multi-language support
- [ ] Custom meeting templates

## 📧 Contact & Links

**Built for Push-to-Prod Hackathon 2026**

- 🌟 **Star this repo** if Readie helped you prep for a meeting!
- 🐛 **Report bugs** via [GitHub Issues](https://github.com/holmesjian/Readie/issues)
- 💡 **Request features** via [GitHub Discussions](https://github.com/holmesjian/Readie/discussions)

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

Copyright (c) 2026 holmesjian

---

<div align="center">

**[⭐ Star on GitHub](https://github.com/holmesjian/Readie)** • **[📥 Download](https://github.com/holmesjian/Readie/raw/main/readie.html)** • **[🐛 Report Bug](https://github.com/holmesjian/Readie/issues)** • **[💡 Request Feature](https://github.com/holmesjian/Readie/discussions)**

Made with ❤️ for better meetings everywhere

</div>
