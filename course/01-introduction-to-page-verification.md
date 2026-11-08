<!-- course-title: Factory Page Check -->
<!-- course-theme: roi-alt-theme -->

<!-- layout: title -->
![ROI Logo](images/roi-logo-with-name.png)

Factory Page Check

# Chapter 1: Introduction to Page Verification

---

# Chapter 1: Objectives

- Confirm the page lists each committed step
- Review an overview of factory page checks
- Inspect local pages in a browser
- Complete the lab verifying local page steps

---

<!-- layout: navigation -->
# Chapter 1

- **Overview of Factory Page Checks**
- Inspecting Local Pages
- Lab: Verifying Local Page Steps

---

# Why Page Verification Matters

- **Automated pipelines**: software factories generate outputs continuously
- **Human confirmation**: automated builds do not guarantee correct rendering
- **Step traceability**: every committed phase must appear on the local view
- **Early detection**: catch missing assets or broken layouts immediately

> [!NOTE]
> Verification bridges the gap between raw code commits and user-facing presentation.

---

<!-- layout: 2-column -->
# Manual Checks vs Automated Validation

### Manual Browser Checks
- Direct visual confirmation
- Catches layout and styling flaws
- Simple for single-page reviews

### Automated Validation
- Scripted health checks and test suites
- Runs in headless CI pipelines
- Fast feedback for regressions

---

# Common Verification Failures

- **Missing outputs**: committed files fail to copy or render on the index
- **Stale cache**: the browser displays an older version of the generated page
- **Broken links**: navigation elements point to missing targets
- **Incorrect ordering**: steps appear out of sequence or hidden

> [!WARNING]
> Always clear browser cache or hard-refresh when testing recent local commits.

---

<!-- layout: navigation -->
# Chapter 1

- Overview of Factory Page Checks
- **Inspecting Local Pages**
- Lab: Verifying Local Page Steps

---

# Inspecting Local Pages in a Browser

- **Local server**: load pages from `file://` or a local development server
- **DOM inspection**: use browser developer tools to verify markup structure
- **Step checklist**: cross-reference rendered items against committed files
- **Responsive review**: verify layout behavior across different viewport sizes

> [!TIP]
> Keep developer tools open while refreshing to monitor network requests and console errors.

---

<!-- layout: 3-column -->
# Browser Verification Tools

### Developer Tools
- Inspect elements and styles
- Trace network load failures
- Monitor JavaScript console output

### Local File Preview
- Quick opening of static HTML
- Useful for immediate feedback
- Minimal setup required

### Local Web Server
- Mimics production hosting
- Handles relative paths correctly
- Prevents security restriction surprises

---

# Verifying Committed Steps

- **Traceability**: verify that every file in the repository maps to a visible list item
- **Incremental checks**: inspect the page after each major build step
- **Asset validation**: confirm images, stylesheets, and links load correctly

```html
<!-- Example expected list item structure -->
<ul class="step-list">
  <li class="completed">Step 1: Repository Initialization</li>
  <li class="active">Step 2: Page Verification</li>
</ul>
```

---

<!-- layout: navigation -->
# Chapter 1

- Overview of Factory Page Checks
- Inspecting Local Pages
- **Lab: Verifying Local Page Steps**

---

# Verifying Local Page Steps

Lab link: TODO

---

# What You Learned

- Confirmed the page lists each committed step
- Reviewed an overview of factory page checks
- Inspected local pages in a browser
- Completed the lab verifying local page steps

---

# Quiz 1 of 3

**Why is human browser verification necessary even when automated pipeline builds pass?**

- A. Automated builds cannot compile HTML files
- B. Automated builds do not guarantee correct visual rendering and layout
- C. Browsers require manual execution for every file write
- D. Pipeline runners delete committed assets automatically

---

# Quiz 1: Answer

**Why is human browser verification necessary even when automated pipeline builds pass?**

**Correct: B.** Automated builds do not guarantee correct visual rendering and layout

- Pipeline success indicates task execution, not correct presentation
- Visual flaws, broken styles, or missing elements require browser review
- Human verification catches subtle integration issues that tests miss
- Combining automated checks with browser reviews ensures end-to-end quality

---

# Quiz 2 of 3

**What is a common pitfall when inspecting rapidly changing local web pages?**

- A. Browser caching displaying an older version of the generated page
- B. Developers using developer tools too frequently
- C. Local development servers running too fast
- D. Markdown files automatically converting to plain text

---

# Quiz 2: Answer

**What is a common pitfall when inspecting rapidly changing local web pages?**

**Correct: A.** Browser caching displaying an older version of the generated page

- Browsers often cache static assets aggressively
- Stale cache can make it appear as though a committed step is missing
- Hard-refreshing or disabling cache during development prevents false alarms
- Verifying file timestamps helps confirm the correct version is loaded

---

<!-- layout: 2-column -->
# Quiz 3 of 3: Discussion

### Prompt
You refresh your local page after committing a new factory step, but the list does not show the update.

### Discuss
- What are the first three troubleshooting checks you perform?
- How do you distinguish a build error from a browser caching issue?
- What validation step prevents this confusion in future workflows?

---

<!-- layout: 2-column -->
# Quiz 3: Discussion Points

**You refresh your local page after committing a new factory step, but the list does not show the update.**

### Strong Answers Mention
- Checking file paths and build output locations
- Performing a hard refresh or clearing browser cache
- Inspecting terminal logs for silent pipeline or generation errors
- Establishing automated validation for file existence before rendering

### Watch For
- Assuming the code committed itself without verifying local file state
- Restarting the entire computer instead of checking browser cache
- Ignoring console errors or missing asset warnings

---

# Questions and Answers

Questions?
