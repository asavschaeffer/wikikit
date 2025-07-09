### **The Documentation Workflow: A Repeatable Process**

This workflow formalizes our two-tiered documentation system: **Core Actionable Documents** and **Working Contextual Documents**.

**The `docs/` Repository Structure**

```
globule/
└── docs/
    ├── 01_Vision_and_Strategy.md
    ├── 02_Product_Requirements_Document_(PRD).md
    ├── 03_Technical_Design_and_Architecture.md
    ├── 04_Project_Roadmap.md
    │
    └── working/
        ├── 2025-07-09_Initial-Vision-Session.md
        ├── 2025-07-10_UX-Critique-Hard-Questions.md
        └── YYYY-MM-DD_Topic-of-Discussion.md
```

  * **`docs/`**: This root folder contains the **Core Documents**. These are the single source of truth for what we are building and why. They should be kept clean, concise, and up-to-date with the latest *decisions*.
  * **`docs/working/`**: This directory is the project's institutional memory. It contains the **Working Documents**—the messy, detailed, and invaluable records of our brainstorming sessions, debates, and explorations.

-----

### The 5-Step Workflow: From Idea to Documented Decision

This is the lifecycle for any significant new feature, architectural change, or strategic pivot.

#### **Step 1: The Brainstorming Session (The "Messy" Part)**

This is where all new ideas begin. It's our conversation, a whiteboard session, or a deep-dive critique.

  * **Goal**: To explore a problem or idea from all angles without restriction.
  * **Output**: A raw, unfiltered record. This could be a chat log, meeting notes, or a rough personal document.
  * **Example**: Our discussion about the "hard questions" and your detailed walkthrough of the creative writing use case.

#### **Step 2: Create the "Working Document"**

Immediately after the session, the raw output is captured and saved as a new **Working Document**.

  * **Action**: Create a new Markdown file in the `docs/working/` directory.
  * **Naming Convention**: Use the format `YYYY-MM-DD_Topic-of-Session.md` for chronological organization and easy discovery.
      * *Example*: `2025-07-10_Refining-the-Drafting-Table-UX.md`.
  * **Content**: Paste the entire raw conversation or notes into this file. Do not edit or heavily format it. The goal is to preserve the context in its original form.

#### **Step 3: Distill the Decisions**

This is the most critical thinking step. Review the new Working Document and identify the key **decisions** that were made.

  * **Goal**: To extract clear, actionable outcomes from the brainstorming noise.
  * **Action**: Write a concise summary at the very top of the Working Document. This summary should be a bulleted list under a heading like "Key Decisions".
  * **Example**:
      * **Decision**: The MVP will focus exclusively on the creative writing use case.
      * **Decision**: The "report" command will be renamed to `globule draft`.
      * **Decision**: The drafting UI will be a two-pane system (Palette and Canvas).
      * **Decision**: The Palette will default to a clustered/categorized view, not chronological.

#### **Step 4: Update the "Core Documents"**

With the decisions clearly summarized, update the relevant Core Documents. You are not re-writing them from scratch; you are making surgical updates to reflect the new decisions.

  * **Goal**: To keep the project's official plan current.
  * **Action**:
    1.  Go to `02_Product_Requirements_Document_(PRD).md` and update the feature list to include the two-pane editor and the default clustered view.
    2.  Go to `03_Technical_Design_and_Architecture.md` and add a section on the TUI architecture.
    3.  Go to `04_Project_Roadmap.md` and ensure the "Ollie" stage explicitly mentions these features.

#### **Step 5: Link for Context (The "Magic" Step)**

This final step connects the **"what"** in the Core Documents to the **"why"** in the Working Documents.

  * **Goal**: To ensure that the rich context behind every decision is never lost.

  * **Action**: At the end of each section you updated in a Core Document, add a citation-style link back to the Working Document.

  * **Example**: In the `02_Product_Requirements_Document_(PRD).md`, under the new section describing the Palette's default view, you would add:

    > *"To prevent overwhelming the user, the Palette will default to a view that clusters notes by category or semantic theme." [For the full discussion on this UX decision, see docs/working/2025-07-10\_Refining-the-Drafting-Table-UX.md]*

This workflow ensures that anyone joining the project can read the four Core Documents for a clear overview, and then follow the links to go as deep as they want into the history and reasoning behind any decision. It's a system that provides both clarity for today and wisdom for tomorrow.
