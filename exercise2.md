# Exercise 2: Create and theme a slide deck

In this exercise, you'll use an AI coding agent plus presentation skills to create a small RevealJS slide deck from a Markdown plan, explore ASCII slide mockups, and theme the deck in a creative direction.

- [Step 1: Create a topic plan](#step-1-create-a-topic-plan)
- [Step 2: Generate the first RevealJS deck](#step-2-generate-the-first-revealjs-deck)
- [Step 3: Theme the deck creatively](#step-3-theme-the-deck-creatively)
- [Step 4: Generate ASCII mockup slide ideas](#step-4-generate-ascii-mockup-slide-ideas)
- [Step 5: Iterate on the deck](#step-5-iterate-on-the-deck)
- [Step 6: Review your result](#step-6-review-your-result)

---

## Step 1: Creat a topic plan

Create a file named `plan.md` in the root of your workspace. You can either copy an example plan or make your own.

### Use an example plan

Choose one of these ready-made example plans:

- [How Python list comprehensions work](example_inputs/mini-talk-plans/python-list-comprehensions.md)
- [Three ways to make a Python web app](example_inputs/mini-talk-plans/python-web-apps.md)
- [Intro to vector search](example_inputs/mini-talk-plans/vector-search.md)
- [What I learned from a favorite hobby](example_inputs/mini-talk-plans/favorite-hobby.md)

To use one of the example plans, copy it into `plan.md`. For example:

```bash
cp example_inputs/mini-talk-plans/python-list-comprehensions.md plan.md
```

### Make your own plan

Choose a topic you could explain in 3 to 5 minutes. Pick something small enough that you can recognize whether the generated slides are accurate.

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

Now ask your agent:

```text
Please improve plan.md for a 3-5 minute mini talk. Keep it concise, practical, and beginner-friendly. Add speaker-note guidance for what I should say on each slide.
```

Review the updated plan. Edit anything that does not sound like you.

---

## Step 2: Generate the first RevealJS deck

Ask your agent:

```text
Create a RevealJS slide deck from plan.md. Make 4-6 slides, include speaker notes, and keep the HTML/CSS easy to edit. Put the deck in slides.html.
```

When the agent finishes, ensure that it used `make-revealjs-presentation` and inspect the files it created.

Open `slides.html` in a browser. You can usually open the file directly, or you can start a local server from the workspace root:

```bash
npx serve .
```

Or, with Python:

```bash
python3 -m http.server
```

If you use a local server, open the local URL that it prints.

Do a quick first pass:

- Does the slide order match your plan?
- Is the talk the right duration?
- Is there one concrete example?
- Are the speaker notes useful?

Do not polish yet. The first deck is just a real artifact to react to.

---

## Step 3: Theme the deck creatively

Now make the deck feel memorable. Pick a theme that is specific, visual, and connected to your topic or personality.

You can choose something practical:

- An existing conference website
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
- A map from a fantasy quest
- A field guide for tiny discoveries

Choose a direction, then ask your agent to apply it:

```text
Apply the [chosen theme] direction to slides.html. Keep the slides readable in a classroom, avoid overcrowding, and preserve the speaker notes. After editing, tell me what changed.
```

You can also ask the agent to match an existing conference website:

```text
Theme slides.html to visually match [conference website URL]. Use the site's colors, typography direction, spacing, and visual style as inspiration, but keep the slides readable and avoid copying any copyrighted images or logos unless they are clearly intended for speaker use.
```

Open the deck again and look at the result.

This is the most creative part of the exercise. Try making the deck feel like something only you would have asked for.

---

## Step 4: Generate ASCII mockup slide ideas

After choosing a theme, ask the agent to sketch layout options using ASCII. This keeps the design conversation fast and low-stakes before the agent edits HTML and CSS.

Pick one slide that feels important, such as the example slide, title slide, or final takeaway slide.

Ask your agent:

```text
Before editing files, mock up 3 different ASCII layout ideas for the most important slide in slides.html. Make the options meaningfully different, and briefly explain when each layout would work best.
```

If you already know which slide needs work, be more specific:

```text
Before editing files, mock up 3 different ASCII layout ideas for the concrete example slide. I want one option that is diagram-heavy, one that is comparison/table-based, and one that is minimal and presenter-focused.
```

Choose your favorite mockup, then ask the agent to apply it:

```text
Apply the second ASCII mockup to the example slide in slides.html. Keep the deck readable and preserve the speaker notes.
```

Open the deck again and check whether the slide is easier to explain.

---

## Step 5: Iterate on the deck

Now make one or two small improvements based on what you see in the browser.

Pick prompts that fit your deck:

```text
Make the title slide more visually distinctive while keeping it readable.
```

```text
Make the example slide easier to understand at a glance.
```

```text
Give me 5 ideas for a better title for Slide N.
```

```text
Reduce the amount of text on each slide and move extra explanation into speaker notes.
```

```text
Make the theme more specific and less generic. Keep the existing structure, but add stronger visual details that match [your theme].
```

```text
Check the deck for text that might overflow or be hard to read on a projector, then fix the highest-risk slide.
```

After each edit, reopen or refresh the deck and inspect the result.

---

## Step 6: Review your result

Do a quick content and delivery review.

Ask your agent:

```text
Open slides.html in the integrated browser in VS Code and review the deck visually and editorially. Check for accuracy, style, accessibility, readability, text overflow, contrast, layout issues, and whether the deck still matches plan.md. Do not edit files yet; give me a prioritized review.
```

Look through the issues, tell the agent which ones to address and which to ignore.

🎉 Congratulations, you now have a themed, reviewed slide deck built from an AI-assisted presentation workflow.

