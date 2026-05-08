# NoveaCockpit Sample GUI

This is a static fake-data preview of the NoveaCockpit product shape. It is a
public teaching/demo surface, not the private desktop app.

Clone or download the public repository, then open `index.html` directly:

```powershell
git clone https://github.com/David-A18/NoveaCockpit.git
cd NoveaCockpit
start sample-gui\index.html
```

You can also serve this folder locally:

```powershell
cd sample-gui
python -m http.server 4174
```

Then open `http://127.0.0.1:4174`.

The sample includes a Getting Started screen, fake Workbench interactions,
Runtime status, Interactions, Dashboard, Models, and Knowledge views.

Read [GUIDE.md](GUIDE.md) for the full install and walkthrough guide.

It does not connect to local APIs, import transcripts, call models, expose
prompts, read local files, or include private app code.

Use `images/` only for screenshots that have been reviewed and approved for public sharing.
