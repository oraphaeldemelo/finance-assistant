# Development Workflow — v1

## Feature development

1. Create a new FIN.
2. Understand the issue that needs to be developed for the project.
3. Define the initial decisions and requirements for the feature.
4. Create a feature branch:
   - Use the pattern `feature/fin-<number-fin>-<title-fin>`.
   - Use a short, kebab-case description for `<title-fin>`.
   - Create the branch from a clean `main` branch that is updated with `origin/main`.
5. The human creates the task specification and prompt.
6. After the prompt is created, the agent implements it and creates code following the principles documented in `AGENTS.md`, including the Architecture and coding guidance section.
7. Before finishing, the agent performs the applicable validations and provides the completion report according to [Definition of Done](definition-of-done.md).
8. A human reviews the changes:
   - **Changes requested:** fix the changes, validate them, and submit them for a new review.
   - **Approved:** continue to the next steps.

## Human integration steps

The following steps must be performed by a human:

1. Commit the changes on the feature branch.
2. Before final integration, verify whether the feature branch is updated with `origin/main`. If it is not:
   1. Switch to the `main` branch.
   2. Update `main` from `origin`.
   3. Switch to the feature branch.
   4. Merge `main` into the feature branch.
      - If there are conflicts, resolve them on the feature branch.
      - If there are no conflicts, continue to validation.
   5. Perform new validation on the feature branch according to [Definition of Done](definition-of-done.md).
      - **Changes requested:** fix the changes, perform new validation, and submit them for a new review.
      - **Approved:** continue to the next step.
3. Push the feature branch to `origin`.
4. Switch to the `main` branch.
5. Merge the feature branch into `main`.
6. Perform final validation using [Definition of Done](definition-of-done.md) with the updated `main` branch.
   - **Changes requested:** report the errors, stop, and wait for human review.
   - **Approved:** continue to the next step.
7. Push `main` to `origin`.
8. Delete the local and remote feature branch.
