# 🌟Wikikit - scaffold v0 of your documentation without suffering 🌟

Often when using LLMs, you get a bunch of great ideas but you're left with crap when you try and ask them to summarize or generate design docs. I just exhaust daily free limits instead of paying for subscriptions, so I often need to do context transfer between models. This repo is designed with the goal of **knowledge management in the age of LLM co-founders.**

-----

## 🧐 What's Inside?

This repository packs two key components to streamline your app development process:

1.  **💡 YAML Superprompts (`/prompts` folder):**
    These are highly structured YAML definitions, crafted to be injected directly into LLM chats. Their purpose is to help you **extract and organize context** from your brainstorming sessions into specific, well-formatted project documents. Think of them as precise instructions that guide the LLM to output exactly what you need.

2.  **📚 Sample Wiki (`/wikikit.wiki` submodule or local copy):**
    This is a comprehensive, pre-structured GitHub Wiki that serves as a **skeleton or scaffold** for your actual project documentation. It's filled with placeholder content, representing the ideal end-state after you've run through all the prompts and saved the generated documents. At the very least, it'll save you the effort of linking together yet another wiki from scratch.

-----

## 🚀 How to Use This Repo

The workflow is straightforward:

1.  **Brainstorm with Your Favorite LLM:**
    Generate ideas and develop concepts with your preferred LLM. I personally recommend **Gemini** for large context summaries and **Claude** for nailing down the details. **Grok** is great for large output windows, and **ChatGPT** is always a solid choice, I particularly enjoy its Markdown formatting style.

2.  **Generate Document Drafts:**

      * **Select a Superprompt:** Choose the YAML file from the `prompts/` directory that corresponds to the document section you want to generate (e.g., `prompts/generate_project_vision.yaml`).
      * **Provide User Input:** Fill in the `user_input` section at the bottom of the chosen YAML file with specific details about your app idea.
      * **Run the Prompt:** Copy the entire YAML content and paste it into your LLM's chat interface. The LLM will then produce a structured draft in Markdown.

3.  **Populate Your Wiki:**
    Copy the generated Markdown content from the LLM and paste it into the relevant page in your project's wiki. Review, refine, and add any specific details or diagrams.

-----

## 🛠️ Getting Started with the Wiki Scaffold

First, let's get your project wiki set up:

1.  **Clone this repository:**

    ```bash
    git clone https://github.com/asavschaeffer/wikikit.git
    cd wikikit
    ```

2.  **Access the Sample Wiki:**

      * **Via GitHub:** If you've forked this repository to your own GitHub account, simply navigate to the **"Wiki" tab** on your repository page. The pre-structured content will be there.
      * **Locally:** The wiki content is also available as a separate Git repository. You can clone it directly:
    
        ```bash
        git clone https://github.com/asavschaeffer/wikikit.wiki.git
        ```

3.  **Adapt for Your Project:**
    Explore the organized structure and example content within the wiki. This sample wiki is designed as a template; you should **copy its structure** for your own project's documentation. You can then easily replace the placeholder content with your app's specific information, section by section.

-----

## 🤝 Contribution & Support

This blueprint is open-source and continuously evolving. Your contributions and feedback are welcome to help improve this resource. If you want to improve a prompt I would be very grateful!

  * **[Report an Issue](https://www.google.com/search?q=https://github.com/asavschaeffer/wikikit/issues)**
  * **[Suggest an Improvement](https://www.google.com/search?q=https://github.com/asavschaeffer/wikikit/pulls)**

-----

**License:** [MIT License](https://www.google.com/search?q=LICENSE)
