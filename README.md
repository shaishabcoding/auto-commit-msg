# Auto Commit Message Generator

A shell script that automatically generates commit messages using AI (Gemini API) based on your git changes, then lets you confirm or cancel the commit.

**Author**: Shaishab Chandra Shil  
**GitHub**: [shaishabcoding](https://github.com/shaishabcoding)  
**CreateAt**: May 10, 2025 at 7:06 PM

## Features

- Automatically detects staged or unstaged changes
- Generates meaningful commit messages using Gemini AI
- Shows a preview of the generated message
- Interactive confirmation before committing
- Handles both staged and unstaged files
- Color-coded output for better visibility
- Environment variable configuration

## Requirements

- Git
- curl
- Gemini API key (free tier available)

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/shaishabcoding/auto-commit-msg.git
   ```

2. Navigate to the project directory:

   ```bash
   cd auto-commit-msg
   ```

3. Make the script executable:

   ```bash
   chmod +x commit.sh
   ```

4. Create a `.env` file in your project root and add your Gemini API key:
   ```env
   GEMINI_KEY=your_api_key_here
   ```

## Usage

### Basic Usage

Run the script when you have changes to commit:

```bash
./commit.sh
```

### Options

- If you have staged changes, it will use those for the commit message
- If you have unstaged changes, it will add all changes and then commit
- If no changes are detected, the script will exit

### Workflow

1. Stage your changes (or leave them unstaged)
2. Run the script
3. Review the generated commit message
4. Press:
   - `Enter` to confirm and commit
   - `Esc` to cancel

## Configuration

Customize the script by editing these variables in the script:

- `AI_API_ENDPOINT`: Change if you want to use a different Gemini model
- Color variables (`GREEN`, `RED`, etc.) for different output styles

## Example

<pre style="background-color:#1e1e2f; color:#ffffff; padding: 1rem; border-radius: 8px; font-family: monospace; line-height: 1.5;">
<span style="color:#8be9fd;">$ ./commit.sh</span>
<span style="color:#bd93f9;">Generated Commit Message:</span>
<span style="color:#50fa7b;">feat: Add README with installation, usage, and configuration instructions</span>

<span style="color:#50fa7b;">This commit introduces a README file that provides comprehensive documentation for the auto-commit-msg script, including installation steps, usage examples, configuration options, and troubleshooting tips. It also outlines the project's key features and contribution guidelines.</span>
<span style="color:#f1fa8c;">Press Enter to confirm the commit message or Esc to cancel.</span>
</pre>

## Troubleshooting

- **No changes detected**: Make sure you have either staged or unstaged changes
- **API errors**: Verify your Gemini API key is correct in `.env`
- **Permission denied**: Ensure the script is executable (`chmod +x commit.sh`)

## Contributing

Contributions are welcome! Please open an issue or pull request for any improvements.

## License

MIT

```

This README includes:
1. Project description
2. Key features
3. Installation instructions
4. Usage guide
5. Configuration options
6. Example output
7. Troubleshooting tips
8. Contribution guidelines
9. License information

You can customize any sections as needed for your specific project requirements.
```
