User documentation for [hpc-setup](https://github.com/nucbio/hpc-setup), built with [Quarto](https://quarto.org).

`packages.qmd` is generated from `hpc-setup/pkgs.json` by `scripts/packages.py` before each render.

The site is rendered locally into `docs/` and served by GitHub Pages from `main` / `docs`
(https://nucbio.github.io/hpc-setup-docs/).

## Publish

With hpc-setup checked out next to this repo, run from hpc-setup:

```bash
deploy/git_upload.sh "commit message"
```

This commits and pushes hpc-setup, renders this site, then commits and pushes this repo.

## Preview locally

```bash
quarto preview      # or set HPC_SETUP_DIR if hpc-setup lives elsewhere
```
