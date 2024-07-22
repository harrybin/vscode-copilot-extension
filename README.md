# Copilot with Issues

This an Visual Studio Code Extension enriching copilot with the option to reference GitHub issues.

## Usage

For referencing a GitHub Issue use the the `/issue` command and prepend an exclamationmark followed by the issue nummeber in your prompt: `!<issueNumber>`

E.g.

> /issue provide a implementation suggestion for solving **!1234** in C#

When appending a `+` to the issue reference beside the issue description also all issue comments will be passed to copilot: `!<issueNumber>+`
E.g.

> /issue provide a implementation suggestion for solving **!1234+** in C#

Using `gh:<owner>/<repo>` you can specify the organization and repo you like to refer to, in case it's not the owner and repo of you current code context.

## Running the extension

- Run `npm install` in terminal to install dependencies
- Run the `Run Extension` target in the Debug View. This will:
  - Start a task `npm: watch` to compile the code
  - Run the extension in a new VS Code window

### Known issues

- if your VS-Code is not in the context of a git repo you will get the error:
  > ❌ fatal: not a git repository (or any of the parent directories): .git

## Inspiration

This Extension is based on the chat sample of [vscode extension guides](https://github.com/microsoft/vscode-extension-samples/tree/main/chat-sample)
documented [here](https://code.visualstudio.com/api/extension-guides/chat)

### Authors
This vs-code copilot extension is created and maintained by [Nico Orschel](https://github.com/norschel) and [Harald Binkle](https://github.com/harrybin)
