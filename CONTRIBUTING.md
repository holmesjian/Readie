# Contributing to Readie

Thank you for considering contributing to Readie! 🎉

## How to Contribute

### Reporting Bugs

If you find a bug, please create an issue with:
- Clear description of the bug
- Steps to reproduce
- Expected vs actual behavior
- Screenshots if applicable
- Browser and OS version

### Suggesting Features

Feature requests are welcome! Please create an issue with:
- Clear description of the feature
- Why it would be useful
- Example use cases
- Mockups or examples if applicable

### Code Contributions

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Make your changes**
4. **Test thoroughly** - the app should work both:
   - In claude.ai (without API key)
   - Locally (with API key)
5. **Commit**: `git commit -m 'Add amazing feature'`
6. **Push**: `git push origin feature/amazing-feature`
7. **Open a Pull Request**

### Development Guidelines

#### Code Style

- Keep the single-file architecture (no build step)
- Use React functional components with hooks
- Follow the existing code organization
- Add comments for complex logic
- Keep functions focused and small

#### Testing Checklist

Before submitting a PR, verify:

- [ ] Works in Chrome (latest)
- [ ] Works in Firefox (latest)
- [ ] Works in Safari (latest)
- [ ] Brief generation works with API key
- [ ] Brief generation works without API key (in claude.ai)
- [ ] PDF download works and produces readable PDFs
- [ ] File uploads work (PDF, DOCX, XLSX, CSV, TXT)
- [ ] Gmail integration works (in claude.ai)
- [ ] No console errors
- [ ] All existing features still work

#### Key Areas for Contribution

**High Priority:**
- [ ] Add more meeting types (Stand-ups, Retrospectives, All-hands)
- [ ] Calendar integration (Google Calendar, Outlook)
- [ ] Better error handling and user feedback
- [ ] Mobile responsive design improvements
- [ ] Performance optimization for large email volumes

**Medium Priority:**
- [ ] Export to other formats (Markdown, Google Docs, Notion)
- [ ] Custom meeting templates
- [ ] Dark mode
- [ ] Multi-language support
- [ ] Keyboard shortcuts

**Nice to Have:**
- [ ] Browser extension version
- [ ] Slack bot integration
- [ ] Teams integration
- [ ] Voice interface for brief reading
- [ ] Analytics dashboard

### Architecture Notes

#### Single File Design

Readie is intentionally a single HTML file. When contributing:
- **DO** add features inline in the HTML
- **DO** use CDN libraries when needed
- **DON'T** add a build process
- **DON'T** split into separate files (defeats the purpose)

#### API Integration

The app supports two modes:

**Mode 1: claude.ai (no API key)**
```javascript
headers: {
  "anthropic-dangerous-direct-browser-calls": "true"
}
```

**Mode 2: Local (with API key)**
```javascript
headers: {
  "x-api-key": userProvidedKey,
  "anthropic-version": "2023-06-01"
}
```

Ensure your changes work in both modes.

#### PDF Export

When modifying PDF export:
- Test with briefs of different lengths
- Ensure special characters are handled (see `cleanForPDF()` function)
- Verify page breaks work correctly
- Check that all fonts render properly

### Code of Conduct

- Be respectful and constructive
- Welcome newcomers
- Focus on the problem, not the person
- Assume good intentions

### Questions?

Open an issue with the `question` label or reach out to the maintainers.

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

Thank you for making Readie better! 🚀
