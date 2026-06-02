## Before submitting to JOSS

1. **Move** `paper.md`, `paper.bib`, and `figures/` into the **public software repository** (same repo as the application source), as required by [JOSS submission guidelines](https://joss.readthedocs.io/en/latest/submitting.html).
2. **Update** `paper.bib` entry `logsheetxtractor_repo` with the canonical GitHub URL and, after acceptance, the Zenodo/figshare archive DOI.
3. **Add** an OSI-approved `LICENSE` file in the software repo if not already present.
4. **Compile** the paper locally or with the [Open Journals GitHub Action](https://joss.readthedocs.io/en/latest/paper.html#github-action) to verify figures and citations.
5. **Review** authorship, ORCID, and affiliations in the YAML header of `paper.md`.
6. **Confirm** the AI usage disclosure in `paper.md` matches your actual workflow.

## Compile locally (PDF)

```bash
docker run --rm --platform linux/amd64 \
  -v "$PWD":/data \
  -w /data \
  -e JOURNAL=joss \
  openjournals/paperdraft \
  paper.md
```
