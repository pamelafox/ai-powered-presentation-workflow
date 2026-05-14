# Exercise 3: Generate shareable artifacts

In this exercise, you'll use the artifact-focused presentation skills to turn existing talk materials into follow-up content such as an annotated write-up, YouTube description, slide outline, transcript-based summary, or social post.

- [Step 1: Choose an example input](#step-1-choose-an-example-input)
- [Step 2: Inspect the presentation metadata](#step-2-inspect-the-presentation-metadata)
- [Step 3: Generate an annotated write-up](#step-3-generate-an-annotated-write-up)
- [Step 4: Review and improve the artifact](#step-4-review-and-improve-the-artifact)
- [Step 5: Generate one smaller artifact](#step-5-generate-one-smaller-artifact)
- [Step 6: Reflect on the artifact workflow](#step-6-reflect-on-the-artifact-workflow)

---

## Step 1: Choose an example input

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

Those inputs are enough for the agent to try the `generate-writeup` workflow.

---

## Step 2: Inspect the presentation metadata

Open `example_inputs/python-agents-session1/presentation.md` and read it.

Ask your agent:

```text
Read example_inputs/python-agents-session1/presentation.md and summarize what source materials are available for generating follow-up artifacts. Do not create files yet.
```

Confirm that the agent noticed the video URL, slide PDF, and original description.

---

## Step 3: Generate an annotated write-up

Ask your agent to use the `generate-writeup` skill:

```text
Use the generate-writeup skill with example_inputs/python-agents-session1/presentation.md. Generate an annotated blog-style write-up from the available slides, video transcript, and talk description. Put all generated files under outputs/python-agents-session1/.
```

Depending on your environment, the skill may fetch the transcript, convert the PDF slides into images, extract slide text, outline the slides, and combine those pieces into a final write-up.

When the agent finishes, inspect the output folder. Look for files such as:

- `writeup.md`
- `chapters.txt`
- slide images
- extracted slide text
- transcript files

If the full workflow cannot complete, ask for a smaller version:

```text
The full write-up workflow did not complete. Use the files that are available in example_inputs/python-agents-session1/ to create outputs/python-agents-session1/writeup-draft.md with a clear summary, slide-by-slide outline, and suggested sections for a future annotated write-up.
```

---

## Step 4: Review and improve the artifact

Open the generated write-up or draft.

Ask your agent:

```text
Review outputs/python-agents-session1/writeup.md as an audience-facing artifact. Check whether it has a clear introduction, accurate section headings, useful slide annotations, and a concise conclusion. Do not edit files yet; give me prioritized suggestions.
```

If your generated file has a different name, replace `writeup.md` in the prompt.

Pick one suggestion and ask the agent to apply it:

```text
Apply the highest-impact improvement to the generated write-up. Keep the tone practical and useful for developers who missed the live session.
```

---

## Step 5: Generate one smaller artifact

Now reuse the same source materials to create one smaller artifact.

Choose one:

- A short README for the talk
- A LinkedIn post
- A short email announcement
- A list of expected audience questions and answers
- A 5-bullet executive summary
- A chapter list for the video
- A YouTube description with clickable timestamps

Example prompt:

```text
Using example_inputs/python-agents-session1/presentation.md and the generated write-up, create outputs/python-agents-session1/linkedin-post.md with a concise LinkedIn post for developers. Make it specific, useful, and not too salesy.
```

Or:

```text
Using example_inputs/python-agents-session1/presentation.md and the generated write-up, create outputs/python-agents-session1/qa.md with 8 likely audience questions and concise answers.
```

Or:

```text
Using the transcript or generated write-up, create outputs/python-agents-session1/chapters-clean.md with a clean chapter list for the video.
```

Or use the `youtube-description` skill:

```text
Use the youtube-description skill with example_inputs/python-agents-session1/presentation.md and the generated transcript or write-up. Create outputs/python-agents-session1/youtube_description.md with a brief intro, relevant links, and YouTube-clickable timestamps. Put each timestamp at the start of its own line in MM:SS or H:MM:SS format.
```

Review the result and make one small improvement.

---

## Step 6: Reflect on the artifact workflow

Write down short answers to these questions:

```markdown
## Exercise 3 reflection

1. Which source material was most useful: slides, transcript, video metadata, or original description?
2. What did the generated artifact get right?
3. What did you need to correct, verify, or rewrite?
4. Which smaller artifact would be most useful after one of your own talks?
5. What would you want to automate next time?
```

The bigger workflow is the same as the deck workflow: preserve your presentation materials, let the agent assemble a first artifact, then use your judgment to review and improve it.
