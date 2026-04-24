# Setup Guide

Complete setup instructions for running Readie in different environments.

## 📋 Table of Contents

- [Quick Start (claude.ai)](#quick-start-claudeai)
- [Local Setup with API Key](#local-setup-with-api-key)
- [Gmail Integration](#gmail-integration)
- [Troubleshooting](#troubleshooting)

---

## Quick Start (claude.ai)

**Best for:** Full features including Gmail integration

### Steps

1. Go to [claude.ai](https://claude.ai)
2. Start a new conversation
3. Upload `readie.html` from this repository
4. Claude will create an artifact - click to open it
5. Done! ✅

**What works:**
- ✅ Brief generation (no API key needed)
- ✅ Gmail integration (fetch recent, search inbox)
- ✅ File uploads
- ✅ PDF downloads
- ✅ All meeting types

**Limitations:**
- Can only be used within claude.ai
- Requires active Claude subscription (Pro/Team)

---

## Local Setup with API Key

**Best for:** Running on your own computer, sharing with team

### Prerequisites

- Modern web browser (Chrome, Firefox, Safari)
- Anthropic API key

### Getting Your API Key

1. Visit [console.anthropic.com](https://console.anthropic.com)
2. Sign up or log in
3. Navigate to **API Keys** section
4. Click **Create Key**
5. Copy the key (starts with `sk-ant-...`)
6. **⚠️ Important**: Never commit this key to GitHub!

### Running Readie

1. **Download** `readie.html` from this repository
2. **Open** the file in your browser:
   - Double-click the file, OR
   - Drag it into your browser window, OR
   - Right-click → Open With → Chrome/Firefox/Safari

3. **Enter API Key**:
   - You'll see a password input at the top-left
   - Paste your API key there
   - The key is stored only in browser memory (not saved to disk)

4. **Generate Brief**:
   - Add some sources (upload files or paste content)
   - Click "Regenerate brief"
   - Wait 5-10 seconds
   - Your brief appears! ✅

### What Works Locally

- ✅ Brief generation (with API key)
- ✅ File uploads (PDF, DOCX, XLSX, CSV, TXT, EML)
- ✅ Manual content entry
- ✅ PDF downloads
- ✅ All meeting types

### What Doesn't Work Locally

- ❌ Gmail integration (requires MCP servers from claude.ai)
- ❌ Real-time email fetching

**Workaround for emails:**
- Save emails as .eml or .txt files
- Upload them as sources
- Works the same way!

---

## Gmail Integration

Gmail integration uses Anthropic's MCP (Model Context Protocol) servers and **only works in claude.ai**.

### How It Works

When running in claude.ai:

1. **Fetch Recent**: Gets your 5 most recent emails
2. **Search**: Searches your inbox with a query
3. **Select**: Click + to add emails as sources
4. **Auto-generate**: Brief updates automatically

### Authentication

- Gmail auth is handled by claude.ai
- First time: You may need to connect Gmail in Settings
- Subsequent uses: Works automatically

### Privacy

- Emails are sent to Anthropic API for processing
- No emails are stored by Readie
- API calls are ephemeral
- See [Anthropic's Privacy Policy](https://www.anthropic.com/legal/privacy)

---

## File Upload Guide

Readie supports multiple file formats:

### Supported Formats

| Format | Extension | What's Extracted |
|--------|-----------|------------------|
| Email | `.eml` | Subject, sender, body, date |
| Text | `.txt` | Full content |
| Markdown | `.md` | Full content |
| PDF | `.pdf` | Text content |
| Word | `.docx` | Text content |
| Excel | `.xlsx`, `.xls` | All sheets as CSV |
| CSV | `.csv` | Full content |
| PowerPoint | `.pptx` | Text content |

### Best Practices

**For Emails:**
- Save emails as .eml (most email clients support this)
- Or copy/paste email content into a .txt file
- Include subject line and sender for better context

**For Documents:**
- Keep files under 5MB each
- Text-heavy files work best
- Images in PDFs/docs may not be processed

**For Spreadsheets:**
- Data is converted to CSV format
- All sheets are included
- Large spreadsheets (1000+ rows) may be truncated

---

## Troubleshooting

### "Could not generate brief — check console for errors"

**Problem:** Brief generation failed

**Solutions:**
1. Check if you entered an API key (local mode)
2. Check browser console (F12) for errors
3. Verify API key is valid
4. Check your Anthropic account has credits

### "Gmail connection required"

**Problem:** Gmail integration not working

**Solutions:**
1. Verify you're using Readie in claude.ai (not locally)
2. Connect Gmail in Claude Settings
3. Use file uploads as workaround

### PDF Download Not Working

**Problem:** Download button doesn't work or PDF is blank

**Solutions:**
1. Check browser console (F12) for errors
2. Try a different browser
3. Ensure popup blockers aren't blocking download
4. Verify brief was generated successfully first

### Brief Generation is Slow

**Problem:** Takes more than 30 seconds

**Solutions:**
1. Reduce number of sources (try 5-10 max)
2. Use shorter documents
3. Check your internet connection
4. Try regenerating

### API Key Not Working

**Problem:** "API Error: authentication failed"

**Solutions:**
1. Verify key starts with `sk-ant-`
2. Check for extra spaces when pasting
3. Verify key is active in console.anthropic.com
4. Check account has available credits

### Characters Look Weird in PDF

**Problem:** Emojis or special characters appear as symbols

**Solutions:**
- This is expected - PDFs use ASCII-safe characters
- ✅ becomes [WIN]
- ⚠️ becomes [RISK]
- This ensures compatibility across all PDF viewers

---

## Advanced Setup

### Running on a Web Server

For team deployments:

1. Host `readie.html` on any web server
2. Share the URL with your team
3. Each person enters their own API key
4. No server-side setup needed!

**Example with Python:**
```bash
python -m http.server 8000
# Visit http://localhost:8000/readie.html
```

**Example with Node:**
```bash
npx http-server
# Visit http://localhost:8080/readie.html
```

### Environment Variables (Not Supported)

Readie is a client-side app, so it doesn't use environment variables.

API keys must be entered in the UI for security reasons.

### Custom Domains

To use a custom domain:
1. Upload `readie.html` to your web host
2. Configure your domain DNS
3. Users access via your domain
4. Everything works the same!

---

## Security Best Practices

### API Key Safety

- ✅ **DO** keep your API key secret
- ✅ **DO** use different keys for testing/production
- ✅ **DO** set spending limits in console.anthropic.com
- ❌ **DON'T** commit API keys to GitHub
- ❌ **DON'T** share API keys via email/Slack
- ❌ **DON'T** hardcode keys in the HTML file

### Data Privacy

- No data is stored by Readie
- All processing happens via API calls
- Files are read in-browser only
- Brief content exists only in browser memory
- PDFs are generated locally

### Recommendations

- Use Readie on trusted devices only
- Clear browser cache after use on shared computers
- Don't use sensitive data in public demos
- Review Anthropic's data retention policies

---

## Performance Tips

### For Faster Brief Generation

1. **Limit sources to 5-10 items**
   - Quality over quantity
   - Most meetings don't need 50 emails

2. **Keep documents concise**
   - Trim long email threads
   - Extract key sections from large docs

3. **Use specific meeting types**
   - More specific = better output
   - "1:1 with Manager" > generic meeting

### For Large Teams

1. **Share one URL** instead of distributing files
2. **Set up a team API key** with spending limits
3. **Create templates** for common meeting types
4. **Document your workflow** for consistency

---

## Getting Help

- 📖 Read the [README](README.md)
- 🐛 Report bugs via [GitHub Issues](https://github.com/yourusername/readie/issues)
- 💬 Ask questions in [Discussions](https://github.com/yourusername/readie/discussions)
- 📧 Contact: [your@email.com]

---

**Ready to prep smarter? Let's go! 🚀**
