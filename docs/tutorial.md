# Tutorial: Build an AI-powered presentation workflow

In this 40-minute tutorial, you will use GitHub Copilot in VS Code plus the presentation agent skills from [pamelafox/presentation-skills](https://github.com/pamelafox/presentation-skills) to create, style, review, and share a short slide deck.

Your goal is not to make a perfect conference talk. Your goal is to experience the workflow:

1. Plan the talk in Markdown.
2. Generate a first slide deck.
3. Theme it in a creative direction.
4. Iterate on content and layout.
5. Review the deck for accuracy.
6. Prepare a shareable follow-up artifact.

By the end, you should have a small RevealJS presentation and a repeatable workflow you can reuse for your own teaching, talks, demos, or workshops.

## What you need

- A GitHub account.
- [VS Code](https://code.visualstudio.com/) installed.
- Access to GitHub Copilot.
- [Node.js](https://nodejs.org/) installed, so that `npx` is available.
- A topic you might teach in 3 to 5 minutes.

Good tutorial topics are small and concrete, for example:

- "How Python list comprehensions work"
- "Three ways to debug a web app"
- "Intro to vector search"
- "How to make a great README"
- "What I learned from a favorite hobby"

Pick something you know enough about to notice when the agent gets it wrong.

## Suggested timing

| Time | Activity |
| --- | --- |
| 0:00-0:05 | Set up Copilot and install skills |
| 0:05-0:10 | Create a Markdown presentation plan |
| 0:10-0:18 | Generate a first RevealJS deck |
| 0:18-0:27 | Apply a creative theme and iterate |
| 0:27-0:34 | Review the deck for accuracy |
| 0:34-0:40 | Create a shareable follow-up artifact and reflect |

If setup takes longer, skip the final follow-up artifact and focus on the plan, deck, theme, and review loop.

## Step 1: Set up GitHub Copilot in VS Code

1. Open VS Code.
2. Open the Copilot Chat side panel. If it is not already open, use the "Toggle Chat" icon at the top of VS Code.
3. If this is your first time using GitHub Copilot, accept the usage terms when prompted.
4. Make sure the chat is in **Agent** mode. You may see the word "Agent", or you may need to click the mode selector / loop icon and choose Agent.
5. Send this test message:

   ```text
   Hello! Please reply with one sentence confirming that you can help me edit files in this workspace.
   ```

6. Confirm that Copilot responds.

During this tutorial, keep Copilot in Agent mode so it can create and edit files in your workspace.

## Step 2: Install the presentation skills

Open a terminal and run:

```bash
npx skills add pamelafox/presentation-skills
```

That installs the full presentation skill collection, including skills for creating RevealJS decks, reviewing presentations, extracting slide text, converting slide formats, and generating write-ups.

If you only want the two most relevant skills for this tutorial, you can install them individually instead:

```bash
npx skills add pamelafox/presentation-skills/make-revealjs-presentation
npx skills add pamelafox/presentation-skills/review-presentation
```

After installation, restart VS Code or reload the window if Copilot does not appear to discover the new skills.

Then ask Copilot:

```text
What presentation-related agent skills are available to you? Do you see a skill for making RevealJS presentations?
```

You do not need to memorize the skill names. The point of a skill is that the agent can discover and load the right instructions when your task matches.

## Step 3: Create a tutorial workspace

Create a new folder for your work, then open it in VS Code. For example:

```bash
mkdir my-ai-presentation
cd my-ai-presentation
code .
```

Create a file named `plan.md`.

Paste this starter plan into `plan.md`, replacing the bracketed text with your topic:

```markdown
# Mini talk plan: [Your topic]

## Audience

[Who is this for? What do they already know?]

## Goal

By the end, the audience should understand [one clear takeaway].

## Constraints

- 3 to 5 minutes
- 4 to 6 slides
- Include one concrete example
- Use simple speaker notes

## Draft outline

1. Why this topic matters
2. The core idea
3. A concrete example
4. Common mistake or misconception
5. Final takeaway
```

Now ask Copilot:

```text
Please improve plan.md for a 3-5 minute mini talk. Keep it concise, practical, and beginner-friendly. Add speaker-note guidance for what I should say on each slide.
```

Review the changes. Edit anything that does not sound like you.

## Step 4: Generate the first RevealJS deck

Ask Copilot:

```text
Use the make-revealjs-presentation skill to create a RevealJS slide deck from plan.md. Make 4-6 slides, include speaker notes, and keep the HTML/CSS easy to edit. Put the deck in docs/index.html.
```

When Copilot finishes, inspect the files it created.

If it created a `docs/index.html`, open it in a browser. You can usually open the file directly, or you can start a simple local server from the workspace root:

```bash
npx serve docs
```

If you use `serve`, open the local URL that it prints.

Do a quick first pass:

- Does the slide order match your plan?
- Is the talk short enough?
- Is there one concrete example?
- Are the speaker notes useful?

Do not polish yet. The first deck is just a real artifact to react to.

## Step 5: Theme the deck creatively

Now make the deck feel memorable. Pick a theme that is specific, visual, and connected to your topic or personality.

You can choose something practical:

- A conference brand
- A university department
- A product documentation style
- A clean classroom whiteboard

Or something more playful:

- Retro arcade
- Botanical field notebook
- Space mission control
- Punk zine
- Museum exhibit labels
- Train station signage
- Cozy cooking show

Ask Copilot for options first:

```text
Give me 5 creative visual theme directions for this deck. For each one, include a color palette, font direction, layout style, and why it fits the topic. Do not edit files yet.
```

Choose one direction, then ask Copilot to apply it:

```text
Apply the [chosen theme] direction to docs/index.html. Keep the slides readable in a classroom, avoid overcrowding, and preserve the speaker notes. After editing, tell me what changed.
```

Open the deck again and look at the result.

Now try one small iteration prompt. Pick the one that fits your deck, or write your own:

```text
Make the title slide more visually distinctive while keeping it readable.
```

```text
Make the example slide easier to understand at a glance.
```

```text
Reduce the amount of text on each slide and move extra explanation into speaker notes.
```

```text
Mock up 3 alternate layouts for the example slide using ASCII diagrams before editing files.
```

Creativity is encouraged here. The best results usually come from giving the agent taste-level direction, then reacting to the rendered deck.

## Step 6: Review the deck for accuracy

Agents are helpful collaborators, but they can still invent details or oversimplify. Treat review as a required part of the workflow.

Ask Copilot:

```text
Use the review-presentation skill to review docs/index.html for accuracy, clarity, and consistency with plan.md. Look for unsupported claims, confusing examples, and places where the speaker notes should clarify the slide. Do not edit files yet; give me a prioritized review.
```

Read the review. Pick the most important issue, then ask Copilot to fix it:

```text
Please fix the highest-priority issue from your review. Keep the deck concise and preserve the current visual theme.
```

If your deck includes technical claims, ask for a stricter check:

```text
List every technical claim in the deck that should be verified against documentation or source code. For each claim, say whether it is safe, uncertain, or should be rewritten.
```

This is the part of the workflow that protects your credibility. Fast slides are useful only if the final deck is trustworthy.

## Step 7: Create a shareable follow-up artifact

If you have time, use the deck and plan to make one small post-talk artifact.

Choose one:

- A short README for the talk
- A blog-style summary
- A one-page handout
- A LinkedIn post
- A list of audience Q&A you expect

Example prompt:

```text
Create docs/summary.md as a short audience-facing summary of this mini talk. Include the main takeaway, 3 bullet points, and one suggested next step. Base it on plan.md and docs/index.html.
```

Or:

```text
Create docs/linkedin-post.md with a concise post about this mini talk. Make it specific, useful, and not too salesy.
```

The larger pattern is that your deck, plan, notes, and review history become reusable context for everything you make after the talk.

## Step 8: Reflect on the workflow

Before you leave, write down short answers to these questions:

```markdown
## Reflection

1. What did the agent help with most?
2. What did you need to correct or steer?
3. What theme did you choose, and why?
4. What would you add to your own reusable presentation workflow?
```

If you want to keep improving the deck after the tutorial, try these next prompts:

```text
Add an AGENTS.md file with slide design preferences for future presentation work in this repo.
```

```text
Turn this mini talk into a 10-minute version with a stronger example and one audience exercise.
```

```text
Generate a checklist I can use before presenting this deck live.
```

## Troubleshooting

### Copilot cannot find the skills

Run the install command again:

```bash
npx skills add pamelafox/presentation-skills
```

Then reload VS Code and ask Copilot what skills it can see.

### The generated deck is too plain

Ask for visual options before asking for edits. For example:

```text
Before editing files, propose 5 much more distinctive visual directions for this deck. Make them specific and varied.
```

### The generated deck is too busy

Ask Copilot to simplify:

```text
Simplify the deck visually. Use fewer colors, less text per slide, and more whitespace. Move extra detail into speaker notes.
```

### The deck has factual errors

Pause the design work and review the content:

```text
Audit the deck for factual accuracy. For anything uncertain, suggest safer wording instead of making a stronger claim.
```

### You are running out of time

Aim for this minimum finish line:

- `plan.md` exists.
- `docs/index.html` exists.
- The deck has a visible theme.
- At least one review issue has been fixed.

That is enough to experience the workflow.
