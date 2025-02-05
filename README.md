# 9-gigifty-shared

Why do we need a helper library? 
To avoid duplicate codes accross microservices

- Helpers consist of interfaces that come from all microservices.
- Cloudinary upload methods that will be used to upload images.
- Error handlers
- The API gateway middleware will contain a token that contains a value that the microservice will check to see if it contains a particular value that it requires, or for the microservices to check if the request is actually coming from the API gateway.
- Logger methods
- Helper methods

### 🔧 Configuration (Setting Environment Variables)

When working with private npm packages or GitHub Package Registry, you need to set the `NPM_TOKEN` environment variable for authentication.

#### 🖥 Windows (PowerShell)

To set the `NPM_TOKEN` environment variable permanently on Windows, run the following command in PowerShell:

```powershell
[System.Environment]::SetEnvironmentVariable("NPM_TOKEN", "your-token-here", "User")
```

This will store the variable at the user level, making it available for all terminal sessions.

To verify the variable, run:

Powershell:

```bash
echo $env:NPM_TOKEN
```

🍏 macOS / 🐧 Linux (Bash, Zsh)
To set the NPM_TOKEN environment variable temporarily in Bash or Zsh, run:

```bash
export NPM_TOKEN=your-token-here
```

This will only be valid for the current terminal session.

To make it persistent, add the following line to your ~/.bashrc, ~/.zshrc, or ~/.bash_profile file:

```bash
echo 'export NPM_TOKEN=your-token-here' >> ~/.bashrc
```

Then reload the shell configuration:

```bash
source ~/.bashrc  # or source ~/.zshrc
```

🗑 Removing the Environment Variable
Windows (PowerShell)

```bash
[System.Environment]::SetEnvironmentVariable("NPM_TOKEN", $null, "User")
```

macOS/Linux

```bash
unset NPM_TOKEN
```

Now your environment is configured correctly for authentication with private npm packages! 🚀

