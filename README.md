# test-governance

[English](README.md) | [简体中文](README_zh.md)

Keep tests maintained as the product changes. This Codex skill prioritizes existing suites, shared fixtures and runners, removes redundant coverage when justified, retires obsolete tests, and controls generated artifacts.

Use it for test planning, implementation, execution and cleanup, and for reviewing test impact during feature changes, version upgrades, interface changes and architectural refactoring. Test code stays in source files; one authoritative testing document explains coverage and execution.

## Copy to Codex: install the skill

Send the entire prompt below to Codex. Let it download, install and verify the skill without manually extracting or moving folders.

```text
Install the test-governance skill for me from https://github.com/KiriuKazurei/test-governance. Complete the download, installation and verification.

Download test-governance.zip from the latest stable GitHub Release:
https://github.com/KiriuKazurei/test-governance/releases/latest/download/test-governance.zip

First inspect the release tag and asset metadata and record the installation source. Verify the downloaded SHA256 if a digest is provided. Use a temporary directory dedicated to this installation; check that archive entry paths and links cannot escape it before extracting. Inspect SKILL.md, agents/openai.yaml and the documentation.

Determine the user-level skill directory that this Codex environment actually discovers, then install the complete test-governance folder there. Use the current environment and official documentation rather than copying the author's username or paths. Do not assume that the skills directory must be inside CODEX_HOME. If a skill with the same name already exists, check its source and local modifications first, then report whether it already meets the requirements or needs updating. Before replacement, preserve a recoverable copy and avoid overwriting unreviewed local modifications.

Read the installed SKILL.md and agents/openai.yaml. Verify that the name is test-governance, the files are complete and readable, and implicit invocation has not been disabled. Report the actual installation path, release tag and verification results. If the current session cannot refresh its skill list, explain that Codex must be restarted or a new session opened before verifying discovery; do not claim that future loading has already been verified.

Limit this task to downloading, installing and verifying this skill. Preserve other skills and global instructions, and do not run project tests or clean historical data. Remove temporary download and extraction files created by this installation once it is complete. I will then use the separate README prompt to configure mandatory use across all projects.
```

See the [official skills documentation](https://learn.chatgpt.com/docs/build-skills) for discovery and refresh behavior. Installing a skill does not itself require Codex to use it for every relevant task; complete the global configuration below.

## Copy to Codex: enable across all projects

After installation, send the entire prompt below once so Codex records the rule in your effective global instructions. Saying “always use this” in one chat is not a substitute for persistent configuration.

```text
Configure the installed $test-governance skill as my test governance rule across all projects, not just this conversation.

First check the available skills, locate test-governance and read its SKILL.md. Record the actual installation path rather than copying another person's username or directory. If the skill cannot be found, report that it is missing; do not claim it has been enabled.

Locate the actual Codex home directory: use CODEX_HOME when set, otherwise ~/.codex. Read the existing global AGENTS.md. If a non-empty AGENTS.override.md exists, write the rule into that effective override rather than only editing an ignored file. Preserve existing content, and add or update a single test-governance block. Repeated configuration must not create duplicate blocks. Do not traverse and modify AGENTS.md in all my repositories.

Add the following requirements to the effective global instructions, including the verified skill path:

In every project, before choosing how to maintain or run tests, read and follow $test-governance whenever work involves test planning, writing, execution or cleanup, or reviewing the test impact of feature changes, bug fixes, version upgrades, interface changes, architectural changes or refactoring. Prefer maintaining existing suites, shared fixtures, runners and the project's authoritative testing document. A new suite needs a distinct, lasting coverage responsibility; do not create a separate suite per task and abandon the old ones. Major changes must review affected tests for retention, updates, consolidation, retirement and missing coverage. Consolidate temporary reproduction scripts or remove them within authorization; document the purpose and next action for anything that must remain. Follow each project's own artifact locations, storage limits and archive rules rather than copying one project's numbers everywhere. Clearly distinguish passing, failing, unexecuted and pending human acceptance results.

These requirements do not override my explicit task scope or applicable project instructions and do not require new tests for low-impact changes. They do not grant additional permission to run programs, install dependencies, call paid or external services, delete files or clean business data. Resolve conflicts according to instruction priority and the applicable scope, and explain conflicts when needed.

For this task, only configure and verify the rule. Do not start project tests, repository-wide refactoring or historical cleanup. Report the actual skill path, the global instruction file changed and the added rule. Explain if a new session or restart is required. Do not describe a written rule as proof that its behavior has been verified in every project.
```

Global instructions default to `~/.codex/AGENTS.md` and can be affected by `CODEX_HOME` and a global `AGENTS.override.md`. Project instructions also participate in the instruction chain. Verify actual loading in a new session after changing configuration. See the [official global instructions guide](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

## Verify configuration

Send this in a new Codex session in any project:

```text
Only verify the test governance configuration; do not run tests or modify the project. List the global and project instruction files actually loaded in this session. Confirm whether they require $test-governance for relevant testing work, then read the skill and identify the existing project test entry point you would maintain for the next test change. Report missing configuration, the skill or a project test entry point honestly.
```

For one-time use, send: `Use $test-governance to maintain the tests affected by this change, prioritizing existing suites and testing documentation.`

## Scope

This is an agent workflow, without a test framework, automatic cleanup program or enforcement hook. It does not prescribe a language, operating system, storage limit or versioned output directory, and it does not replace CI gates. Test execution, cleanup scope and external service access remain subject to user authorization and project rules.
