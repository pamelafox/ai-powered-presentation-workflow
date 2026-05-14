Lightning Talk: Your Slides, But Faster: Building an AI-powered presentation workflow

Description: (This is the original description, we could deviate fom this slightly)

I love putting together presentations to teach new technology, but when you’re building talks constantly, the prep work adds up fast. In this talk, I will share the many ways that I've been using LLM-powered agents, like GitHub Copilot, for automation and collaboration during the process of making a presentation.

We will start at the beginning, with planning the presentation, using a markdown file as a shared plan between human and agent. With the plan in place, we can generate the presentation, like as a Reveal.JS slide deck (very LLM-friendly) or as a PowerPoint deck (not so much). As we iterate on the presentation, we can continually audit it for accuracy, asking the agent to check its accuracy against documentation and code samples. When we're ready for finishing touches, we can prompt the agent to style the presentation to match a theme or brand, and even ask for multiple design options so we can pick our personal favorite. Finally, after we deliver our polished and accurate presentation, we will use an agent to generate multiple forms of sharing the presentation, like annotated slides and high-level summaries.

Outline:

1. Hook: Presentation prep is secretly a workflow problem (0:00-0:30)
	- Open with the recurring pain: every talk needs planning, drafting, checking, styling, and follow-up materials.
	- Frame the big idea: an AI agent is most useful when it shares the whole workflow, not just one prompt.
	- Visual: compact workflow diagram showing the hidden work around a talk: plan, draft, check, style, share. Avoid screenshots here; the opening needs instant recognition, not tiny UI details.

2. Start with a shared plan (0:30-1:15)
	- Use a markdown plan as the source of truth for the talk goals, audience, arc, and constraints.
	- Show how the human edits intent while the agent turns that intent into structure.
	- Visual: cropped screenshot of the markdown plan beside the agent/chat making edits to it, with only one or two key lines highlighted.

3. Generate the first deck quickly (1:15-2:00)
	- Compare LLM-friendly formats like Reveal.js with harder-to-edit formats like PowerPoint.
	- Emphasize speed to first draft: not perfect slides, but a real artifact to react to.
	- Visual: best option is a 10-15 second embedded screen recording of the agent generating a Reveal.js deck from the plan, ending on the first rendered deck. Backup option is a before/after screenshot pair with the markdown plan on the left and generated slides on the right.

4. Use Agent Skills to make the workflow repeatable (2:00-2:30)
	- Explain Agent Skills as reusable instructions plus workflow knowledge for the agent.
	- Show how skills package the process, standards, and checks that improve both speed and output quality.
	- Visual: three-part card diagram: capture the recipe, encode your standards, raise the floor.

5. Style and polish with options (2:30-3:10)
	- Prompt for a theme, brand fit, or multiple visual directions.
	- Pick the visual direction early so future content changes happen inside the real presentation experience.
	- Visual: screenshot grid of 3 visual theme options, with the chosen direction clearly marked. Prioritize visible slide thumbnails over prompt text.

6. Iterate with accuracy checks (3:10-4:00)
	- Ask the agent to audit claims against docs, source code, and examples.
	- Treat the agent as a reviewer that can keep checking as the styled deck evolves.
	- Visual: screenshot with callouts showing one claim being reviewed against docs or code, labeled “claim,” “source,” and “suggested fix.”

7. Reuse the finished talk after delivery (4:00-4:45)
	- Generate annotated slides, summaries, blog-style writeups, and social snippets.
	- Show the value of preserving the workflow artifacts, not just the final deck.
	- Visual: fan-out diagram from the final deck to annotated slides, summary, blog post, and social snippets, with small artifact thumbnails if available.

8. Closing takeaway (4:45-5:00)
	- AI does not replace the presenter; it compresses the repetitive parts around the presenter's judgment.
	- End with the repeatable pattern: plan, generate, style, audit, share.
	- Visual: polished version of the workflow diagram from the opening, updated to the final repeatable pattern: plan, generate, style, audit, share.

Overall guidance:

- Use screenshots for evidence, diagrams for process, and embedded video only for the one moment where motion adds real value: generating the first deck.
- Keep every screenshot aggressively cropped and highlighted; unreadable full-screen IDE shots will lose the room.
- For a lightning talk, aim for one strong visual idea per slide instead of mixing screenshots, code, and diagrams on the same slide.

TODO:
* Slide about Tip: Add to AGENTS.md?

AGENTS.md
https://github.com/pamelafox/azure-cosmosdb-identity-aware-mcp-server/blob/main/AGENTS.md#slide-design

Make a tutorial version! Minimize token cost though

