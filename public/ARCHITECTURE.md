# NoveaCockpit Public Architecture

Last updated: 2026-05-08.

## Layers

- Desktop shell for local app startup and runtime supervision
- Web UI for Workbench, Runtime, Interactions, Dashboards, Models, and Knowledge Graph workflows
- Local API for health, projects, conversations, agent runs, tool runs, providers, and reports
- Local profile database for auditable state
- Local artifact storage for generated reports and imported interaction metadata
- Optional local Ollama provider for approved local models

## Safety Model

- Local-first execution
- Explicit approval for mutating tools
- No automatic Obsidian file writeback
- No arbitrary shell execution in the current approved path
- Public mirror excludes source code and operational values
- Public sample GUI is static fake-data content only

## Ollama Integration

NoveaCockpit detects a local Ollama server when available. It does not install Ollama, pull models, or own the Ollama process by default.

The secondary bridge validates local model and tool-wrapper patterns before they are accepted into the main app.

## Public Demo Boundary

The public sample GUI is a teaching surface for the workflow shape. It does not contain the Electron shell, FastAPI API, React source, database schema, tool runtime, local transcripts, or operational configuration.
