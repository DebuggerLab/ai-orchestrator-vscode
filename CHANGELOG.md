# Changelog

All notable changes to the **AI Orchestrator** extension will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-02-18

### 🎉 Initial Release

We're excited to announce the first public release of AI Orchestrator!

### ✨ Added

#### Core Features
- **Multi-Model Orchestration**: Support for OpenAI (GPT-4), Anthropic (Claude 3), Google (Gemini), and Moonshot (Kimi)
- **Intelligent Task Routing**: Automatic task detection and routing to specialized models
- **Parallel Execution**: Run multiple models simultaneously for complex tasks
- **Result Consolidation**: Unified output from multiple AI responses

#### User Interface
- **Sidebar Chat Panel**: Modern chat-like interface with real-time progress
- **Task History View**: Browse, re-run, and export past orchestrations
- **Status Bar Integration**: Quick access to orchestrator status
- **Syntax Highlighting**: Beautiful code formatting using highlight.js

#### Commands
- `AI Orchestrator: Run Task` - Submit a new task
- `AI Orchestrator: Configure` - Set up API keys
- `AI Orchestrator: Check Status` - View model status and statistics
- `AI Orchestrator: Clear History` - Clear task history
- `Send to AI Orchestrator` - Process selected code (context menu)

#### Configuration
- Model selection for each provider
- Task routing preferences
- UI customization options
- History management settings

#### Security
- Secure API key storage using VS Code Secrets API
- Direct API calls (no intermediary servers)
- Content Security Policy for webviews

### 🔧 Technical

- TypeScript implementation with full type safety
- Webview-based UI with modern CSS
- Support for VS Code 1.85.0+
- Compatible with Windows, macOS, and Linux

---

## [Unreleased]

### Planned Features
- [ ] Custom model endpoint support
- [ ] Conversation history within sessions
- [ ] Code insertion directly into editor
- [ ] Workspace-aware context
- [ ] Custom prompt templates

---

**Full Changelog**: https://github.com/debugger-lab/ai-orchestrator-vscode/commits/v1.0.0
