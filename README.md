# The chiasm LaTeX Package

A LaTeX package for typesetting chiastic literary structures with automatic labeling and progressive indentation.

## What is a Chiasm?

A chiasmus (plural: chiasmi) is a literary device where concepts or phrases are presented in a sequence and then repeated in reverse order, creating a mirror or symmetric structure. For example:

```
A: First concept
  B: Second concept
    C: Third concept
  B': Second returns
A': First returns
```

This pattern is common in ancient literature, rhetoric, religious texts, and poetry.

## Features

- **Automatic labeling**: Items are automatically labeled A, B, C, ..., then C', B', A' on return
- **Progressive indentation**: Each level is indented further to create a "staircase" effect
- **Nested structures**: Support for chiasms within chiasms with prefixed labels (e.g., B.a, B.b)
- **Replacement nesting**: Nested chiasms can automatically replace a level (e.g., D.a, D.b instead of D)
- **Pivot markers**: Mark center elements that have no prime partner
- **Customizable**: Adjustable indentation step size

## Installation

### Method 1: Local Installation

1. Copy `chiasm.sty` to your document directory
2. Use `\usepackage{chiasm}` in your LaTeX document

### Method 2: System Installation

Copy `chiasm.sty` to your local TeX tree:
- Linux/Mac: `~/texmf/tex/latex/chiasm/`
- Windows: `C:\Users\YourName\texmf\tex\latex\chiasm\`

Then run `texhash` or `mktexlsr` to update the TeX database.

## Quick Start

```latex
\documentclass{article}
\usepackage{chiasm}

\begin{document}

\begin{chiasm}
  \item First concept
  \item Second concept
  \item Third concept
  \chiasmreturn
  \item Third returns
  \item Second returns
  \item First returns
\end{chiasm}

\end{document}
```

## Documentation

See `chiasm-doc.pdf` for complete documentation including:
- Detailed usage instructions
- All available commands
- Multiple examples
- Nested chiasm patterns
- Replacement nesting
- Pivot elements

## Examples

The package includes several example files:
- `example-simple.tex` - Basic usage examples
- `example-advanced.tex` - Complex nested structures and literary examples

Compile these with:
```bash
pdflatex example-simple.tex
pdflatex example-advanced.tex
```

## Basic Commands

- `\begin{chiasm} ... \end{chiasm}` - Create a chiastic structure
- `\item` - Add an element (automatically labeled)
- `\chiasmreturn` - Mark the transition from descending to ascending
- `\chiasmpivot` - Mark the next item as a center pivot (no prime)

## Package Options

```latex
\usepackage[smallindent]{chiasm}  % 0.8em per level
\usepackage{chiasm}               % 1.2em per level (default)
\usepackage[largeindent]{chiasm}  % 1.6em per level
```

## Requirements

- LaTeX2e
- `enumitem` package
- `xparse` package (part of LaTeX3)

## Version History

- **v1.0** (2025-01-27): Initial release

## License

LaTeX Project Public License v1.3c or later

## Author

Jeremy Lloyd Conlin ([@jlconlin](https://github.com/jlconlin)) in collaboration with AI tools. My (La)TeX skills are not good enough to do this on my own, but I needed this capability.

## Contributing

Bug reports and feature requests are welcome!

## Acknowledgments

Based on collaborative development exploring LaTeX techniques for typesetting complex literary structures.
