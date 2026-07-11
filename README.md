# NGC1277 Relic Si/Mg A&A Draft

This is a clean, git-ready A&A draft directory for the NGC1277 / compact relic Si/Mg yield-channel project.

The draft describes copied-code yield-channel tests of whether an NGC1277-like compact relic model can reach high NIR-inferred `[Si/Mg]` while preserving the relic fit in stellar mass, metallicity, `[Mg/Fe]`, and `M/L`.

The current version also includes the weak/moderate normal-ETG control sequence. These figures and notes test whether ordinary massive ETG diagnostics can preserve the mass-metallicity and mass-`[Mg/Fe]` calibration while allowing only weak or moderate early PopIII/PISN-like Si-rich enrichment.

## Layout

- `manuscript/main.tex`: A&A manuscript root.
- `manuscript/sections/`: split manuscript sections.
- `manuscript/tables/`: LaTeX tables generated from lightweight analysis products.
- `manuscript/figures/`: selected lightweight existing figures.
- `notes/`: copied markdown/CSV planning and provenance notes from the analysis directory.

## Compile Locally

From `manuscript/`:

```bash
latexmk -pdf main.tex
```

or:

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

The A&A class and bibliography style were copied locally:

- `manuscript/aa.cls`
- `manuscript/aa.bst`
- `manuscript/linenoaa.sty`
- `manuscript/lineno.sty`

## Import Into Overleaf

Upload the contents of this directory, or zip the directory and import it as a new Overleaf project. Set `manuscript/main.tex` as the main file if Overleaf does not detect it automatically.

## Generated From Analysis Outputs

The current draft uses lightweight products from:

`/home/tereza/early_type_galaxies/results/yield_channel_tests/analysis/`

Key generated/copied items:

- `notes/project_overview.md`
- `notes/result_inventory.csv`
- `notes/figure_table_plan.md`
- `notes/next_actions.md`
- `manuscript/tables/key_models.tex`
- `manuscript/tables/weakmod_etg_control_sequence.tex`
- `manuscript/figures/final_relic_simg_key_models.png`
- `manuscript/figures/weakmod_etg_simg_sequence.pdf`
- `manuscript/figures/weakmod_etg_simg_vs_mgfe.pdf`
- `manuscript/figures/weakmod_mass_metallicity_mgfe_validation.pdf`
- `manuscript/figures/weakmod_allowed_channel_strength_by_mass.pdf`

See `notes/source_manifest.md` for provenance.

## Before Sharing With Collaborators

- Replace placeholder authors, affiliations, and acknowledgements.
- Verify the exact PopIII/PISN-like `170 Msun` yield table/row.
- Verify every number in `final_relic_simg_key_models.csv`.
- Verify the weak/moderate ETG control-sequence classifications against `paper_ready_weakmod_etg_simg_sequence_table.csv`.
- Replace placeholder BibTeX entries with exact references.
- Decide whether to keep the existing key-model PNG or remake all figures in a publication style.
- Keep the language cautious: these are copied-code yield-channel tests, not production-code replacements.
