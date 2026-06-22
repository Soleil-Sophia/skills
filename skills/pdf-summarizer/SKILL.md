---
name: pdf-summarizer
description: Use this skill whenever the user wants to summarize a PDF or extract key information from PDF-derived text. This includes executive summaries, key-point extractions, section-by-section breakdowns, and multi-document PDF comparisons. Trigger when the user asks to summarize, condense, extract key points from, or give an overview of a PDF (or pasted text clearly taken from a PDF). Prefer this skill over `pdf` when the user’s primary intent is summarization rather than file handling or OCR.
---

# PDF Summarizer Skill

## Overview

This skill produces accurate, structured summaries of PDF documents and other text-based files. The goal is to help users quickly understand the content, key findings, and structure of a document without reading it in full.

## Workflow

### 1. Understand the User's Goal

Before summarizing, identify what the user actually needs:
- **Quick overview**: A short paragraph covering the main topic and conclusions.
- **Executive summary**: A structured summary with key points, suitable for decision-makers.
- **Section-by-section breakdown**: A summary of each chapter or section.
- **Key point extraction**: A bulleted list of the most important takeaways.
- **Specific focus**: The user wants only a specific part (e.g., "just the methodology" or "only the financial figures").

If the request is vague (e.g., "summarize this PDF"), default to an executive summary format and offer alternatives.

### 2. Read the Document

If the PDF has been provided as a file or its text has been pasted:
- Read the full document before summarizing.
- Note the document type (research paper, legal contract, technical report, etc.) as this affects the appropriate summary format.

If the user has not yet provided the document, ask them to share it.

### 3. Produce the Summary

Choose the appropriate format based on the user's goal:

#### Executive Summary (default)
```
## Executive Summary

**Document**: [Title or filename]
**Type**: [e.g., Research Paper / Annual Report / Contract]
**Length**: [e.g., 24 pages]

### What This Document Is About
[1–3 sentences describing the document's purpose and scope.]

### Key Findings / Main Points
- [Key point 1]
- [Key point 2]
- [Key point 3]
- ...

### Conclusions / Recommendations
[1–3 sentences on the document's conclusions or recommended actions, if applicable.]

### Notable Details
[Any figures, dates, names, or data points that stand out.]
```

#### Section-by-Section Breakdown
Summarize each major section or chapter in 2–5 sentences. Preserve section headings from the original document.

#### Bulleted Key Points
Extract the most important facts, arguments, decisions, or data points as a concise bulleted list.

### 4. Follow-Up

After delivering the summary, offer to:
- Answer specific questions about the document.
- Search for particular information within the document.
- Compare this document with another.
- Translate the summary into another language (use the `translation` skill if available).

## Guidelines

- **Accuracy first**: Never invent or infer facts not present in the document. If something is unclear, say so.
- **Preserve key figures and data**: Numbers, dates, names, and statistics should be quoted accurately.
- **Match the register**: A legal contract summary should be precise and formal; a marketing brochure summary can be lighter.
- **Do not editorialize**: Summarize what the document says, not whether it is correct or good.
- **Flag limitations**: If the PDF is scanned and text extraction was poor, or if certain sections were illegible, note this.
- **Respect length**: A 5-page document needs a shorter summary than a 200-page report. Calibrate accordingly.

## Examples

- "Summarize this research paper." → Executive summary with abstract, methods, findings, and conclusion.
- "Give me the key points from this contract." → Bulleted list of obligations, dates, parties, and penalties.
- "What does chapter 3 say?" → Section-level summary of the requested chapter.
- "Compare these two reports." → Side-by-side summary highlighting similarities and differences.
- "What are the main risks mentioned in this document?" → Targeted extraction of risk-related content.

## Document Types

This skill handles a wide range of document types:
- Academic and scientific papers
- Business and financial reports
- Legal contracts and agreements
- Technical manuals and specifications
- Policy documents and government reports
- Presentations and slide decks (converted to text)
- Books and long-form articles
