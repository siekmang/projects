# Web Extension Documentation Expansion

Reducing the bus factor on our web extension by documenting institutional knowledge into the codebase.

## The Problem

After 8+ months of working on the [extension](https://github.com/Unity-Environmental-University/lxd-tools), I'd become the primary holder of a lot of knowledge that wasn't written down anywhere: specific quirks, decisions, things that just lived in my head because I'd figured them out the hard way. That's a liability. If I'm unavailable, whoever picks this up is starting from a harder place than they need to be.

## What I Did

I created a knowledge base markdown file inside the extension repository as a dedicated place to document the things that aren't obvious from reading the code alone. The specific quirks of the Canvas API, the reasoning behind non-obvious implementation decisions, the things a new developer would otherwise have to rediscover on their own.

## Tools & Technologies

- Markdown
- GitHub

## Outcome

The extension's bus factor is higher than it was. Someone stepping into this codebase now has a starting point that I didn't have when I started.

## What I Learned

I learned how to distinguish what needs to be documented, and how to document it well. How to translate things that have become second nature into concepts that someone with less familiarity can understand.
