# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a research/laboratory repository for comparing ESLint/Prettier with Biome in Next.js projects. The repository name "lab-202511-biome" indicates this is a November 2025 lab project focused on Biome evaluation.

## Repository Structure

- `documents/` - Contains Japanese documentation outlining the research plan
  - `001_進行.md` - Main progress/planning document with numbered research steps
  - `901_参考リンク.md` - Reference links (Biome official docs)
- `next_biome/` - Next.js 16 project configured with Biome
- `next_eslint/` - Next.js 16 project configured with ESLint/Prettier

## Project Configurations

### next_eslint (ESLint/Prettier Baseline)

**Key Configuration Files:**
- `eslint.config.mjs` - ESLint flat config using `eslint-config-next` (both core-web-vitals and typescript presets)
- `.prettierrc` - Prettier config with 4-space indentation, semicolons, double quotes, and ES5 trailing commas
- `package.json` - Scripts include `lint` (runs eslint) and `format` (runs prettier --write)

**Development Commands:**
```bash
cd next_eslint
npm run dev      # Start dev server on http://localhost:3000
npm run build    # Build for production
npm run lint     # Run ESLint
npm run format   # Format with Prettier
```

### next_biome (Biome Configuration)

**Key Configuration Files:**
- `biome.json` - Biome config with VCS integration, 2-space indentation, recommended React/Next.js rules, and import organization
- `package.json` - Scripts include `lint` (runs biome check) and `format` (runs biome format --write)

**Development Commands:**
```bash
cd next_biome
npm run dev      # Start dev server on http://localhost:3000
npm run build    # Build for production
npm run lint     # Run Biome check (lint + format check)
npm run format   # Format with Biome
```

**Notable Biome Configuration:**
- VCS integration enabled with git ignore file support
- React and Next.js domains set to "recommended"
- Auto-organize imports enabled
- `noUnknownAtRules` disabled for CSS compatibility

## Configuration Comparison

### Formatting Differences
- **Indentation:** ESLint project uses 4 spaces (Prettier), Biome project uses 2 spaces
- **Quote Style:** ESLint project uses double quotes (Prettier), Biome uses default (double quotes)
- **Trailing Commas:** ESLint project uses ES5 (Prettier), Biome uses default

### Linting Approach
- **ESLint:** Uses Next.js's curated rule sets (core-web-vitals + typescript)
- **Biome:** Uses Biome's recommended rules + React/Next.js domain-specific rules

### Tooling Philosophy
- **ESLint/Prettier:** Two-tool approach (separate linter and formatter)
- **Biome:** Unified tool for both linting and formatting

## Research Plan Overview

The research plan (documents/001_進行.md) follows these phases:

1. **ESLint/Prettier baseline** - Document typical React/Next.js ESLint/Prettier configurations
2. **Biome defaults** - Understand Biome's default rules and behavior for React/Next.js
3. **Configuration mapping** - Learn how to replicate ESLint/Prettier settings in Biome
4. **Practical testing** - Test lint/format behavior changes with actual code
5. **Migration validation** - Compare migration from ESLint/Prettier to Biome
6. **Setup experience** - Compare `biome init` with Next.js v16 template generation
7. **VS Code integration** - Configure editor settings and handle conflicts
8. **CI integration** - Set up GitHub Actions for format/lint checks
9. **Documentation review** - Review VCS integration, migration guides, and Next.js-specific considerations

## Language Note

Documentation is in Japanese. When working with this repository:
- Read and understand Japanese documentation in `documents/`
- Create or modify Japanese documentation if requested
- Keep consistent with the existing documentation language
