# Elements of Style Agent Skill

An installable Agent Skill that lets AI coding and writing agents use
William Strunk Jr.'s _The Elements of Style_ as a compact, navigable
writing reference.

The skill is designed for progressive disclosure: the agent first reads
a chapter map, then loads only the chapter needed for the writing task.
This keeps routine prose-editing prompts small while preserving access
to the complete converted text when needed.

## Install

Install from this repository with the Skills CLI:

```bash
npx skills add <owner>/elements-of-style --skill elements-of-style
```

Install directly from the skill path:

```bash
npx skills add https://github.com/<owner>/elements-of-style/tree/main/skills/elements-of-style
```

Install globally for Claude Code:

```bash
npx skills add <owner>/elements-of-style --skill elements-of-style -a claude-code -g
```

Replace `<owner>` with the GitHub account or organization that hosts
the repository.

## What It Contains

```text
skills/
  elements-of-style/
    SKILL.md
    references/
      chapter-map.md
      elements-of-style.md
      chapters/
        01-purpose-scope-and-style-method.md
        02-punctuation-and-basic-usage-rules.md
        03-composition-sentence-and-paragraph-principles.md
        04-manuscript-form-quotations-and-typography.md
        05-misused-words-and-usage-glossary.md
        06-spelling-and-word-forms.md
        07-punctuation-composition-exercises.md
```

`SKILL.md` contains the activation description and workflow.
`references/chapter-map.md` tells the agent which chapter to load for a
given writing task. The chapter files preserve the book's rules,
examples, tables, verse, and visual spacing as Markdown.

## Source

The source text is William Strunk Jr.'s 1918/1919 _The Elements of
Style_, converted from the Project Gutenberg plain-text edition,
eBook #37134.

This edition is public domain in the United States. The Project
Gutenberg header states that it may be copied, given away, or reused
under the Project Gutenberg License.

## Example Uses

- Revise a paragraph for concision while preserving the author's voice.
- Check punctuation, comma use, apostrophes, parenthetic expressions,
  comma splices, and sentence fragments.
- Rewrite passive or vague prose into active, concrete language.
- Find needless words, stock phrases, and inflated expressions.
- Improve paragraph unity, topic sentences, parallel structure, word
  order, tense consistency, and sentence emphasis.
- Check common usage problems such as `less` vs. `fewer`, `like` vs.
  `as`, `which` clauses, `whom`, `while`, `should`, and `would`.
- Format quotations, references, numerals, titles, parentheses, and
  manuscript headings.
- Generate style exercises or explain why a sentence violates a rule.

## Example Prompts

```text
Use The Elements of Style to tighten this paragraph without changing my meaning.
```

```text
Check this passage for comma splices, dangling modifiers, and needless words.
```

```text
Review this essay intro for topic-sentence clarity and concrete language.
```

```text
Explain which Elements of Style rules apply to this sentence and suggest a revision.
```

## Notes

The skill treats Strunk's rules as guidance for clear prose, not as a
replacement for the user's voice, genre, house style, or modern usage
requirements. When rules conflict with meaning, audience, or deliberate
style, the agent should explain the tradeoff and preserve the stronger
choice.
