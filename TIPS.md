# AI Coding Agent Setup & Tips

Quick reference for setting up and using various AI coding agents.

## Web-Based Agents

### General Logic & Reasoning

Best for architecture, debugging, and complex questions.

  * **Google Gemini:** [gemini.google.com](https://gemini.google.com/) (Large context window, good for pasting full files)
  * **ChatGPT (o1/4o):** [chatgpt.com](https://chatgpt.com/) (High reasoning capabilities)

### Full-Stack Generators

Browser-based environments that build full apps.

  * **Bolt:** [bolt.new](https://bolt.new/) (React/Vue/Svelte full-stack prototypes)
  * **v0:** [v0.dev](https://v0.dev/) (UI generation with Tailwind/Shadcn)

## Local GUI Agents (IDEs)

### Cursor

VS Code fork with deep AI integration.

  * **Download:** [cursor.com](https://www.cursor.com/)
  * **Setup:** Settings → Models → Add API keys (Anthropic/OpenAI/Google).
  * **Key Features:**
      * `Cmd+K`: Inline edits.
      * `Cmd+I` (Composer): Multi-file editing agent.
      * Context: Use `@Files`, `@Folders`, or `@Docs` to reference code.

### Kiro

Agentic IDE by AWS (VS Code compatible).

  * **Download:** [kiro.dev](https://kiro.dev/)
  * **Key Features:**
      * **Spec-Driven:** Generates `requirements.md` and `tasks.md` before coding.
      * **Hooks:** Triggers AI agents automatically on file save or creation.
      * **Modes:** Switch between "Vibe" (fast) and "Spec" (structured) modes.

### Windsurf

The "Flow" editor by Codeium.

  * **Download:** [windsurf.ai](https://windsurf.ai/)
  * **Key Features:** "Cascade" flow—the AI tracks cursor movement and terminal output to maintain deep context.

### GitHub Copilot

Standard extension for VS Code/JetBrains.

  * **Usage:** `Tab` to complete, `Cmd+I` for inline chat.
  * **Tip:** Write descriptive comments *before* function headers to guide generation.

### LM Studio

Run local models with a GUI (Offline).

  * **Download:** [lmstudio.ai](https://lmstudio.ai/)
  * **Usage:** Download models (Llama 3, DeepSeek) and run a local server compatible with OpenAI clients.

## Command-Line Agents

### Claude Code

Anthropic's official CLI agent (Beta).

```bash
npm install -g @anthropic/claude-code
claude
```

  * Authenticates directly with Anthropic console.
  * Performs architectural analysis and file management.

### Aider

Popular terminal pair programmer.

```bash
pip install aider-chat

# Run with Gemini (Efficient & Large Context)
export GEMINI_API_KEY=your_key
aider --model gemini/gemini-1.5-pro

# Run with Local Models
aider --model ollama/deepseek-coder-v2
```

  * **Commands:** `/add <file>` to track files, `/architect` for planning.
  * **Git:** Automatically commits changes with descriptive messages.

## Local Model Platforms

### Ollama

Backend to run models locally (Linux/Mac/Windows).

```bash
# Install
curl -fsSL https://ollama.com/install.sh | sh

# Pull models
ollama pull llama3.2
ollama pull deepseek-coder-v2
```

  * **Note:** Requires no internet, once installed; performance heavily depends on GPU.
  * **Integration:** Powers the backend for Continue.dev, Aider, and generic extensions.

## Using Tessl to Enhance Agent Context

Tessl provides usage specs (tiles) that give agents accurate, version-specific documentation.

**Setup:**

```bash
npm install -g @tessl/cli
tessl init
```

**Usage:**

1.  **Install tiles:** `tessl search react` or `tessl registry sync`
2.  **Prompt your agent:** "Build this using the installed usage specs for accurate API usage."

## General Prompting Tips

**Be specific:**

  * ✅ "I have a CSV with columns: date, merchant, amount, category"
  * ❌ "I have some transaction data"

**Describe the outcome:**

  * ✅ "Create a line chart showing spending trends over time, grouped by month"
  * ❌ "Make a chart"

**Specify technical details:**

  * ✅ "Use Recharts library, TypeScript, and Tailwind for styling"
  * ❌ "Use whatever you think is best"

**Iterate incrementally:**

  * ✅ "First let's get the data loading working, then we'll add visualizations"
  * ❌ "Build the entire dashboard in one go"

**Provide constraints:**

  * ✅ "This will run in the browser only, no backend available"
  * ❌ "Build a dashboard"
