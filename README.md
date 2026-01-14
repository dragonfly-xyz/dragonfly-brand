# Dragonfly Brand Plugin for Claude Code

Official Dragonfly brand style guidelines for Claude Code. This plugin provides the `dragonfly-style` skill for applying Dragonfly branding to documents, websites, CSS, and digital materials.

## Installation

**Step 1: Add the marketplace**
```
/plugin marketplace add https://github.com/dragonfly-xyz/dragonfly-brand.git
```

**Step 2: Install the plugin**
```
/plugin install dragonfly-brand@dragonfly-brand
```

Or browse available plugins:
```
/plugin
```
Then select "Discover" to find and install the dragonfly-brand plugin.

## What's Included

### Skill: `dragonfly-style`

Automatically activated when you ask Claude to:
- Style content with Dragonfly branding
- Create Dragonfly-styled UI
- Get color/typography/logo specs

### Brand Assets

**Fonts** (`plugins/dragonfly-brand/skills/dragonfly-style/assets/fonts/`)
- `NONNaturalGrotesk-Regular.woff2`
- `NONNaturalGrotesk-Bold.woff2`
- `NONNaturalMono-Light.woff2`

**Logos** (`plugins/dragonfly-brand/skills/dragonfly-style/assets/logos/`)
- Logomark (light/dark)
- Wordmark (light/dark)
- Full logo (light/dark)
- ASCII variants

## Brand Quick Reference

| Element | Value |
|---------|-------|
| **Primary Black** | `#000000` |
| **Grey** | `#F2F2F2` |
| **Dragon Blood Orange** | `#FA4C14` |
| **Primary Font** | Non Natural Grotesk |
| **Mono Font** | Non Natural Mono |

## Usage

Once installed, simply ask Claude to apply Dragonfly styling:

- "Style this landing page with Dragonfly branding"
- "What are the Dragonfly brand colors?"
- "Create a Dragonfly-styled button component"

Claude will automatically use the brand guidelines and can copy font/logo assets to your project.

## License

Internal use only - Dragonfly brand assets are proprietary.
