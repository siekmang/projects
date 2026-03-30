# Course Update Process Automation

Automating the deployment of course materials into 75+ courses per term via a single button per course, replacing a manual process and centralizing updates to a single source of truth.

## The Problem

A new hidden module needed to be introduced into all undergraduate courses in a way that was repeatable, and allowed the module to be changed in one place.

## What I Did

I led the discovery phase on how the process needed to function in Canvas to avoid surfacing the module to students who didn't need to see, and assigning it to specific students when they did need to see it. Then I built a process into our TypeScript extension that used Canvas API calls to automate the steps it would take to get that module into the blueprint for each course. Built in user feedback to make sure the user knows the process is in progress.

## Tools & Technologies

- TypeScript
- Canvas API
- Web Extension

## Outcome

75+ courses every term are setup using this button that takes 1 minute to run the full process, replacing a manual process that would've taken 5+ minutes. This saves hours of learning designer time each year. Having this module in its own template course creates a single source of truth, so when changes need to happen to that module, they can happen in one place and propagate out for the next term.

## What I Learned

This project taught me the value of understanding a system deeply before automating it. Before writing a line of code I had to map out how Canvas handles module visibility and student assignment well enough to design a process that wouldn't surface materials to the wrong people at the wrong time. I got comfortable using browser developer tools to intercept and inspect API calls when I wasn't seeing what I expected to. It also made me think about asynchronous UX. When a process takes a minute to run, the user needs to know it's working.
