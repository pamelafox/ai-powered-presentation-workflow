# Exercise 1: Set up your environment

In this exercise, you'll set up a development environment and coding agent.

- [Step 1: Set up VS Code](#step-1-set-up-vs-code)
- [Step 2: Set up GitHub Copilot](#step-2-set-up-github-copilot)
- [Step 3: Install the presentation skills](#step-3-install-the-presentation-skills)

---

## Step 1: Set up VS Code

**Prerequisites:**

- [VS Code](https://code.visualstudio.com/) installed

**Steps:**

1. Clone the repository:

   ```bash
   git clone https://github.com/pamelafox/ai-powered-presentation-workflow
   ```

2. Open the folder in VS Code:

   ```bash
   code ai-powered-presentation-workflow
   ```

3. Once the editor loads, you're ready to move on to [Step 2](#step-2-set-up-a-coding-agent).

## Step 2: Set up GitHub Copilot

1. Check the right side of VS Code to see if the Copilot Chat side panel is already open. If it's not open, find the "Toggle Chat" icon at the top of VS Code, locate and click it to open the side panel.

   ![Screenshot of "Toggle chat" icon in top right](docs/screenshot_copilot_togglechat.png)

   > 🪧 **Note:** If this is your first time using GitHub Copilot, you will need to accept the usage terms to continue.

2. Make sure the chat is in **Agent** mode. (You may not see "Agent", but you should see a loop icon which says "Agent" upon clicking.)

   ![Screenshot of chat box with "Agent" mode selected](docs/screenshot_copilot_agent.png)

3. Send a test message "Hello" to confirm the agent is working.

## Step 3: Install the presentation skills

The [pamelafox/presentation-skills](https://github.com/pamelafox/presentation-skills) repository contains reusable agent skills for presentation workflows, including skills for creating RevealJS decks, reviewing presentation content, extracting slide text, fetching transcripts, and generating write-ups.

Open a terminal and run:

```bash
npx skills add pamelafox/presentation-skills
```

That installs the full presentation skill collection.

Ask your agent:

```text
What presentation-related agent skills are available to you? Do you see a skill for making RevealJS presentations and a skill for generating write-ups?
```

Once the agent confirms the skills are available, you're ready for [Exercise 2](exercise2.md).