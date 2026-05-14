# Exercise 3: Generate shareable artifacts

In this exercise, you'll use the artifact-focused presentation skills to turn existing talk materials into follow-up content: an annotated write-up, a YouTube description, and a LinkedIn post.

- [Step 1: Review the example input](#step-1-review-the-example-input)
- [Step 2: Generate an annotated write-up](#step-2-generate-an-annotated-write-up)
- [Step 3: Generate a YouTube description](#step-3-generate-a-youtube-description)
- [Step 4: Generate a LinkedIn post](#step-4-generate-a-linkedin-post)
- [Step 5: Review and improve the artifacts](#step-5-review-and-improve-the-artifacts)
- [Step 6: Reflect on the artifact workflow](#step-6-reflect-on-the-artifact-workflow)

---

## Step 1: Review the example input

This repository includes example presentation inputs under `example_inputs/`.

For this exercise, use:

```text
example_inputs/python-agents-session1/presentation.md
```

That file describes a recorded talk and points to the source materials:

- A YouTube video URL
- A slide PDF
- The original talk description

The folder also includes the referenced PDF:

```text
example_inputs/python-agents-session1/PythonAgents-BuildingFirstAgent.pdf
```

---

## Step 2: Generate an annotated write-up

Ask your agent to use the `generate-writeup` skill:

```text
Generate a write-up for example_inputs/python-agents-session1/presentation.md.
Put all generated files under outputs/python-agents-session1/.
```

Depending on your environment, the skill may fetch the transcript, convert the PDF slides into images, extract slide text, outline the slides, and combine those pieces into a final write-up.

When the agent finishes, inspect the output folder. Look for files such as:

- `writeup.md`
- `chapters.txt`
- slide images
- extracted slide text
- transcript files

Review the generated write-up and ask the agent for any desired improvements.

---

## Step 3: Generate a YouTube description

Now reuse the same source materials to create a YouTube video description.

Ask your agent to use the `youtube-description` skill:

```text
Use the youtube-description skill with example_inputs/python-agents-session1/presentation.md and the generated transcript or write-up. Create outputs/python-agents-session1/youtube_description.md with a brief intro, relevant links, and YouTube-clickable timestamps. Put each timestamp at the start of its own line in MM:SS or H:MM:SS format.
```

When the agent finishes, inspect `outputs/python-agents-session1/youtube_description.md`.

Check that:

- The first line clearly describes the talk.
- The timestamps are at the start of their lines.
- The description includes useful related links.
- The tone sounds appropriate for YouTube.

---

## Step 4: Generate a LinkedIn post

Next, create a short social post that points people to the talk or write-up.

Example prompt:

```text
Using example_inputs/python-agents-session1/presentation.md and the generated write-up, create outputs/python-agents-session1/linkedin-post.md with a concise LinkedIn post for developers. Make it specific, useful, and not too salesy.
```

When the agent finishes, inspect `outputs/python-agents-session1/linkedin-post.md`.

Check that:

- It has a strong opening line.
- It mentions a concrete thing the audience will learn.
- It sounds like a person, not a press release.
- It is short enough to read quickly.

---

## Step 5: Review and improve the artifacts

Now compare the three generated artifacts: the write-up, YouTube description, and LinkedIn post.

Ask your agent:

```text
Review outputs/python-agents-session1/writeup.md, outputs/python-agents-session1/youtube_description.md, and outputs/python-agents-session1/linkedin-post.md. Check whether they are accurate, consistent with each other, and appropriate for their formats. Do not edit files yet; give me a prioritized review.
```

Choose one or two improvements, then ask the agent to apply them.

Optional extra artifacts, if you have time:

- A short README for the talk
- A short email announcement
- A list of expected audience questions and answers
- A 5-bullet executive summary
- A clean chapter list for the video

🥳 Congratulations, you now have a small set of shareable artifacts generated from one presentation workflow.


