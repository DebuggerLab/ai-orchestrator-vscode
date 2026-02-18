# AI Orchestrator - VS Code Extension

![AI Orchestrator](media/icon.png)

**Intelligently orchestrate multiple AI models for complex development tasks**

AI Orchestrator automatically routes your tasks to the best-suited AI models (ChatGPT, Claude, Gemini, Kimi) based on task type, then consolidates the results into a unified output.

## ✨ Features

### 🤖 Multi-Model Orchestration
- **OpenAI (ChatGPT)**: Architecture design, roadmaps, and documentation
- **Anthropic (Claude)**: Coding implementation and debugging
- **Google Gemini**: Reasoning, logic, and analysis
- **Moonshot (Kimi)**: Code review and security audits

### 🎯 Smart Task Routing
The extension automatically detects what type of task you're performing and routes it to the specialized model:

| Task Type | Primary Model | Description |
|-----------|--------------|-------------|
| Architecture | OpenAI | System design, schemas, APIs |
| Coding | Claude | Implementation, functions, classes |
| Reasoning | Gemini | Analysis, trade-offs, decisions |
| Code Review | Kimi | Quality, security, best practices |

### 🖥️ User Interface

#### Sidebar Chat Panel
- Modern chat-like interface for entering tasks
- Quick action buttons for common operations
- Real-time progress updates showing active models
- Formatted results with syntax highlighting

#### Task History
- Browse and search past orchestrations
- Re-run previous tasks with one click
- Export results to Markdown

#### Status Bar
- Always visible orchestrator status
- Quick access to configuration and status info

### ⚡ Commands

Access these from the Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`):

| Command | Description |
|---------|-------------|
| `AI Orchestrator: Run Task` | Enter a new task to orchestrate |
| `AI Orchestrator: Configure` | Set up API keys and preferences |
| `AI Orchestrator: Check Status` | View configured models and statistics |

### 📝 Context Menu

Select any code in the editor, right-click, and choose **"Send to AI Orchestrator"** to:
- Review code quality
- Debug and fix issues
- Improve and refactor
- Generate documentation
- Get explanations

## 📦 Installation

### From VSIX
1. Download the `.vsix` file
2. In VS Code, go to Extensions (`Ctrl+Shift+X`)
3. Click the `...` menu → "Install from VSIX..."
4. Select the downloaded file

### From Marketplace
Search for "AI Orchestrator" in the VS Code Extensions marketplace.

## ⚙️ Configuration

### Setting Up API Keys

1. Open the Command Palette (`Ctrl+Shift+P`)
2. Run `AI Orchestrator: Configure`
3. Select the model provider to configure
4. Enter your API key (stored securely using VS Code's Secrets API)

You only need to configure the models you want to use. The orchestrator will automatically fall back to available models if your preferred model isn't configured.

### Settings

Configure model preferences in VS Code Settings (`Ctrl+,`):

```json
{
  "aiOrchestrator.openai.model": "gpt-4",
  "aiOrchestrator.anthropic.model": "claude-3-opus-20240229",
  "aiOrchestrator.gemini.model": "gemini-pro",
  "aiOrchestrator.moonshot.model": "moonshot-v1-8k",
  "aiOrchestrator.routing.preferredCodingModel": "anthropic",
  "aiOrchestrator.routing.preferredArchitectureModel": "openai",
  "aiOrchestrator.routing.preferredReasoningModel": "gemini",
  "aiOrchestrator.routing.preferredReviewModel": "moonshot",
  "aiOrchestrator.ui.showDetailedProgress": true,
  "aiOrchestrator.history.maxItems": 50
}
```

## 🚀 Usage Examples

### Example 1: Complex Task with Multiple Models

**Task:** "Design and implement a REST API for user authentication with JWT tokens"

The orchestrator will:
1. 🏗️ Use **OpenAI** for API architecture and endpoint design
2. 💻 Use **Claude** for implementing the authentication code
3. 🔍 Use **Kimi** for security review of the implementation

### Example 2: Code Review

**Task:** "Review this function for performance issues and security vulnerabilities"

```typescript
// Select this code and right-click → "Send to AI Orchestrator"
function processUserInput(input) {
  eval(input);  // 😱 Security issue!
  return database.query("SELECT * FROM users WHERE name = '" + input + "'");
}
```

### Example 3: Reasoning Task

**Task:** "Compare microservices vs monolithic architecture for a startup with 5 developers"

Gemini will analyze the trade-offs and provide a reasoned recommendation.

## 📊 Task History

The extension maintains a history of your orchestrated tasks. You can:

- **View** past results in the History panel
- **Re-run** tasks with a single click
- **Export** results to Markdown for documentation
- **Clear** history when needed

## 🔒 Security

- **API keys** are stored securely using VS Code's Secrets API
- Keys are **never** sent to third parties or stored in plain text
- All API calls go directly to the respective AI providers

## 🐛 Troubleshooting

### "No AI models available"
- Make sure you've configured at least one API key
- Run `AI Orchestrator: Configure` to set up your keys

### Model not responding
- Check your API key is valid
- Verify you have credits/quota with the provider
- Check your internet connection

### Task taking too long
- Complex tasks with multiple models may take 30-60 seconds
- Check the status bar for progress updates

## 📄 License

MIT License - see [LICENSE](LICENSE) for details.

## 🤝 Contributing

Contributions are welcome! Please read our contributing guidelines and submit pull requests to our GitHub repository.

## 📞 Support

- **Issues**: Report bugs on GitHub Issues
- **Discussions**: Join our GitHub Discussions for questions
- **Email**: support@ai-orchestrator.dev

---

**Made with ❤️ by the AI Orchestrator Team**
