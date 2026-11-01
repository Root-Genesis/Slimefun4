# Contribution Guidelines

Before contributing code to the Slimefun (English Fork), please read these guidelines carefully.

# Environment Setup

We provide an automated code style check system. Please run `./gradlew spotlessApply` to initialize the environment.

The project includes an `.editorconfig` file to control code style. If you have your own code style, please switch to the project's style before contributing.

# Branching Policy

Before starting your contribution, ensure your code is based on the `dev` branch.

# Commit Message Convention

This project **strictly enforces** the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification.

> In short, your commit message should follow this format:
>
> <type>[optional scope]: <description>
>
> For example, a commit adding a new feature should be: `feat(item): add new item to Slimefun`

If your code fixes an issue, explicitly state it in the commit body (not just the title).

> e.g., `resolves #114514` or `fix #114514`

If the fix is obvious and described in the title, duplication is not necessary.

Supported type prefixes: `(feat(ure)?|fix|docs|style|refactor|ci|chore|perf|build|test|revert|trans)`

Additionally, use the `trans` type for translation-related commits.

# Code Style

**!! This project uses 4-space indentation !!**

Please do not over-condense code. Slimefun won't run faster just because you used fewer spaces.

We use **Spotless** as our formatting tool. Before submitting, you **must** run `./gradlew spotlessCheck spotlessApply` to auto-format your code; otherwise, the CI will block your PR.

# Contribution Types

You can submit bug fixes, new content, or API improvements.

The fork currently supports API-related contributions, and developers can depend on this English fork via JitPack.
