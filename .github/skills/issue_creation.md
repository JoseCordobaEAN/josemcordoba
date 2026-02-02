# Iterative Ticket Creation Instructions

This guide describes how to create GitHub issues (tickets) for this project an iterative, agent-assisted approach. The process ensures all planned features are tracked as issues, and each ticket is reviewed before being created.

The repo is at https://github.com/JoseCordobaEAN/josemcordoba/issues

## Workflow Steps

1. **Read the Implementation Plan**
   - The agent reads the `implementation_plan.md` file to identify all planned sections, features, and components.

2. **Check for Missing Issues**
   - The agent compares the plan with existing GitHub issues using MCP to determine which planned items are not yet tracked as issues.

3. **Propose Draft Issues**
   - For each missing item, the agent drafts a proposed issue, including:
     - Title
     - Description (purpose, requirements, route, components, data sources, etc.)
     - Suggested labels
   - The draft is presented for review and approval.

4. **Review and Approve**
   - The user reviews the draft issue(s).
   - If changes are needed, the agent revises the draft.
   - Once approved, the agent proceeds to create the issue.

5. **Create Issue via MCP**
   - The agent uses the GitHub MCP integration to create the approved issue in the repository.
   - The process repeats for each missing item until all planned work is tracked.

## Example

- Agent reads `implementation_plan.md` and finds a section for the About page.
- No existing issue for About page is found.
- Agent drafts an issue:
  - Title: "Implement About Page"
  - Description: Details from the plan (purpose, route, components, data, etc.)
- User reviews and approves the draft.
- Agent creates the issue via MCP.

## Notes

- Keep issues focused and scoped to a single feature or section.
- Use labels for categorization (e.g., `feature`, `frontend`, `content`).
- Reference the implementation plan in each issue for traceability.
- Repeat the process as the plan evolves or new sections are added.

---

For questions or improvements to this workflow, update this file or discuss in the repository.
