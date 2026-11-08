# Verifying Local Page Steps

## Time Required

20 minutes

## Overview

In this lab, you inspect and verify local factory pages in a browser to confirm that every committed step renders correctly. You use browser developer tools to inspect elements, check network logs, and cross-reference rendered items against repository files.

### You learn how to:
- Open and inspect local web pages in a browser.
- Use developer tools to verify DOM structure and troubleshoot layout issues.
- Cross-reference committed repository files against visible page steps.
- Perform hard refreshes to bypass stale browser cache.

## Scenario

Your factory pipeline has committed several new steps to the project repository. Before releasing them, you need to ensure that the local page correctly renders each step and that no assets or layout items are missing.

## Lab Instructions

### Task 1: Open and inspect the local page

In this task, you open the local page in your browser and prepare developer tools for inspection.

1. Open your browser and navigate to your local workspace page or open the static index file.

2. Open the browser developer tools by pressing `F12` or right-clicking anywhere on the page and selecting **Inspect**.

3. Select the **Elements** tab to view the live Document Object Model (DOM) structure.

> [!NOTE]
> Keeping developer tools open helps you immediately spot missing styles or unrendered markup elements.

<!-- TODO IMAGE: Browser developer tools showing elements tab and local page structure -->
![Browser developer tools inspection](images/inspector-view.png)

### Task 2: Cross-reference committed steps

In this task, you compare the list of committed steps in your repository with the items rendered on the local page.

1. Review the step list rendered on your local page.

2. Verify that each committed step from your repository appears in the correct order.

3. Check for any missing outputs or broken list items.

> [!IMPORTANT]
> Every committed factory step must have a corresponding visible entry on the page.

### Task 3: Troubleshoot caching and verify network assets

In this task, you verify that stylesheets and assets load correctly and handle any stale cache issues.

1. Navigate to the **Network** tab in your developer tools.

2. Perform a hard refresh (such as `Ctrl+Shift+R` on Windows/Linux or `Cmd+Shift+R` on macOS) to bypass cached assets.

3. Verify that all network requests return status code `200 OK` without missing files or broken links.

> [!TIP]
> Disabling cache in the Network tab while developer tools remain open prevents stale rendering during iterative checks.

## Congratulations!

In this lab, you have:
- Opened and inspected local web pages in a browser.
- Used developer tools to verify DOM structure and troubleshoot layout issues.
- Cross-referenced committed repository files against visible page steps.
- Performed hard refreshes to bypass stale browser cache.
