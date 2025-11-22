---
description: AI rules derived by SpecStory from the project AI interaction history
globs: *
---

---
description: AI rules derived by SpecStory from the project AI interaction history
---

# Copilot Instructions for Cognitive Archaeology Tribunal

## HEADERS

## TECH STACK

- Python 3.14.0
- Trunk

## PROJECT DOCUMENTATION & CONTEXT SYSTEM

## CODING STANDARDS

- When creating fenced code blocks in Markdown, always specify a language for syntax highlighting and accessibility. Use identifiers like `text`, `bash`, or `plaintext` for directory structures, `python` for Python code, `json` for JSON data, `yaml` for YAML configuration, and `markdown` for nested Markdown examples.
- Avoid multiple top-level H1 headings in Markdown documents (MD025). Convert subsequent H1 headings to H2 or lower levels as appropriate.
- Ensure headings within a Markdown document have unique content (MD024). Modify duplicate headings to be distinct.

## WORKFLOW & RELEASE RULES

- When conversation preservation is required, follow the "Preservation Execution Checklist" in the cognitive-os-master-plan repository. This includes: exporting conversation via chatgpt-exporter, uploading the JSON to cognitive-os-master-plan/planning-conversations/, creating required GitHub issues for each planned repo, posting the architecture discussion to ivi374forivi/.github discussions, linking the master plan from all planned repos, and updating the main README. Mark statuses to track completion.
- If AI conversation exports are required for a task, and the exports are incomplete or missing, prioritize obtaining fresh exports before proceeding. Follow these steps:
    - **ChatGPT Export:**
        ```bash
        # 1. Go to https://chat.openai.com/
        # 2. Settings → Data Controls → Export Data
        # 3. Wait 24-48 hours for email
        # 4. Download and extract to a known location
        ```
    - **Claude Export:**
        ```bash
        # 1. Go to https://claude.ai/settings
        # 2. Look for data export option
        # 3. Alternative: Use chatgpt-exporter tool from your personal repos
        ```
    - **Gemini Export:**
        ```bash
        # 1. Go to Google Takeout: https://takeout.google.com/
        # 2. Select only "Gemini Apps Activity"
        # 3. Download when ready
        ```
    - While waiting for AI exports, proceed with tasks that do not depend on them. For example, Tier 1 fork integrations as outlined in `INTEGRATION_QUEUE.md`.

## DEBUGGING

- When debugging GitLens Launchpad, check GitHub authentication, pull request data, and extension settings.
- When debugging the Local History extension, and if problems persist, uninstall the extension entirely. If the extension is enabled, set the limit to 0 days, the save delay to 0, and the path to empty.
- Do not format or debug configuration dot files/folders (`.venv` and other hidden config directories).