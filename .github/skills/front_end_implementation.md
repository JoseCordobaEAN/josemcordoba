[Agent Implementation Workflow — Issue-Based Tasks]

This workflow guides agents to implement tasks based on issues in the repository, ensuring user involvement and traceability. Follow these steps for each issue:

1. **Retrieve Issue Context**
   - Use MCP to get the full context of the issue by its ID (title, description, requirements, labels, etc.).

2. **Summarize and Confirm**
   - Present your understanding of the issue’s purpose, requirements, and scope to the user.
   - Ask the user to confirm or clarify before proceeding.

3. **Create Implementation Branch**
   - Create a new branch for the implementation, named after the issue (e.g., `issue-123-feature-title`).

4. **Propose Implementation Plan**
   - If the user agrees, propose a step-by-step implementation plan, referencing repo conventions and the implementation plan if relevant.

5. **Iterative Step Confirmation**
   - For each step, present the proposed action to the user and request confirmation before executing.
   - Iterate until all steps are completed and the task is fully implemented.

6. **Checkout Implementation Branch Locally**
   - After creating the remote branch, fetch and checkout the branch locally using `git fetch origin && git checkout <branch-name>`.

7. **Test and Validate**
   - Run `npm run dev` to test changes locally.
   - Run `npm run type-check` and `npm run lint` to validate code quality.
   - For Tailwind changes, restart the dev server to ensure styles are properly compiled.

**Notes:**

- Always reference the issue and implementation plan for traceability.
- Use repo conventions for branch naming, code structure, and commit messages.
- Keep the user involved at every decision point.
- Consider the site's purpose and target audience when implementing features.
- Use semantic HTML5 and accessibility best practices (ARIA labels, proper heading hierarchy).
- For Tailwind v4: use utility classes directly in templates, avoid `@apply`, use `@import "tailwindcss"` in CSS files.
