## Table of Contents

These projects span CI/CD infrastructure, Canvas API automation, internal tooling, and engineering culture — built while maintaining a TypeScript browser extension used by 20 people across our learning technology team.

- [Web Extension Build Pipeline](build-pipeline-automation.md)
- [Course Update Process Automation](canvas-api-process.md)
- [Sprint Summary Write-up Assistant](sprint-summary-script.md)
- [Web Extension Documentaition Expansion](documentation-expansion.md)

## [Web Extension Build Pipeline](build-pipeline-automation.md)

Before this project, publishing the extension was a manual process that depended on remembering every step. I replaced it with a GitHub Actions pipeline that runs tests on every push, builds a testable artifact on every pull request, and handles signing, distribution, and release tagging automatically on merge.

## [Course Update Process Automation](canvas-api-process.md)

Specific materials needed to reach 75+ courses every term in a way that was repeatable and maintainable. I led the discovery process on how Canvas needed to be configured to avoid surfacing materials to the wrong students, then built a one-button automation into our extension that handles the deployment via Canvas API.

## [Sprint Summary Write-up Assistant](sprint-summary-script.md)

Writing a biweekly newsletter for other university teams meant manually piecing together two weeks of sprint work from our Trello board. I built a Python script that pulls the cards, detects keywords, and groups the work into a structured template I can write from directly.

## [Web Extension Documentation Expansion](documentation-expansion.md)

Institutional knowledge about the extension had accumulated in my head with nowhere to live in the codebase. I created a knowledge base markdown file inside the repo to capture the quirks, decisions, and non-obvious details that a new developer would otherwise have to rediscover on their own.
