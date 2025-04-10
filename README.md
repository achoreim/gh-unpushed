# gh-unpushed
A GitHub CLI extension that shows your unpushed Git commits.

## Description
`gh-unpushed` is a simple extension for the GitHub CLI that shows which commits on your current branch haven't been pushed to the remote repository yet. This helps you keep track of local work that hasn't been shared with your team.

## Installation
To install this extension:
```bash
gh extension install achoreim/gh-unpushed
```

## Usage
```bash
gh unpushed [options] [remote]
```

### Parameters
- `remote`: (Optional) The name of the remote to compare against. Default: `origin` (or your configured default)

### Options
- `--remote, -r <remote>`: Override the default remote for this run
- `--set-remote, -sr <remote>`: Set a new default remote for future runs
- `--help, -h`: Show help message

### Examples
Check unpushed commits to the default remote:
```bash
gh unpushed
```

Check unpushed commits to a specific remote:
```bash
gh unpushed upstream
```
Or:
```bash
gh unpushed --remote upstream
```

Set a new default remote:
```bash
gh unpushed --set-remote upstream
```

## Output
The extension will display:
- A success message if there are no unpushed commits
- A list of unpushed commits with their hash, date, and commit message if there are any
- An error message if you're not on a branch or if the remote branch doesn't exist

## Example Output
```
🚀 Unpushed commits on 'feature' (not yet pushed to 'origin/feature'):

• 1a2b3c4 2025-04-09 12:30:00 Fixed critical bug in data fetching routine
• 5d6e7f8 2025-04-09 10:15:00 Added new logging functionality

```

## Configuration
The extension stores your default remote preference in `~/.gh-unpushed-config`. This configuration can be changed using the `--set-remote` option.

## Requirements
- [GitHub CLI](https://cli.github.com/) must be installed
- Git must be installed

## Development
To contribute to this extension:
1. Clone the repository
   ```bash
   git clone https://github.com/achoreim/gh-unpushed.git
   cd gh-unpushed
   ```
2. Make the script executable
   ```bash
   chmod +x gh-unpushed
   ```
3. Create a symbolic link to make it available in your PATH
   ```bash
   gh extension install .
   ```

## License
[MIT License](LICENSE)

## Author
Created by [@achoreim](https://github.com/achoreim)