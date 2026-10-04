# TOFIX

Findings from a code scan on 2026-10-04.

## High

- `src/main.rs:1-3` - the crate is a "Hello, World!" stub, yet it is released and published as a markdown linter: `Cargo.toml:3,7` (version 0.1.7, "Rust version of markdownlint") and crates.io carries `rsmarkdownlint` 0.1.7. Anyone who installs it gets a binary that prints "Hello, World!". Stop cutting releases until there is a real implementation, and mark the crate as a placeholder (description, README) - or yank the published versions.

## Medium

- `README.md:4-13` - the README is a pasted chat answer, not project documentation: indented continuation lines, references to "the SVG linter" with no link, and advice that "markdownlint works fine via Node.js". Rewrite it to say what the crate is (an unimplemented stub), and note that the fleet already lints markdown with rumdl, a Rust markdownlint port, which may make this project redundant.
- `docs/src/introduction.md:3` - the mdBook (deployed to Pages on release) claims "Rust version of markdownlint" with no mention that nothing is implemented; align it with the README.

## Low

- `src/main.rs:11-14` - the only test is a placeholder that runs `main()`; replace it with real rule tests once a rule exists.
