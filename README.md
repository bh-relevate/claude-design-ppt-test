# Claude Design × Relevate Health PPT Template

This repository documents an exploration of using **Claude Design** to generate PowerPoint presentations that follow the **Relevate Health PPT template** (`ppt template/RH_PPT_Template_V1B_test.pptx`).

## What we tried

Two different prompting approaches were used to produce comparable deck outputs:

| Folder | Approach | Input |
|--------|----------|--------|
| `rh-ppt/` | Simple prompt | `rh-ppt/input/rh-ppt-prompt.rtf` |
| `rene-ppt-prompt/` | Structured content brief | `rene-ppt-prompt/input/sales_prompt_v2.md` (markdown prescribing content hierarchy) |

Both runs targeted the same template and brand system; the difference is how much structure was given up front versus a single open-ended prompt.

## Workflow

Claude Design generated an **HTML version** of each presentation first. From that HTML preview, decks can be **exported as editable `.pptx` files**. Related artifacts for each attempt live under that folder’s `output/` directory (HTML, assets, PDF exports, and PPT files where generated).

## Viewing the decks

Open [`index.html`](index.html) in a browser for a landing page with links to each HTML deck. For reliable asset loading, serve the repo locally:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080/`.

## Repository layout

```
ppt template/          Relevate Health PPT template (.pptx)
rh-ppt/
  input/               Simple-prompt source
  output/              HTML deck, assets, exported PPT/PDF
rene-ppt-prompt/
  input/               Markdown content-hierarchy brief
  output/              HTML deck, assets, exported PPT/PDF
index.html             Links to both HTML deck outputs
```
