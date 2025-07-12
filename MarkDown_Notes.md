- [Creating a Table of Contents (TOC) in Markdown](#creating-a-table-of-contents-toc-in-markdown)
  - [📝 Manual Method (Works Everywhere)](#-manual-method-works-everywhere)
  - [⚙️ Automatic Method (Editor-Specific)](#️-automatic-method-editor-specific)
# Creating a Table of Contents (TOC) in Markdown
## 📝 Manual Method (Works Everywhere)
Use Markdown headings (#, ##, ###, etc.) and create anchor links to them:
```markdown
## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [FAQ](#faq)
```
Then, in your document:
```markdown
## Introduction
Welcome to the guide...

## Installation
Follow these steps...

## Usage
Here's how to use it...

## FAQ
Answers to common questions...
```
🔗 Markdown automatically converts headings into anchors. Just lowercase the heading text and replace spaces with hyphens.
## ⚙️ Automatic Method (Editor-Specific)
VS Code
1. Install the Markdown All in One extension.
2. Open Command Palette (Ctrl+Shift+P or Cmd+Shift+P).
3. Select "Markdown All in One: Create Table of Contents".

It auto-generates and updates the TOC based on your headings.
