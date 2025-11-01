# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a research/laboratory repository for comparing ESLint/Prettier with Biome in Next.js projects. The repository name "lab-202511-biome" indicates this is a November 2025 lab project focused on Biome evaluation.

## Repository Structure

- `documents/` - Contains Japanese documentation outlining the research plan
  - `001_進行.md` - Main progress/planning document with numbered research steps
  - `901_参考リンク.md` - Reference links (Biome official docs)
- `next_biome/` - Empty directory (likely for Next.js project with Biome)
- `next_eslint/` - Empty directory (likely for Next.js project with ESLint/Prettier)

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

## Working with this Repository

When asked to set up or create projects in this repository:

- `next_biome/` should contain a Next.js project configured with Biome
- `next_eslint/` should contain a Next.js project configured with ESLint/Prettier
- Both directories will likely be created via `npx create-next-app@latest` or similar commands
- Pay attention to biome.json, .eslintrc, .prettierrc configuration files when they are created

## Language Note

Documentation is in Japanese. When working with this repository, be prepared to:
- Read and understand Japanese documentation
- Create or modify Japanese documentation if requested
- Keep consistent with the existing documentation language
