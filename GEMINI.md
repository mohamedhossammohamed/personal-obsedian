# Gemini Project Context: Obsidian Workflow Template

## Project Overview

This project is a sophisticated **Obsidian Vault Template** designed for personal productivity, knowledge management, and task tracking. It implements methodologies like **PARA** (Projects, Areas, Resources, Archives), **GTD** (Getting Things Done), and **Zettelkasten**.

Unlike a standard Obsidian vault, this project relies heavily on code-based automation using JavaScript, specifically via plugins like **Dataview**, **QuickAdd**, and **Templater**.

### Key Technologies
*   **Obsidian**: The core markdown-based knowledge base.
*   **DataviewJS**: For generating dynamic views (calendars, task lists) using JavaScript (`_Scripts/view.js`).
*   **QuickAdd**: For scripting complex workflows and integrations (`_Scripts/tasksync.js`).
*   **Todoist Plugin**: For synchronizing tasks with external services.
*   **Semantic Release**: Used to version and release this template itself (configured via `package.json`).

## Directory Structure

The vault follows the **PARA** organization method with specific support folders:

*   **`0-Inbox/`**: Entry point for new, unprocessed notes.
*   **`1-Projects/`**: Active projects with defined goals and deadlines.
*   **`2-Areas/`**: Ongoing responsibilities without specific deadlines.
*   **`3-Resources/`**: Topics of interest and reference materials (Zettelkasten).
*   **`4-Archives/`**: Completed or inactive items.
*   **`5-Templates/`**: Markdown templates for Daily Notes, Projects, etc.
*   **`_Scripts/`**: **CRITICAL**. Contains the JavaScript logic that powers the vault's automation.
    *   `tasksync.js`: Functions for syncing/importing tasks from Todoist (used by QuickAdd).
    *   `view.js`: A complex DataviewJS script that renders a custom task calendar/dashboard.
    *   `*.css`: Custom styling snippets.
*   **`_Media/`** & **`_Canvas/`**: Assets and Obsidian Canvas files.
*   **`.obsidian/`**: Configuration directory.
    *   `community-plugins.json`: Lists the extensive set of active plugins (Dataview, QuickAdd, Periodic Notes, etc.).

## Automation & Development

This is a "Code-Enhanced" vault. Changes to the workflow often involve editing JavaScript files in `_Scripts/`.

### Key Scripts
1.  **`_Scripts/tasksync.js`**:
    *   **Purpose**: Bridges Obsidian and Todoist.
    *   **Usage**: Invoked by QuickAdd macros inside Obsidian.
    *   **Exports**: `SelectFromAllTasks`, `GetAllTasksFromProject`, `GetAllTasksFromSection`.
2.  **`_Scripts/view.js`**:
    *   **Purpose**: Renders the "Tasks Calendar" view.
    *   **Usage**: Embed via DataviewJS blocks in markdown files (e.g., `dv.view("_Scripts/view", { ... })`).
    *   **Inputs**: Accepts parameters for view type (month, week), filters, and styling.

### Building & Running
*   **No Build Step**: The vault runs directly in Obsidian.
*   **Package.json**: The `npm` configuration is **only** for the release workflow of this template (using `semantic-release`). It does not run the vault or its scripts.
*   **Testing**: Changes to scripts must be tested manually within Obsidian by triggering the associated command or viewing the note.

## conventions
*   **Markdown First**: Content is stored in `.md` files.
*   **Script Locations**: All executable logic resides in `_Scripts/` rather than scattered in code blocks, to maintain maintainability.
*   **PARA Method**: Strict adherence to the 0-5 folder structure for note organization.
