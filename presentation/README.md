# TPIF Presentation

## Tiered Privacy: Restoring Trust in the Digital Age

This presentation provides an overview of the Tiered Privacy and Identity Framework (TPIF), a decentralized approach to online identity verification that balances privacy and authenticity.

## Contents

- `Slides.md` - The main presentation file in Marp format
- `TPIF-architecture.md` - Detailed architecture diagram (in Mermaid format)

## How to Use

This presentation is created using [Marp](https://marp.app/), a Markdown presentation ecosystem. To view and present these slides:

### Option 1: Using Marp CLI

1. Install [Marp CLI](https://github.com/marp-team/marp-cli):
   ```
   npm install -g @marp-team/marp-cli
   ```

2. Generate a PDF:
   ```
   marp --pdf Slides.md
   ```

3. Or start a presentation server:
   ```
   marp -s Slides.md
   ```

### Option 2: Using Visual Studio Code

1. Install the [Marp for VS Code extension](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)
2. Open the `Slides.md` file
3. Use the "Marp: Export slide deck..." command to export to PDF, PPTX, or HTML
4. Or use the preview window to present directly

## Presentation Duration

This presentation is designed to be delivered in approximately 15 minutes.

## References

The content is based on the detailed white paper "Tiered Privacy: Restoring Trust in the Digital Age" located in the documents directory.

## Architecture Diagram

The system architecture diagram uses Mermaid syntax. If you want to render it separately:

1. Use the [Mermaid Live Editor](https://mermaid.live/)
2. Or install a Mermaid rendering tool like:
   ```
   npm install -g @mermaid-js/mermaid-cli
   mmdc -i TPIF-architecture.md -o TPIF-architecture.png
   ``` 