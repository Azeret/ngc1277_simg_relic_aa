# Paper-ready weak/moderate ETG Si/Mg sequence

## Source

This note is post-processing only. It uses the completed copied-code weak/moderate fixed diagnostic campaign:

- `/home/tereza/early_type_galaxies/results/yield_channel_tests/analysis/full_etg_mass_sequence_weakmod_sirich_results.csv`
- `/home/tereza/early_type_galaxies/results/yield_channel_tests/analysis/full_etg_mass_sequence_mass_metallicity_mgfe_validation.csv`
- `/home/tereza/early_type_galaxies/results/yield_channel_tests/analysis/full_etg_mass_sequence_weakmod_sirich_allowed_region.csv`

No chemical-evolution models were run for this figure preparation step.

## Key [Si/Mg] sequence

| Mass | clean | d20_f0p10 | d40_f0p10 | d20_f0p20 | d40_f0p20 |
| --- | ---: | ---: | ---: | ---: | ---: |
| M1e9 | 0.192 | 0.246 | 0.277 | 0.293 | 0.347 |
| M1e10 | 0.147 | 0.178 | 0.197 | 0.207 | 0.242 |
| M1e11 | 0.093 | 0.113 | 0.126 | 0.132 | 0.155 |
| M1e12 | 0.074 | 0.129 | 0.160 | 0.175 | 0.229 |

## Paper-facing classification

The paper-facing classification uses the multi-constraint calibration from the campaign: stellar mass, metallicity, [Mg/Fe], and whether [Si/Mg] is in or can be diluted into the normal ETG locus with an old alpha-enhanced envelope. M1e9 is labelled `low_mass_upper_limit` because its clean [Si/Mg] is already near the upper normal range and its [Mg/Fe] is low compared with the massive ETG calibration regime.

## Figure Guide

- `paper_ready_weakmod_etg_simg_sequence_plot.png/.pdf`: [Si/Mg] versus target mass with normal ETG allowed and preferred bands.
- `paper_ready_weakmod_etg_simg_vs_mgfe_plot.png/.pdf`: [Si/Mg] versus [Mg/Fe], separating rapid-formation calibration from Si-rich preservation strength.
- `paper_ready_mass_metallicity_mgfe_validation_plot.png/.pdf`: mass-metallicity, mass-[Mg/Fe], and normalized residual checks.
- `paper_ready_allowed_channel_strength_by_mass.png/.pdf`: classification grid for allowed channel strength by mass.

## Interpretation

The conservative normal-ETG channel is `d20_f0p10`. For M1e10, M1e11, and M1e12 it modifies [Si/Mg] while preserving the stored mass, metallicity, and [Mg/Fe] calibration within the adopted tolerance box. M1e11 and M1e12 also tolerate several moderate channels. The `d40_f0p20` channel is best treated as an upper-normal or boundary case, while `d40_f0p35` remains reserved for the NGC1277/relic-strength comparison.

The sequence supports a differential-preservation picture. Normal ETGs may preserve a weak effective PopIII/PISN-like Si-rich enrichment channel while remaining on the calibrated ETG relations. NGC1277-like compact relics require stronger preservation of the same early Si-rich phase.
