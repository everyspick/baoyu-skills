# Changelog

English | [中文](./CHANGELOG.zh.md)

<!-- Personal fork notes: I'm primarily using baoyu-diagram and baoyu-post-to-wechat skills -->
<!-- Personal note: baoyu-diagram SVG-to-PNG @2x conversion is super useful for Retina displays -->

## 1.108.0 - 2026-04-19

### Refactor
- Refactor skills into focused reference files for better maintainability
- Use npm packages for shared skill code across skills

## 1.107.0 - 2026-04-15

### Features
- `baoyu-diagram`: add SVG-to-PNG @2x conversion script — auto-converts generated SVG diagrams to @2x PNG using Sharp; consolidate reference files and add `{baseDir}` path resolution for portable skill loading

### Fixes
- `claude-plugin`: allow inline marketplace manifest (#130)

## 1.106.0 - 2026-04-14

### Features
- `baoyu-diagram`: add architecture enrichment rules — automatically expand architecture diagrams with multiple client types, per-service tech stacks, database tiers, message buses, and color-coded categories; add full structural layout patterns, architecture-specific pitfalls, network topology templates, and layout math for complex diagrams

## 1.105.0 - 2026-04-13

### Features
- `baoyu-diagram`: unify to analyze→confirm→generate workflow — remove single/multi mode split; skill now analyzes any input material, recommends diagram types and splitting strategy, confirms once, then generates all diagrams

## 1.104.0 - 2026-04-13

### Features
- `baoyu-diagram`: add Mermaid sketch step (6d-0) before SVG generation — write a Mermaid code block as structural intent; add Mermaid–SVG consistency check in step 6f

### Fixes
- `baoyu-post-to-wechat`: verify editor focus before paste and type operations to prevent silent paste failures

## 1.103.1 - 2026-04-13

### Fixes
- `baoyu-markdown-to-html`: decode HTML entities and strip tags from article summary
- `baoyu-post-to-weibo`: decode HTML entities and strip tags from article summary

## 1.103.0 - 2026-04-12

### Features
- `baoyu-diagram`: add multi-diagram mode — analyze article content and generate multiple diagrams at identified positions; new `--density` option (`minimal`, `balanced`, `per-section`, `rich`) and `--mode` option (`single`, `multi`, `auto`); auto-detects mode from input (file path → multi, short topic → single); inserts diagram image links into article; output structure `diagram/{article-slug}/NN-{type}-{slug}/`

### Fixes
- `baoyu-article-illustrator`: prevent color names and hex codes from appearing as visible text in generated images — add semantic constraint to all palette references and prompt construction rules
- `baoyu-cover-image`: prevent color names and hex codes from appearing as visible text in generated images — add constraint to all palette references and prompt template
- `baoyu-image-cards`: prevent color names from appearing as visible text in generated images
- `baoyu-post-to-wechat`: decode HTML entities and strip HTML tags from article summary before using as WeChat article digest

## 1.102.0 - 2026-04-12

### Features
- `baoyu-imagine`: add OpenAI-compatible image API dialect — new `--imageApiDialect` flag, 
