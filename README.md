<!-- omit in toc -->

# slidev-template

A practical Slidev template for building many presentation repositories quickly, with:

- `theme: apple-basic`
- useful example slides
- addons (Asciinema, Poll/Quiz)
- GitHub Pages deployment workflow
- assistant-friendly workflow instructions

Forked from: [espressif/slidev-esp-template](https://github.com/espressif/slidev-esp-template).

## Quick Start (2 minutes)

1. Create a new repo from this template (GitHub: **Use this template**).
2. Clone your new repo.
3. Install dependencies:

```sh
npm install
```

4. Run slides locally:

```sh
slidev
```

5. Open: <http://localhost:3030>

## Recommended Authoring Workflow

### Template files

- `slides.example.md` → immutable baseline example/template
- `slides.md` → optional default entrypoint

### For each new deck

1. Keep `slides.example.md` unchanged.
2. Create a new working deck, e.g.:
   - `slides-ai-intro.md`
   - `slides-2026-03-02.md`
3. Build your presentation in that new file.
4. Only overwrite `slides.md` if explicitly needed.

This keeps template integrity while allowing many deck variants.

## Use with AI Assistants (Claude, Cline, Codex…)

Use:

> Follow instructions in `docs/SLIDEV-INPUT-WORKFLOW.md`.

That file defines a consistent, assistant-agnostic process for converting PPT/Keynote/PDF/notes into Slidev decks.

### Where to put source input files

Copy raw source materials into `input/<deck-id>/`, for example:

```text
input/2026-03-ai-course/
  source.pptx
  notes.md
  images/
```

See also `input/README.md`.

### Missing images (default policy)

If images are missing, prefer sourcing **modern, minimal, abstract** visuals from [Unsplash](https://unsplash.com/).

- Save them to: `public/<deck-id>/images/`
- Add credits (author + source URL + license) to: `input/<deck-id>/sources.md`

## Project Structure

- `slides.example.md` — baseline template deck
- `slides.md` — optional active/default deck
- `docs/SLIDEV-INPUT-WORKFLOW.md` — AI workflow contract
- `input/` — raw source files to ingest (PPT/PDF/notes/images)
- `pages/` — reusable/imported slide sections
- `public/` — static assets (images, logos, casts)
- `components/` — Vue components for slides
- `snippets/` — external code snippets for embedding

## Addons Included

- [@olzhas-adiyatov/slidev-addon-asciinema](https://www.npmjs.com/package/@olzhas-adiyatov/slidev-addon-asciinema)
- [slidev-addon-sync](https://github.com/Smile-SA/slidev-addon-sync)
- [slidev-component-poll](https://github.com/Smile-SA/slidev-component-poll)

Examples are already available in slide files.

## Deploy to GitHub Pages

This repo includes `.github/workflows/deploy.yml`.

### Required repo setting

In GitHub:

- **Settings → Pages → Build and deployment → Source = GitHub Actions**

### Deployment trigger

- Push to `main` (or manual workflow dispatch).

The workflow builds Slidev with a project-repo base path (`/${repo-name}/`) and deploys `dist` to Pages.

## Useful Commands

```sh
# dev
slidev

# build
npm run build

# export (if configured)
npm run export
```

## Learn More

- Slidev docs: <https://sli.dev>
- Syntax guide: <https://sli.dev/guide/syntax>
- Directory structure: <https://sli.dev/custom/directory-structure>
- Apple Basic theme docs (raw): <https://raw.githubusercontent.com/slidevjs/themes/refs/heads/main/packages/theme-apple-basic/README.md>
- Apple Basic theme example (raw): <https://raw.githubusercontent.com/slidevjs/themes/refs/heads/main/packages/theme-apple-basic/example.md>
