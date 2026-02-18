# AI Orchestrator - Multi-Model AI Assistant

<p align="center">
  <img src="media/icon.png" alt="AI Orchestrator Logo" width="128" height="128">
</p>

<p align="center">
  <strong>Intelligently orchestrate multiple AI models for complex development tasks</strong>
</p>

<p align="center">
  <a href="https://marketplace.visualstudio.com/items?itemName=debugger-lab.ai-orchestrator">
    <img src="https://img.shields.io/visual-studio-marketplace/v/debugger-lab.ai-orchestrator?style=flat-square&logo=visual-studio-code&logoColor=white&label=VS%20Marketplace&color=7c3aed" alt="VS Marketplace Version">
  </a>
  <a href="https://marketplace.visualstudio.com/items?itemName=debugger-lab.ai-orchestrator">
    <img src="https://img.shields.io/visual-studio-marketplace/i/debugger-lab.ai-orchestrator?style=flat-square&logo=visual-studio-code&logoColor=white&label=Installs&color=10a37f" alt="Installs">
  </a>
  <a href="https://marketplace.visualstudio.com/items?itemName=debugger-lab.ai-orchestrator">
    <img src="https://img.shields.io/visual-studio-marketplace/r/debugger-lab.ai-orchestrator?style=flat-square&logo=visual-studio-code&logoColor=white&label=Rating&color=f59e0b" alt="Rating">
  </a>
  <a href="https://github.com/debugger-lab/ai-orchestrator-vscode/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/debugger-lab/ai-orchestrator-vscode?style=flat-square&color=4285f4" alt="License">
  </a>
</p>

<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-installation">Installation</a> •
  <a href="#%EF%B8%8F-configuration">Configuration</a> •
  <a href="#-usage">Usage</a> •
  <a href="#-support">Support</a>
</p>

---

## 🎯 Why AI Orchestrator?

Stop switching between ChatGPT, Claude, and other AI assistants. **AI Orchestrator** automatically routes your tasks to the most suitable AI model and consolidates results into a unified output.

> **The Problem:** Different AI models excel at different tasks. GPT-4 is great for architecture, Claude excels at coding, Gemini shines at reasoning.
>
> **The Solution:** AI Orchestrator automatically detects your task type and routes it to the best model—or uses multiple models in parallel for complex tasks.

---

## ✨ Features

### 🤖 Multi-Model Support

| Provider | Model | Best For |
|----------|-------|----------|
| **OpenAI** | GPT-4, GPT-4 Turbo, GPT-4o | Architecture, Documentation, Roadmaps |
| **Anthropic** | Claude 3 Opus/Sonnet/Haiku | Coding, Implementation, Debugging |
| **Google** | Gemini Pro, Gemini 1.5 | Reasoning, Analysis, Trade-offs |
| **Moonshot** | Kimi 8k/32k/128k | Code Review, Security Audits |

### 🎯 Intelligent Task Routing

The extension automatically analyzes your task and routes it to specialized models:

```
📝 "Design a REST API for user auth" → OpenAI (Architecture)
💻 "Implement JWT token validation" → Claude (Coding)
🔍 "Review this code for security" → Kimi (Code Review)
🧠 "Compare microservices vs monolith" → Gemini (Reasoning)
```

### 🖥️ Modern Chat Interface

- **Sidebar Panel**: Chat-like interface for entering tasks
- **Real-time Progress**: See which models are working
- **Syntax Highlighting**: Beautiful code formatting in results
- **Task History**: Browse, re-run, and export past tasks

### ⚡ Powerful Commands

| Command | Description | Shortcut |
|---------|-------------|----------|
| `AI Orchestrator: Run Task` | Submit a new task | `Ctrl+Shift+P` |
| `AI Orchestrator: Configure` | Set up API keys | `Ctrl+Shift+P` |
| `AI Orchestrator: Check Status` | View model status | `Ctrl+Shift+P` |
| `Send to AI Orchestrator` | Process selected code | Right-click |

### 📝 Context Menu Integration

Select any code in the editor and right-click to:
- 🔍 **Review** code quality and best practices
- 🐛 **Debug** and identify issues
- ♻️ **Refactor** and improve structure
- 📚 **Document** with comments and docs
- 💡 **Explain** complex logic

---

## 📦 Installation

### From VS Code Marketplace

1. Open VS Code
2. Go to Extensions (`Ctrl+Shift+X` / `Cmd+Shift+X`)
3. Search for **"AI Orchestrator"**
4. Click **Install**

### From VSIX File

