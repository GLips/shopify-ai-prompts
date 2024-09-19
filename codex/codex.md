# AI Codex

## Usage

- Review: @codex.md (silent load, no output)
- Update: @learn.md
- File paths: Always use absolute paths from project root

## Errors

E000:

- Context: [Relevant project area or file]
- Error: [Precise description]
- Correction: [Exact fix]
- Prevention: [Specific strategy]
- Related: [IDs of related errors/learnings]

## Learnings

L000:

- Context: [Relevant project area or file]
- Insight: [Concise description]
- Application: [How to apply this knowledge]
- Impact: [Potential effects on project]
- Related: [IDs of related errors/learnings]

L001:

- Context: @codex.md usage
- Insight: @codex.md is for context, not for direct modification
- Application: Use @codex.md for silent loading and context only; execute subsequent commands separately
- Impact: Improved accuracy in responding to user intentions
- Related: None

L002:

- Context: Shopify theme development, schema translations
- Insight: User prefers straight English strings in Shopify schemas rather than references to i18n values
- Application: Use plain English text for labels, descriptions, and other schema content instead of translation keys
- Impact: Improved readability of schema files, simplified development process, potential loss of multi-language support
- Related: None

L003:

- Context: Shopify theme development, liquid file organization
- Insight: User prefers to define all Shopify variables at the top of the file or at the start of block type iterations
- Application: Group all section.settings and block.settings assignments at the beginning of the file or block loop
- Impact: Improved code readability, cleaner HTML without inline Shopify variable references
- Related: None
