---
name: sales-call-prep
description: Prepare for an upcoming sales call by pulling CRM context and past conversation history, researching attendees and their company, and building a structured agenda with tailored discovery questions. Use this skill whenever a user mentions an upcoming customer call, sales meeting, demo, discovery call, QBR, or check-in — even if they don't use the word "prep". Trigger on phrases like "I have a call with", "meeting with [company/person]", "preparing for my call", "call tomorrow", "what should I know before talking to", "help me get ready for", or any request to research a prospect or customer ahead of a conversation.
---

# Sales Call Prep

Prepare for an upcoming sales call end-to-end: pull CRM and conversation history, research the attendees and their company, then deliver a structured briefing with a ready-to-run agenda and sharp discovery questions.

## Step 1 — Gather what you already know

Start by collecting context from available sources in parallel:

**From CRM / Airtable** (if connected via MCP):
- Account name, deal stage, ARR / deal size, owner, close date
- Recent activity log: emails, calls, notes
- Open tasks and next steps
- Any recorded pain points or use cases

**From past conversations** (search Slack, Gmail, Notion, Google Docs as available):
- Previous meeting notes or follow-up emails
- Commitments made in either direction
- Objections already raised and how they were handled
- Champion and economic buyer names

**From the user directly** (ask if data is missing or tools aren't connected):
- Who is attending (names, titles, company)?
- What stage is this deal / relationship?
- What's the goal of this specific call?
- Any specific concerns or topics the user wants to cover?

Collect everything before moving to research — doing it in parallel saves time.

## Step 2 — Research attendees and company

For each named attendee, look up:
- Current role and how long they've been in it
- Professional background relevant to your product (LinkedIn / web search if available)
- Any public content they've written or spoken at (signals priorities and vocabulary)

For the company, gather:
- Industry, size, business model
- Recent news: funding, product launches, leadership changes, layoffs, acquisitions
- Likely pain points given their stage and industry
- Known competitors and how the prospect talks about them (if any signals exist)

Note anything that creates natural conversation hooks ("I saw you recently announced X — how is that affecting Y?").

## Step 3 — Build the call brief

Deliver a concise briefing with the following sections. Use the exact template below so it's scannable in under 2 minutes.

```
## Call Brief — [Company Name] | [Date]

### Attendees
| Name | Title | Notes |
|------|-------|-------|
| ...  | ...   | ...   |

### Deal / Relationship Snapshot
- Stage: ...
- Goal of this call: ...
- Key history: [2-3 bullet summary of past interactions]

### Company Intel
- [2-3 bullets: recent news, size/stage, business model]

### Their Likely Priorities
- [2-3 inferred pain points or strategic initiatives based on research]

### Agenda (suggested)
1. [Opening / rapport — X min]
2. [Topic — X min]
3. [Topic — X min]
4. [Next steps / close — X min]

### Discovery Questions
**Situation**
- ...

**Problem / Pain**
- ...

**Impact**
- ...

**Decision / Next Steps**
- ...

### Watch-outs
- [Any objections to anticipate, sensitivities from past conversations, or topics to avoid]

### Pre-call checklist
- [ ] Confirm attendees haven't changed
- [ ] Review latest product updates relevant to their use case
- [ ] Prepare a relevant customer story or case study
- [ ] Know your walk-away / next step if the call goes well / badly
```

## Guidance for discovery questions

Write questions that are genuinely open, non-leading, and calibrated to the deal stage:

- **Early / discovery**: Focus on current state, challenges, and consequences. Avoid pitching.
- **Mid / evaluation**: Focus on decision criteria, internal process, and stakeholder map.
- **Late / close**: Focus on any remaining blockers, timeline pressure, and implementation readiness.

Aim for 3–5 questions per quadrant (situation, problem, impact, decision), pruned to the 2–3 sharpest in each that fit this specific meeting. Tailor language to what you've learned about the attendee — a CTO and a VP of Sales need very different questions.

## Handling missing context

If CRM tools are not connected or return no data, note that clearly and ask the user to fill in the gaps. Do not invent deal details. For company and attendee research, use web search if available; if not, flag that research was skipped.

If the user hasn't said who will be on the call, ask before building the agenda — the right questions depend heavily on the audience.

## Output format

- Default: deliver the full brief in the conversation thread as markdown.
- If the user asks for a document (Google Doc, Notion page, etc.) and the relevant MCP is connected, offer to create it there.
- Keep the brief tight — a sales rep should be able to read it in 2 minutes before joining the call.
