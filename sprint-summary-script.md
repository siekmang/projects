# Sprint Summary Write-up Assistant

A [Python script](https://github.com/siekmang/trello-reporting-tool) that pulls from a Trello board and generates a structured summary template, making a recurring task faster and less dependant on memory.

## The Problem

Our learning technology team started sending a sprint summary newsletter to keep other university teams informed on what we were working on. Writing it meant switching back and forth between the newsletter draft and our Trello board, manually pulling out what was worked on and trying to remember context for projects the writer didn't actually work on.

## What I Did

I built a Python script that connects to the Trello API, pulls the cards from our sprint board, detects recurring keywords, and groups cards accordingly. The output is a structured template I can open in my IDE and use as a starting point for drafting the newsletter.

## Tools & Technologies

- Python
- Trello API
- PyCharm

## Outcome

Every two weeks when it's time to write the summary, I run the script instead of scrolling through Trello trying to piece together what happened. The grouping gives me a structure to write from, and the keyword detection surfaces patterns I might not have noticed otherwise.

## What I Learned

This was a small project but it was the first time I built something specifically to make my own recurring work easier. Figuring out how to structure the keyword detection so the groupings were actually useful — rather than just technically correct — required more thought than I expected.
