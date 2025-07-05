name: generate_high_level_design_doc
version: 1.1
description: High-level design and system architecture document for software projects.
output_type: markdown
output_file: high_level_design.md
instructions: |
  Read the full conversation history and output a clean, structured high-level design document.
  Do not include any introductory or explanatory text.
  Only output the document below, formatted as markdown.
output_format: |
  # High-Level Design Document: {{app_name}}
  ## App Summary
  A concise summary of what the app is and what it solves.
  ## Design Goals
  - State 2–5 architectural or product design goals that guided decisions.
  - These may be about speed, reliability, modularity, cost, etc.
  ## System Overview
  Describe the major components and how they interact.
  Include user interaction, external APIs, frontend/backend relationships, and where state lives.
  ## Tech Stack
  | Layer        | Stack Choices + Notes         |
  |--------------|-------------------------------|
  | Frontend     |                               |
  | Backend      |                               |
  | Database     |                               |
  | Auth         |                               |
  | Hosting/Infra|                               |
  ## Component Breakdown
  ### Frontend
  - What screens or components exist?
  - Any frameworks or client-side logic worth noting?
  ### Backend
  - Major services, APIs, endpoints
  - What logic or responsibilities are held server-side?
  ### External APIs & Services
  - What third-party integrations are required?
  ### Storage / State
  - Where and how is data stored or cached?
  ## Data Flow
  Describe how data flows through the system from input to output.
  Can include user actions, server responses, model outputs, etc.
  ## Diagram: System Context
  Use Mermaid syntax. Show the relationship between user, frontend, backend, and any external systems.
  
  Example (modify to fit your project):
  ```mermaid
  graph TD
    User -->|clicks| Frontend
    Frontend -->|API call| Backend
    Backend -->|query| Database
    Backend -->|calls| ExternalAPI
    ExternalAPI --> Backend
    Backend --> Frontend
    Frontend --> User
