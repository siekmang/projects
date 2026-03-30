# Web Extension Build Pipeline

Replacing a manual, error-prone publish process with a fully automated CI/CD pipeline for a browser extension serving 20 users.

## The Problem

Our learning deisng extension was a fully manual process that was prone to human error. A developer could easily forget to run unit tests, bump the package number, or pull the most recent changes before running the publish script and be left with a new version of the extension that didn't work or didn't feature changes that were expected.

## What I Did

I started by building a workflow with GitHub Actions that ran the unit tests, type checking, and a linter on every push to any branch. This alerted the developer responsible for the push if anything failed. Then I built a workflow that built the extension on every opened pull request and commented a link to the build, so non-developers could download the build and test it without needing to build the extension themselves. Finally, I worked with the sysadmin to implement a workflow that signed the extension for both Chrome and Firefox, and uploaded the necessary files to a Cloudflare R2 bucket using the AWS S3 API so a group policy could be deployed on user computers that keeps the extension updated. This workflow runs on a merged pull request to the main branch, with that PR having to pass a version check to make sure the version number gets bumped in `package.json` before merging. The merge workflow also culls the files older than the 5th most recent to reduce bucket bloat, sends the built extension to our backup build repo, tags the release, and creates a new release branch for the next cycle.

## Tools & Technologies

- GitHub Actions
- Cloudflare R2 Bucket
- AWS S3 API
- TypeScript

## Outcome

20 users now have an extension that stays updated on their computers. GitHub runs checks to make sure the code is up to quality standards. The build process is now less susceptible to human error.

## What I Learned

Before this project, I had a basic understanding of CI/CD as a concept but had never built a pipeline. Working through GitHub Actions taught me more about triggers and dependencies — and the usefulness of chokepoints in the process. Integrating with Cloudflare R2 via the S3 API was my first hands-on experience with cloud storage, and this was my first time thinking about extension distribution concepts like signing.
