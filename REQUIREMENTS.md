# Archive Analyst requirements

Updated: 2026-09-15

## Purpose

Build a desktop app that makes personal archives readable, searchable and available for conversational exploration. Users should be able to revisit past discussions, reconstruct events and examine how their thinking changed over time. Answers must link to the original dated messages.

This is the current scope. It supersedes earlier descriptions that restricted the project to ChatGPT or Gmail alone.

## Sources in scope

- ChatGPT conversation archives.
- Gmail email archives.
- Apple Messages / iMessage history. The supported import method still needs to be established.

Use a common reading, search and question interface across supported sources. Allow users to choose which archives a query covers. Import must report missing or unsupported records; including a source in the plan does not establish that its entire history is recoverable.

## Core capabilities

- A double-clickable Mac application with a usable interface.
- Import archives and retain a local library for later visits.
- Browse original messages and conversations.
- Search message text and email subjects, with date and sender filters.
- Open search results at the matching message with the surrounding conversation available.
- Ask questions, follow up conversationally and compare different periods.

Conversational analysis is part of the intended product. Ordinary browsing and search should also work without an AI service.

## Question and retrieval workflow

1. Start from the user's question and chosen sources, dates and speakers.
2. Generate an extensive set of relevant search terms.
3. Find candidate matches and retrieve the text around each match.
4. Have AI assess whether each passage is relevant to the question.
5. Filter out irrelevant passages and consider retained evidence together.
6. Produce an answer with direct references that open the supporting original messages.

Retain enough context to interpret short replies. Report the scope of a search and gaps in coverage. Absence from retrieved results must not become a claim that something never happened.

## Dates and attribution

Preserve original timestamps and display the selected time zone. Keep the date a message was written separate from dates of events it describes. Mark missing dates and inferred event dates explicitly.

Distinguish the user's words from assistant replies and other people's messages. Allow searching just the user's messages or the whole conversation. Assistant suggestions must not be attributed to the user as beliefs. Material quoted inside a message must remain distinguishable from the sender's own statements.

Preserve conversation structure and available branches. Answers should distinguish quotations from interpretation and retain conflicting evidence or changes of position.

## First real acceptance test

The owner will import a personal Gmail archive and use the app to search and read the emails. This is the first practical test of the broader application. Build that app workflow before investigating the contents of the owner's personal archive separately.

Use invented messages for development checks and public demonstrations. Keep personal archives and derived libraries outside the public source repository. Explain any external AI data processing and let the user enable it.

## Project delivery

Develop Archive Analyst as a public GitHub project with documented behavior and a downloadable application. No terminal commands should be required to use the released app. Telegram and other sources can be reconsidered later.
