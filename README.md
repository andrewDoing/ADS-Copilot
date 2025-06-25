# 🏗️ ADS Copilot

Welcome to **ADS Copilot**! This project is designed to help automate and streamline Architecture Design Sessions by generating structured documents and integrating with Azure DevOps.

---

## 📁 Repo Structure

- `docs/prd.md` – Product Requirements Document (PRD) with project goals and user stories.
- `.vscode/mcp.json` – VS Code config for connecting to Azure DevOps MCP using your org name.
- `.github/chatmodes/` – Contains chat modes for generating PRDs, architectures, and backlog documents.
- `generated/` – Folder for generated outputs (e.g., summaries, docs).
- `context/` – (Reserved for context files or data).

---

## 🚀 Key Features

- Generate PRDs and architecture docs from your ideas or meeting transcripts.
- Summarize meeting transcripts into clear, actionable documents.
- Integrate with Azure DevOps MCP for backlog and artifact management.

---

## ⚙️ Quick Start

1. Clone this repo.
2. Open in VS Code.
3. Use the `.vscode/mcp.json` config to connect to your Azure DevOps org:
   - You’ll be prompted for your org name (e.g., `contoso`).
4. Run `az login` and select the appropriate subscription.
5. Start generating and managing your architecture session docs!

---

## 📄 References

- See [`docs/prd.md`](docs/prd.md) for full requirements and design.
- See [`.vscode/mcp.json`](.vscode/mcp.json) for DevOps integration setup.

---

## 📝 License

See [LICENSE](LICENSE) for details.

---

✨ Happy architecting!