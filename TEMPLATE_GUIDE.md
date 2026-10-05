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

Show oxide in normal use, with readable content that demonstrates the port's colors and UI.

To make a preview:

1. Apply oxide in the app and arrange the content you want to show.
2. Use a window size that fits the app's layout. **1200 × 750** is a suggested starting point.
3. Capture the app window with your preferred screenshot tool, keeping the native shadow on a transparent background when available.
4. Save the PNG as `assets/preview.png`. Keep the capture's native resolution; shadow margins and display scaling affect the final pixel dimensions. Avoid stretching or upscaling it.
5. Uncomment the screenshot block in `README.md` and check that its filename matches the saved image exactly.
6. Check the rendered README at normal reading width. Increase the app's font size and recapture if the text becomes too small.

Choose content that fits the tool:

- **Terminals:** A shell prompt, representative command output, and a compact ANSI color palette.
- **Editors:** Syntax-highlighted code with useful UI visible. Completion, search, or diagnostics can have separate screenshots when they show something distinct.
- **Terminal apps:** The tool's own panels with useful content, such as a diff in Lazygit or files and a preview in Yazi.
- **Notes and chat apps:** Sample notes or conversations that show text hierarchy and relevant controls.
- **Userstyles:** A representative page for each supported website.

Use sample content without private information. Hide unrelated windows, notifications, and unused panels. Avoid empty dashboards, excessive blank space, decorative backdrops, and annotations. Keep framing and font scale consistent across ports.

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

### UI Color Usage

**Read `oxide/UI_COLOR_GUIDE.md` before writing any theme files.** This guide explains:
- The monochrome-first philosophy for UI chrome
- When accents are appropriate (errors, success, warnings, active states)
- How to map oxide colors to UI elements (borders, selections, tabs, etc.)

Do not infer UI usage from `colors.lua` comments — those describe syntax highlighting, not UI chrome.

## Maintain Philosophy

Remember oxide's core principles:

- Function first
- Visual silence
- Calculated colors
- Minimalist approach
- Monochrome-first UI, accents for semantic meaning only
