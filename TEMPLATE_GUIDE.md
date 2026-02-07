# Oxide Port Template

This template provides a consistent structure for creating new oxide ports. Follow these steps to create a new port:

## 1. Copy Template

```bash
cp -r template/ your-new-port-name/
cd your-new-port-name/
```

## 2. Replace Placeholders

Replace the following placeholders in `README.md`:

### Required Replacements

- `[PORT_NAME]` → Your port name (e.g., `vscode`, `alacritty`, `zed`)
- `[PORT_CREATOR]` → Your GitHub username (e.g., `jakmaz`)
- `[TOOL_NAME]` → The tool's display name (e.g., `VS Code`, `Alacritty`, `Zed`)
- `[TOOL_DESCRIPTION]` → Brief description (e.g., `your code editor`, `your terminal`, `your editor`)
- `[TOOL_WEBSITE]` → Official tool website (e.g., `https://code.visualstudio.com/`)
- `[TOOL_LOGO]` → Logo name for shields.io (e.g., `visualstudiocode`, `alacritty`)

### Configuration-Specific Replacements

- `[CONFIG_PATH]` → Where config files go (e.g., `~/.config/alacritty/themes/`)
- `[CONFIG_FILE_PATH]` → Main config file location (e.g., `~/.config/alacritty/alacritty.toml`)
- `[config_format]` → Config file format (e.g., `toml`, `json`, `yaml`)

## 3. Customize Sections

### Installation Methods

- Update installation sections with tool-specific instructions
- Remove unused installation methods
- Add tool-specific package manager instructions if applicable

### Configuration Examples

- Replace placeholder config examples with actual syntax
- Add tool-specific configuration options
- Include any special setup steps

### Tool-Specific Features

- Add sections for tool-specific features (plugins, extensions, etc.)
- Include any advanced configuration options
- Document tool-specific color usage

## 4. Optional Enhancements

### Screenshots

- Add preview images in `assets/` directory
- Uncomment the screenshot section in the README
- Use consistent screenshot style across ports

### Additional Badges

- Add version badge if releases are available
- Add download count badge if applicable
- Keep consistent with existing oxide ports

## Example Replacements

For an Alacritty port:

```text
[PORT_NAME] → alacritty
[TOOL_NAME] → Alacritty  
[TOOL_DESCRIPTION] → your terminal
[TOOL_WEBSITE] → https://alacritty.org/
[TOOL_LOGO] → alacritty
[CONFIG_PATH] → ~/.config/alacritty/themes/
[CONFIG_FILE_PATH] → ~/.config/alacritty/alacritty.toml
[config_format] → toml
```

## 5. Create Repository

1. Initialize git repository
2. Add your theme files
3. Commit and push to GitHub under oxidescheme organization
4. Ensure consistent branding across all oxide ports

## Color Consistency

Always use the oxide OKLCH color palette:

- Background: `#161616`
- Foreground: `#cecece`
- Accent colors: Use semantic colors from oxide.nvim/lua/oxide/colors.lua

## Maintain Philosophy

Remember oxide's core principles:

- Function first
- Visual silence  
- Calculated colors
- Minimalist approach

