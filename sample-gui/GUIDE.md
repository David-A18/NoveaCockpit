# NoveaCockpit Sample GUI Guide

## What This Is

The sample GUI is a static, fake-data preview of the NoveaCockpit product shape.
It is meant for public exploration, screenshots, and onboarding conversations.

It is not the private desktop app. It does not connect to APIs, read local files,
call Ollama, import transcripts, run agents, expose prompts, or include private
runtime code.

## Install Or Open

Download the public repository as a ZIP, or clone it:

```powershell
git clone https://github.com/David-A18/NoveaCockpit.git
cd NoveaCockpit
```

Then open the static HTML file:

```powershell
start sample-gui\index.html
```

You can also serve the folder locally:

```powershell
cd sample-gui
python -m http.server 4174
```

Then open:

```text
http://127.0.0.1:4174
```

No build step, package install, backend server, API key, or Ollama setup is
required for the public sample.

## Suggested Demo Script

1. Open **Getting Started** and read the public/private boundary notice.
2. Open **Workbench**, click **Preview plan**, then click **Approve draft step**.
3. Open **Runtime** to see the desktop supervisor concept.
4. Open **Interactions** to see how imported assistant sessions are represented.
5. Open **Models** to review the local model policy sample.
6. Open **Knowledge** to see the vault graph and database-only draft concept.

Every action is browser-local and fake. Nothing is persisted outside the current
page session.

## Screen Tour

### Getting Started

Explains how to open the sample and what each screen is intended to teach.

### Workbench

Shows the intended user flow for planning an agent run, reviewing a safe plan,
and approving a database-only draft step.

### Runtime

Shows the desktop runtime concept: local API health, tray behavior, Ollama
readiness, and bounded restart visibility.

### Interactions

Shows how imported assistant sessions can become reviewable conversations and
reports.

### Dashboard

Shows fake operational metrics for local agent activity.

### Models

Shows the local-first model policy: approved local models, the 20B validation
boundary, and blocked oversized/cloud paths for local demos.

### Knowledge

Shows the local vault graph concept and the rule that drafts stay database-only
until a user applies them.

## Privacy And Safety

The sample GUI must stay safe for public distribution:

- Use fake data only.
- Do not include private paths, logs, transcripts, prompts, reports, artifacts,
  database URLs, keys, tokens, or customer data.
- Do not import private `apps/`, `packages/`, `db/`, `tests/`, `scripts/`, or
  runtime files.
- Do not add API calls or model calls to the public sample.
- Put only reviewed public screenshots in `sample-gui/images/`.

## Troubleshooting

- If double-clicking the file does not work, use the local server command above.
- If styles look stale, refresh the browser with cache bypass.
- If a browser blocks local files, use `python -m http.server 4174`.
- If a link points outside this public mirror, check the publication policy
  before adding it.

## Related Public Docs

- [Public overview](../public/README.md)
- [Roadmap](../public/ROADMAP.md)
- [Ollama bridge boundary](../public/OLLAMA-BRIDGE.md)
- [Publication policy](../docs/publication-policy.md)