1. Download the `.vsix` file from [Releases](https://github.com/debugger-lab/ai-orchestrator-vscode/releases)
2. In VS Code, go to Extensions
3. Click `...` → **"Install from VSIX..."**
4. Select the downloaded file

---

## ⚙️ Configuration

### Setting Up API Keys

1. Open Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`)
2. Run **"AI Orchestrator: Configure"**
3. Select your AI provider
4. Enter your API key

> 🔐 **Security**: API keys are stored securely using VS Code's Secrets API. They are never transmitted to third parties or stored in plain text.

### Getting API Keys

| Provider | Get Key | Pricing |
|----------|---------|---------|
| OpenAI | [platform.openai.com](https://platform.openai.com/api-keys) | Pay-per-use |
| Anthropic | [console.anthropic.com](https://console.anthropic.com/) | Pay-per-use |
| Google | [makersuite.google.com](https://makersuite.google.com/app/apikey) | Free tier available |
| Moonshot | [platform.moonshot.cn](https://platform.moonshot.cn/) | Pay-per-use |

### Settings Reference

```json
{
  // Model Selection
  "aiOrchestrator.openai.model": "gpt-4",
  "aiOrchestrator.anthropic.model": "claude-3-opus-20240229",
  "aiOrchestrator.gemini.model": "gemini-pro",
  "aiOrchestrator.moonshot.model": "moonshot-v1-8k",
  
  // Task Routing Preferences
  "aiOrchestrator.routing.preferredArchitectureModel": "openai",
  "aiOrchestrator.routing.preferredCodingModel": "anthropic",
  "aiOrchestrator.routing.preferredReasoningModel": "gemini",
  "aiOrchestrator.routing.preferredReviewModel": "moonshot",
  
  // UI Options
  "aiOrchestrator.ui.showDetailedProgress": true,
  "aiOrchestrator.history.maxItems": 50
}
```

---

## 🚀 Usage

### Example 1: Complex Multi-Model Task

**Task:** *"Design and implement a REST API for user authentication with JWT tokens"*

The orchestrator will:
1. 🏗️ **OpenAI** designs API architecture and endpoints
2. 💻 **Claude** implements the authentication code
3. 🔍 **Kimi** reviews for security vulnerabilities

### Example 2: Code Review

```typescript
// Select this code, right-click → "Send to AI Orchestrator"
function processUserInput(input) {
  eval(input);  // 😱 Security issue!
  return db.query("SELECT * FROM users WHERE name = '" + input + "'");
}
```

**Result:** Comprehensive security review identifying SQL injection and code injection vulnerabilities.

### Example 3: Architecture Decision

**Task:** *"Compare microservices vs monolithic architecture for a startup with 5 developers"*

**Result:** Detailed analysis with trade-offs, recommendations, and migration considerations from Gemini.

---

## 📊 Task History

The History panel shows all your past orchestrations:

- **📋 View** past results anytime
- **🔄 Re-run** tasks with one click
- **📤 Export** results to Markdown
- **🗑️ Clear** history when needed

---

## 🔒 Privacy & Security

- ✅ API keys stored using VS Code's secure Secrets API
- ✅ Keys never stored in plain text or settings files
- ✅ Direct API calls to AI providers (no intermediaries)
- ✅ No telemetry or usage data collection
- ✅ Open source and auditable

---

## 🐛 Troubleshooting

### "No AI models available"
→ Configure at least one API key using **"AI Orchestrator: Configure"**

### Model not responding
→ Check your API key validity and account credits/quota

### Task taking too long
→ Complex multi-model tasks may take 30-60 seconds. Check the status bar for progress.

---

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

- 🐛 [Report bugs](https://github.com/debugger-lab/ai-orchestrator-vscode/issues/new?labels=bug)
- 💡 [Request features](https://github.com/debugger-lab/ai-orchestrator-vscode/issues/new?labels=enhancement)
- 📖 [Improve docs](https://github.com/debugger-lab/ai-orchestrator-vscode/pulls)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 💬 Support

- **📧 Email**: [support@debuggerlab.com](mailto:support@debuggerlab.com)
- **🐛 Issues**: [GitHub Issues](https://github.com/debugger-lab/ai-orchestrator-vscode/issues)
- **💬 Discussions**: [GitHub Discussions](https://github.com/debugger-lab/ai-orchestrator-vscode/discussions)

---

<p align="center">
  <strong>Made with ❤️ by <a href="https://debuggerlab.com">Debugger Lab</a></strong>
</p>

<p align="center">
  <sub>© 2026 Debugger Lab. All rights reserved.</sub>
</p>
