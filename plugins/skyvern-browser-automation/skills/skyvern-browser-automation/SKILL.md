---
name: skyvern-browser-automation
description: Browser automation via Skyvern MCP for navigation, form filling, authentication, structured data extraction, and multi-step workflows.
trigger: skyvern
license: MIT
metadata:
  author: mark1ian
  version: "1.0.0"
---

# Skyvern Browser Automation

Use this skill when a task requires real browser interaction through Skyvern MCP.

This skill enables agents to control a live browser session to navigate websites, fill forms, handle authentication, and extract structured data.

## When to Use

Use this skill when the task requires:

- navigating real websites
- interacting with dynamic web pages
- filling and submitting forms
- logging into services
- extracting structured data from pages
- executing multi-step browser workflows
- validating results after actions

## When NOT to Use

Do not use this skill when:

- the task can be solved without browser interaction
- the answer is already available in context
- the task is purely informational or text-based
- no external website interaction is required

## Execution Strategy

Follow this process when using the skill:

1. Identify the target website and goal.
2. Break the task into clear browser steps.
3. Create a browser session.
4. Navigate to the required page.
5. Perform interactions (clicks, inputs, etc.).
6. Verify the page state after each step.
7. Extract structured data if needed.
8. Close the session when finished.

Do not attempt to perform the entire workflow in a single step.

## Authentication Handling

If the task requires login:

- detect login requirements early
- enter credentials when provided
- confirm successful login before continuing
- do not assume authentication succeeded without verification
- re-check page state if flow breaks

## Data Extraction Guidelines

When extracting data:

- identify exactly what fields are required
- navigate to the correct page before extracting
- return structured output (JSON-like when possible)
- avoid including irrelevant content
- validate extracted data against the page

## Multi-step Workflows

For complex tasks:

- split the task into sequential steps
- execute one step at a time
- confirm success before moving forward
- report intermediate progress if needed
- stop and explain if the workflow cannot continue

## Error Handling

If something fails:

- inspect current browser state
- identify the cause (navigation, auth, UI changes, etc.)
- retry only when justified
- avoid repeating failing actions blindly
- clearly report blockers

## Output Requirements

When returning results:

- clearly state what was completed
- separate successful and failed steps
- return structured data where applicable
- include any limitations or missing data

## MCP Configuration

This skill uses the Skyvern MCP endpoint:

```
https://api.skyvern.com/mcp
```

## Example Tasks

- Open a website and extract structured data
- Log into a dashboard and collect information
- Fill out and submit a web form
- Navigate a multi-step workflow and report results
- Validate data across multiple pages
