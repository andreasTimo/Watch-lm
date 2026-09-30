# NotebookLM project mapping

Each project owns exactly one NotebookLM notebook. Store the mapping in the project root at `.watch-lm/notebook.json`:

```json
{
  "project": "Example Project",
  "notebook_id": "<NotebookLM UUID>",
  "notebook_url": "https://notebooklm.google.com/notebook/<NotebookLM UUID>",
  "schema_version": 1
}
```

NotebookLM YouTube sources are transcript-based. Keep visual evidence and OCR from Watch Skill in `evidence.md` and add that report as a source.

Create this file with `python3 scripts/init_watch_lm_project.py --project-root /path/to/project --project "Example" --notebook-id <existing-notebook-uuid>`. The initializer refuses to replace a different mapping and adds `notebook.json` and `runs/` to the local `.watch-lm/.gitignore`. Never publish a real notebook UUID as part of a template.
