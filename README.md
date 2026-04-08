# rsmarkdownlint
Markdown linter written in rust

Not a mature one. The Rust ecosystem has pulldown-cmark for parsing markdown but no full-featured linter like
  markdownlint. There's comrak (CommonMark parser) but again, parser not linter.

  You could build one using pulldown-cmark or comrak as the parser and adding lint rules on top. Same approach
  as the SVG linter — a standalone crate. The rules from markdownlint (heading style, blank lines, line length,
  etc.) aren't hard to implement individually.

  That said, markdownlint works fine via Node.js. It's lighter than mermaid — no browser/puppeteer needed. If
  you're trying to eliminate all Node.js dependencies, then a Rust markdown linter would make sense as a
  companion project to the SVG linter.
