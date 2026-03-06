---
name: reading-quiz
description: Use when the user asks to be quizzed on what they recently read, or wants to review reading material from crossbill. Triggers on words like "quiz", "test me", "review reading", "what did I read".
---

# Reading Quiz

Quiz the user on their recently read material from Crossbill.

## Workflow

1. **Find the book** - Use `mcp__crossbill__list_books` to search by title
2. **Get reading sessions** - Use `mcp__crossbill__get_reading_sessions` with the book ID
3. **Filter to relevant sessions** - By default, filter to today's sessions. If user specifies a time range, use that instead.
4. **Extract content** - Parse the session content from the results
5. **Quiz with 5 questions** - Ask one question at a time, wait for the answer before proceeding

## Question Style

Ask about **substance and big ideas**, not details:

- Underlying principles and reasoning
- Why something matters, not just what it says
- Connections between concepts
- Implications and applications
- Author's core arguments

Do NOT ask about:

- Specific names, terms, or labels
- Minor details or examples
- "What was X called?"
- Trivia recall questions

## Interaction Pattern

- Ask one question, wait for the user's response
- Give brief feedback (2-3 sentences) on their answer, clarifying or expanding if needed
- If user doesn't know, explain the key idea concisely and move on
- After all questions, give a brief overall summary of how they did
- Keep tone conversational, not like an exam
