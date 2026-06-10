# Style Guide

Shared voice, tone, and formatting rules that every agent follows when producing documentation.

## Voice and Tone

- **Active voice.** "The API returns a 200 response" not "A 200 response is returned by the API"
- **Present tense.** "The endpoint accepts a `limit` parameter" not "The endpoint will accept"
- **Second person.** "You can paginate results using `cursor`" not "Users can paginate"
- **Be direct.** Prefer short sentences. Omit unnecessary words.

## Formatting

- **Code elements** (parameters, methods, endpoints, file paths) use backticks
- **Emphasis** uses bold or context, not italics
- **Lists** use dashes, not asterisks
- **Headers** use ATX-style (`##`), not Setext-style (underlines)

## Document Structure

Every document should have:

1. **Title** — single H1 at the top
2. **Context** — one paragraph explaining what this doc covers and who it's for
3. **Body** — organized with H2 and H3 sections
4. **Examples** — realistic code snippets for key operations

## API Documentation Specific

- List parameters in a table with Name, Type, Required, Default, Description
- Show one request-response pair per endpoint
- Group related endpoints under resource headings

## Writing Guidelines

- Define acronyms on first use
- Prefer descriptive links ("see the [pagination guide](/pagination)") over bare URLs
- Use `null` for null values, not `nil`, `None`, or empty string
- Spell out numbers under 10; use numerals for 10 and above
