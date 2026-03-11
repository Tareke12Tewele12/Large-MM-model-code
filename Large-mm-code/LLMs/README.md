

A command line tool and Python package that enables interaction with many Large Language Models such as **OpenAI**, **Anthropic Claude**, **Google Gemini**, **Meta Llama**, and numerous others. It supports both remote API based models and models that can run locally on your own computer.

You can watch the demo **Language models on the command line** on YouTube or read the detailed accompanying notes for a deeper explanation.

Using this tool, you can:

* Execute prompts directly from the command line
* Save prompts and responses in an SQLite database
* Create and store vector embeddings
* Extract structured information from text and images
* Enable models to use external tools
* And many additional capabilities

### Quick Start

First install the tool using one of the following methods:

**Using pip**

```bash
pip install llm
```

**Using Homebrew**

```bash
brew install llm
```

**Using pipx**

```bash
pipx install llm
```

**Using uv**

```bash
uv tool install llm
```

If you already have an OpenAI API key, configure it and run a prompt:

```bash
llm keys set openai
llm "Ten fun names for a pet pelican"
```

Example tasks you can perform:

Extract text from an image:

```bash
llm "extract text" -a scanned-document.jpg
```

Explain code from a file:

```bash
cat myfile.py | llm -s "Explain this code"
```

### Using Other Models

You can also connect to other providers through plugins.

**Google Gemini**

```bash
llm install llm-gemini
llm keys set gemini
llm -m gemini-2.0-flash "Tell me fun facts about Mountain View"
```

**Anthropic Claude**

```bash
llm install llm-anthropic
llm keys set anthropic
llm -m claude-4-opus "Impress me with wild facts about turnips"
```

### Running Local Models

You can run models locally using plugins such as Ollama.

```bash
llm install llm-ollama
ollama pull llama3.2:latest
llm -m llama3.2:latest "What is the capital of France?"
```

### Interactive Chat

To start an interactive conversation with a model:

```bash
llm chat -m gpt-4.1
```

The chat interface allows you to type prompts, edit them, or input multiple lines before sending them to the model.

---
