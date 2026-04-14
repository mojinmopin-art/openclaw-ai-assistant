# OpenClaw AI Assistant - 个人AI助手插件

[![Official Site](https://img.shields.io/badge/Official_Site-opeclaw.info-brightgreen)](https://opeclaw.info)
[![Version](https://img.shields.io/badge/Version-2026.4-blue)]()
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

OpenClaw is an AI-powered personal assistant plugin that integrates with your browser to provide context-aware AI assistance for writing, coding, research, and daily tasks.

## Features

- **Context-Aware Chat**: AI understands the current webpage context for better responses
- **Writing Assistant**: Grammar check, rewrite, summarize, and translate selected text
- **Code Helper**: Explain code snippets, suggest fixes, and generate boilerplate
- **Research Mode**: Summarize articles, extract key points, and generate citations
- **Quick Actions**: Keyboard shortcuts for common AI tasks (⌘+Shift+A)

## Supported Platforms

| Browser | Version | Status |
|---------|---------|--------|
| Chrome | 120+ | ✅ Full support |
| Edge | 119+ | ✅ Full support |
| Firefox | 122+ | ✅ Full support |
| Arc | Latest | ✅ Compatible |

## Getting Started

1. Download from [opeclaw.info](https://opeclaw.info)
2. Install the browser extension
3. Press `⌘+Shift+A` (Mac) or `Ctrl+Shift+A` (Windows) to activate
4. Start chatting with your AI assistant

## Use Cases

### Writing Enhancement
Select any text on a webpage → Right-click → OpenClaw → Choose action:
- **Rewrite**: Improve clarity and tone
- **Summarize**: Condense long paragraphs
- **Translate**: Instant translation to 20+ languages
- **Explain**: Simplify complex text

### Code Assistance
Works on GitHub, StackOverflow, CodePen, and any page with code:
- Explain code blocks in plain language
- Suggest performance improvements
- Convert between programming languages
- Generate unit test templates

### Research & Study
- Summarize academic papers and articles
- Extract and organize key arguments
- Generate APA/MLA citations automatically
- Create study notes from web content

## Technical Architecture

```
User Input (text selection / chat)
    ↓
Context Extraction (DOM analysis of current page)
    ↓
Prompt Construction (context + user intent + history)
    ↓
AI Engine (configurable: GPT-4 / Claude / local models)
    ↓
Response Rendering (markdown → formatted overlay)
```

Key design principles:
- **Privacy-first**: Page content is processed locally; only the constructed prompt is sent to the AI provider
- **Model-agnostic**: Bring your own API key, supports multiple AI providers
- **Lightweight**: Core extension is <500KB, no heavy dependencies

## Known Issues

### Extension icon not appearing after install
Chrome 125+ requires manual pin:
1. Click the puzzle icon (Extensions) in toolbar
2. Find OpenClaw and click the pin icon

### Slow response on long pages
Context extraction on pages with 10,000+ DOM nodes may take 2-3 seconds. We're optimizing the DOM parser for v2.1.

### API key configuration
If you see "API key not configured":
1. Click OpenClaw icon → Settings
2. Enter your AI provider API key
3. Select your preferred model

For detailed setup guides, visit [opeclaw.info](https://opeclaw.info).

## Contributing

We welcome contributions! See [Issues](../../issues) for current tasks.

## License

MIT License - see [LICENSE](LICENSE) for details.

---
*Full documentation, API key setup guide, and feature demos at [opeclaw.info](https://opeclaw.info)*
