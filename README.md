# Tallyman

A command-line tool that summarizes the size of a codebase by language, showing lines of code with and without comments and blank lines.

![](https://mkennedy-shared.nyc3.digitaloceanspaces.com/github/tallyman-for-commandbook.webp)

## Overview

Point Tallyman at any project directory and get a quick breakdown of what's in it. It counts lines across languages  -  Python, Rust, JavaScript, CSS, HTML, Markdown, and more  -  and reports both the raw line count and the count excluding comments and blank lines. Results are grouped into categories (Code, DevOps, Design, Docs) so you can see the shape of your project at a glance.

Tallyman automatically skips things that aren't your code: virtual environments, `node_modules`, build artifacts, `.git`, and generated or minified files. What you get back is a realistic picture of the code *you* wrote.


## Features

- **Dual line counts**  -  Total lines and lines excluding comments and blank lines, per language
- **Category totals**  -  Aggregated summaries across Code, DevOps, Design, Docs, and Data
- **Multi-language support**  -  Python, Rust, JavaScript, TypeScript, CSS, HTML, Markdown, and more
- **Smart exclusions**  -  Automatically ignores:
  - Virtual environments (`venv/`, `.venv/`, `env/`)
  - Node modules (`node_modules/`)
  - Build artifacts and caches
  - Version control directories (`.git/`)
  - Generated and minified files
- **Colorful terminal output**  -  Clean, readable formatting in the terminal
- **Realistic metrics**  -  Only counts the code you wrote, not third-party dependencies

> **Note on comment detection:** Tallyman detects single-line comments (`#`, `//`, `--`, etc.) but does not detect multi-line comment blocks (`/* */`, `""" """`, `{- -}`, etc.). Lines inside multi-line comment blocks are counted as code.

## Supported Languages

Tallyman recognizes 40 languages, grouped into five categories for the summary totals:

### Code

| Language | Extensions / Filenames |
|----------|----------------------|
| Python | `.py` |
| Rust | `.rs` |
| Go | `.go` |
| JavaScript | `.js`, `.jsx`, `.mjs` |
| TypeScript | `.ts`, `.tsx` |
| Java | `.java` |
| C | `.c` |
| C Header | `.h` |
| C++ | `.cpp`, `.hpp`, `.cc`, `.cxx` |
| C# | `.cs` |
| Swift | `.swift` |
| Kotlin | `.kt`, `.kts` |
| Ruby | `.rb` |
| Shell | `.sh`, `.bash`, `.zsh` |
| Lua | `.lua` |
| PHP | `.php` |
| Perl | `.pl`, `.pm` |
| R | `.r`, `.R` |
| Dart | `.dart` |
| Scala | `.scala` |
| Elixir | `.ex`, `.exs` |
| Zig | `.zig` |
| Haskell | `.hs` |
| Erlang | `.erl` |
| OCaml | `.ml`, `.mli` |
| Nim | `.nim`, `.nims` |
| V | `.v`, `.vv` |

### DevOps

| Language | Extensions / Filenames |
|----------|----------------------|
| Terraform | `.tf`, `.tfvars` |
| Makefile | `.mk`, `Makefile`, `makefile`, `GNUmakefile` |
| Docker | `.dockerfile`, `Dockerfile*`, `docker-compose.yml/yaml`, `compose.yml/yaml` |

### Design

| Language | Extensions |
|----------|-----------|
| CSS | `.css` |
| SCSS | `.scss` |
| LESS | `.less` |
| HTML | `.html`, `.htm`, `.xhtml`, `.shtml`, `.pt`, `.jinja`, `.jinja2`, `.j2`, `.njk`, `.hbs`, `.ejs`, `.mustache` |
| SVG | `.svg` |

### Docs

| Language | Extensions |
|----------|-----------|
| Markdown | `.md`, `.mdx` |
| reStructuredText | `.rst` |

### Data

| Language | Extensions |
|----------|-----------|
| TOML | `.toml` |
| YAML | `.yml`, `.yaml` |
| JSON | `.json` |
| XML | `.xml` |
| SQL | `.sql` |

There is also a **Specs** category  -  when Markdown or reStructuredText files are found inside directories named `specs/`, `plans/`, `specifications/`, or `agents/`, they are automatically reclassified from Docs to Specs.

## Installation

```bash
uv tool install tallyman-metrics
```

Or with pip:

```bash
pip install tallyman-metrics
```

## Usage

```bash
# Analyze current directory
tallyman

# Analyze a specific path
tallyman /path/to/project

# Show help
tallyman --help
```

## Requirements

- Python 3.14+

## License

MIT License
