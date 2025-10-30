# Botpress Agent Development Kit (ADK)

The Botpress Agent Development Kit (ADK) is a high-level TypeScript framework for building AI agents on the Botpress platform.

### Quick Install

**macOS & Linux**
```bash
curl -fsSL https://github.com/botpress/adk/releases/latest/download/install.sh | bash
```

**Windows (PowerShell)**
```powershell
powershell -c "irm https://github.com/botpress/adk/releases/latest/download/install.ps1 | iex"
```

### Manual Installation

<details>
<summary>Click to expand manual install instructions</summary>

**macOS (Apple Silicon)**
```bash
curl -fsSL https://github.com/botpress/adk/releases/download/v1.4.2/adk-darwin-arm64.tar.gz | tar -xz
sudo mv adk-darwin-arm64 /usr/local/bin/adk
adk --version
```

**macOS (Intel)**
```bash
curl -fsSL https://github.com/botpress/adk/releases/download/v1.4.2/adk-darwin-x64.tar.gz | tar -xz
sudo mv adk-darwin-x64 /usr/local/bin/adk
adk --version
```

**Linux (x64)**
```bash
curl -fsSL https://github.com/botpress/adk/releases/download/v1.4.2/adk-linux-x64.tar.gz | tar -xz
sudo mv adk-linux-x64 /usr/local/bin/adk
adk --version
```

**Windows (Manual)**
```powershell
Invoke-WebRequest -Uri "https://github.com/botpress/adk/releases/download/v1.4.2/adk-windows-x64.zip" -OutFile "adk.zip"
Expand-Archive -Path "adk.zip" -DestinationPath "$env:LOCALAPPDATA\Programs\adk"
$env:PATH += ";$env:LOCALAPPDATA\Programs\adk"
[Environment]::SetEnvironmentVariable("PATH", $env:PATH, "User")
adk --version
```

</details>

### Getting Started

```bash
# 1. Install ADK
curl -fsSL https://github.com/botpress/adk/releases/latest/download/install.sh | bash

# 2. Create and set up your agent
adk init my-agent

# What this does:
# - Prompts you to log in (if not already authenticated)
# - Lets you choose a template:
#   • Blank: Empty agent with no pre-configured integrations
#   • Hello World: Starter agent with chat and webchat ready to use
# - Lets you select your package manager (npm / pnpm / bun)
# - Automatically installs all dependencies
# - Automatically links your agent to Botpress

# 3. Navigate to your agent directory
cd my-agent

# 4. (Optional) Add integrations as needed
adk add linear
...

# 5. Start local development server
adk dev

# 6. (Optional) Test your agent in the terminal
adk chat
# Run this in a new terminal while 'adk dev' is running

```

### Documentation

- [ADK Documentation](https://botpress.com/docs/adk)
- [Botpress Platform](https://botpress.com)
