
# CLINT: CLI Navigator Toolkit

A Command Line Tool that helps you navigate other CLIs.

This is a _Rustification_ of [https://github.com/funnierinspanish/cli-explorer-toolchain_legacy](https://github.com/funnierinspanish/cli-explorer-toolchain_legacy), even though the original project is not maintained anymore, it is still a great resource to explore CLI tools.

## Features

### Extract a CLI tool's structure

Recursively navigates through a CLI tool using its _help page_ output and extracts the structure of the tool, including commands, subcommands, flags, and their occurrences.

### Unique _Keywords_

Generates a summary of the CLI tool's structure in different formats:

- **Markdown**: A human-readable markdown file.
- **Plain Text**: A simplified human-readable plain text file.
- **JSON**: A structured JSON file that contains the structure of the CLI tool.

### Generate a Summary

Generates a summary of the CLI tool's structure in different formats:

- **Markdown**: A human-readable markdown file.
- **Plain Text**: A simplified human-readable plain text file.
- **JSON**: A structured JSON file that contains the structure of the CLI tool.

### Generate a web-based visualization

Generates a web-based visualization of the CLI tool's structure using simplified HTML and JavaScript.

### Replicate a CLI tool

Generates a replica of the CLI tool in Rust using the `clap` library. This includes commands, subcommands, and flags, and creates placeholders for the implementation of each command. It is meant to be a starting point for building experiments with Developer Experience (DX) in mind.

Example:

```plain
cargo run -- replicate out/hugo/hugo-structure.json -o out/hugo/replica
```

A new rust project will be created in the `out/hugo/replica` directory with a pre-built binary. You can then modify any of the commands and subcommands to implement your own logic.

## Usage

```plain
Usage: clint [COMMAND]

Commands:
  parse            Parses a CLI program written with the Cobra library and generates a JSON file with its structure
  unique-keywords  Extracts unique keywords (commands, subcommands, and flags) from a parsed JSON file
  summary          Generates a summary of the CLI structure
  webpage          Genrates a static webpage with the CLI structure
  replicate        Generates a replica of the CLI program in RustLang using the clap library
  help             Print this message or the help of the given subcommand(s)

Options:
  -h, --help     Print help
  -V, --version  Print version
```