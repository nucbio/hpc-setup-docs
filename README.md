User documentation for [hpc-setup](https://github.com/nucbio/hpc-setup), built with [Quarto](https://quarto.org).

`packages.qmd` is generated from `hpc-setup/pkgs.json` by `scripts/packages.py` before each render.

The site is rendered locally into `docs/` and served by GitHub Pages from `main` / `docs`
(https://nucbio.github.io/hpc-setup-docs/).

## Publish

With hpc-setup checked out next to this repo, run from hpc-setup:

```bash
deploy/git_upload.sh "commit message"
```

This bumps the patch number in `VERSION`, commits and pushes hpc-setup, renders this site,
then commits and pushes this repo.

For a release, `-m` bumps minor (1.0.14 -> 1.1.0) and `-M` bumps major (-> 2.0.0);
both also create and push a release tag with the current date `YY.MM` (e.g. `26.11`).
The same name is used for the GitHub release and the release directory on servers
(`tools/26.11`). One release per month: an existing tag aborts the run.

```bash
deploy/git_upload.sh -m "release 26.11"
```

## Preview locally

```bash
quarto preview      # or set HPC_SETUP_DIR if hpc-setup lives elsewhere
```
