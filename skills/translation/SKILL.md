---
name: translation
description: Use this skill whenever the user wants to translate text from one language to another. This includes translating documents, paragraphs, sentences, or individual words. Handles all major languages and language pairs. Also useful for explaining nuances, idiomatic expressions, tone preservation, and localization. Trigger when the user asks to translate, convert, or localize content between languages.
---

# Translation Skill

## Overview

This skill guides precise, high-quality translation between any two languages. The goal is not word-for-word substitution, but faithful, natural-sounding output that preserves the original tone, register, intent, and meaning.

## Workflow

### 1. Identify the Task

Determine:
- **Source language**: What language is the input in? (Detect automatically if not specified.)
- **Target language**: What language should the output be in?
- **Register/tone**: Is the text formal, informal, technical, literary, conversational?
- **Context**: Is this a legal document, marketing copy, personal message, technical manual, or something else?

If the target language is unclear, ask the user before proceeding.

### 2. Translate

Produce a translation that:
- **Preserves meaning** — convey the full intent of the source, not just the words.
- **Preserves tone and register** — formal text stays formal; casual text stays casual.
- **Preserves formatting** — maintain paragraphs, bullet points, headings, bold/italic, etc.
- **Uses natural phrasing** — the output should read as if it were originally written in the target language, not translated.
- **Handles idiomatic expressions** — replace idioms with equivalent expressions in the target language rather than translating literally.

### 3. Provide Annotations (when helpful)

For complex or nuanced translations, offer:
- **Alternative translations** for words or phrases with multiple valid options.
- **Notes on idioms or cultural references** that required adaptation.
- **Glossary of key terms** for technical or specialized content.

Only include annotations if they add value. For simple, clear translations, just provide the result.

## Guidelines

- **Ambiguity**: If the source text is ambiguous, translate the most likely interpretation and note the ambiguity.
- **Untranslatable terms**: When a term has no direct equivalent, use the closest natural equivalent and add a brief note if needed.
- **Names and proper nouns**: Keep names as-is unless they have standard translated forms (e.g., place names, historical figures).
- **Numbers and dates**: Adapt to the conventions of the target language and region.
- **Units of measurement**: Adapt if necessary for the target audience (e.g., imperial vs. metric).
- **Currency and addresses**: Preserve as-is unless localization is explicitly requested.

## Examples

- "Translate this email to French." → Translate, preserve formal register if present.
- "How do you say 'It's raining cats and dogs' in German?" → Provide equivalent idiom and explanation.
- "Translate this technical manual to Spanish." → Translate, preserve technical terminology, flag any terms without standard equivalents.
- "What's the difference between 'tu' and 'vous' in French?" → Explain the distinction clearly.

## Supported Languages

All major world languages are supported, including but not limited to:
English, German, French, Spanish, Italian, Portuguese, Dutch, Polish, Russian, Arabic, Chinese (Simplified and Traditional), Japanese, Korean, Hindi, Turkish, Swedish, Norwegian, Danish, Finnish, Czech, Romanian, Hungarian, and more.
