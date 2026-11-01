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

> e.g., `resolves #123` or `fix #123`

If the fix is obvious and described in the title, duplication is not necessary.

Supported type prefixes: `(feat(ure)?|fix|docs|style|refactor|ci|chore|perf|build|test|revert|trans)`

Additionally, use the `trans` type for translation-related commits.

# Code Style

**!! This project uses 4-space indentation !!**

Please do not over-condense code. Slimefun won't run faster just because you used fewer spaces.

We use **Spotless** as our formatting tool. Before submitting, you **must** run `./gradlew spotlessCheck spotlessApply` to auto-format your code; otherwise, the CI will block your PR.

# Contribution Types

This fork mainly needs **translation fixes**: wrong, unclear or missing English text in messages, menus, item lore and console output. Bug fixes are welcome too.

New features, larger code changes and API changes are best sent to [SlimefunGuguProject](https://github.com/SlimefunGuguProject/Slimefun4) first, so the Chinese and English builds stay the same. They reach this fork with the next upstream sync. Addon developers should build against the upstream API (see the README).

# License

By submitting a contribution, you agree that it is licensed under the [GNU General Public License v3.0](LICENSE), the same license as the rest of the project. Only submit work you wrote yourself or have the right to share under that license. Keep existing copyright notices and `@author` tags as they are.
