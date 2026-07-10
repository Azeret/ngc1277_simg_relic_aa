# Project Overview: NGC1277 Relic Si/Mg Yield-Channel Tests

## 1. Project Summary

This project tests whether an NGC1277-like compact relic galaxy can reproduce the high NIR-inferred `[Si/Mg]` suggested by Eftekhari-style analysis while preserving the already successful relic-galaxy fit in stellar mass, metallicity, `[Mg/Fe]`, and mass-to-light ratio. The current framework uses an environment-dependent, time-variable galaxy-wide IMF model, with IGIMF/GalIMF as the computational machinery/tool. The clean relic model does not naturally reach high `[Si/Mg]`; copied-code PopIII/PISN-like Si-rich yield-channel experiments show that a short early enrichment episode can raise `[Si/Mg]` into the lower high-Si regime, but not to the nominal `[Si/Mg]~0.67` value without degrading the relic fit.

## 2. Scientific Motivation

NGC1277 is a compact relic candidate whose old, rapid formation history should make it a sensitive test of early enrichment physics. The baseline relic model already captures the core relic observables, especially high `[Mg/Fe]`, which reflects rapid star formation and limited late-time dilution. The tension is silicon: Eftekhari-style NIR analysis implies much higher Si relative to Mg than the clean chemical-evolution model predicts. If real, that tension may point to early Si-selective yields, localized enrichment, aperture/light-weighting effects, or abundance-response systematics in the NIR indices.

## 3. Observational Target / Problem

The working comparison values are:

- lower high-Si regime: `[Si/Mg]~0.4`;
- nominal NGC1277 value: `[Si/Mg]~0.67`.

These are treated as NIR-index-inferred abundance targets, not direct outputs of the one-zone chemical-evolution model. The clean baseline has code-light `[Si/Mg]=0.058` and E-MILES NIR-local `[Si/Mg]=0.075`, so it is far below both the lower-edge and nominal comparison values.

## 4. Model Baseline

The baseline is the fixed NGC1277 relic best-fit rerun in the copied yield-channel test tree. The clean control has:

- `logM = 11.082`;
- light-weighted `[M/H]` or `[Z/X] = 0.262`;
- light-weighted `[Mg/Fe] = 0.422`;
- light-weighted `[Si/Fe] = 0.480`;
- light-weighted `[Si/Mg] = 0.058`;
- `M/L = 29.374` in internal code luminosity units.

The baseline remains the reference for relic-fit deltas. The yield-channel experiments are copied-code tests and not production-code replacements.

## 5. IMF Treatment

The science model is an environment-dependent, time-variable galaxy-wide IMF model. IGIMF/GalIMF is the machinery used to compute the galaxy-wide IMF. In this Si/Mg project, the relic baseline is not re-optimized when the yield channel is varied; most scans keep the NGC1277 best-fit parameters fixed and perturb only the yield/enrichment channel.

The E-MILES weighting and index checks use public BaSTI baseFe bimodal SSPs with IMF slopes including 1.3 and 3.0. For the clean old relic case, changing the E-MILES weighting SSP between slope 1.3 and 3.0 has negligible impact on final `[Si/Mg]`. The E-MILES index inventory shows that MgI and SiI baseline indices vary with IMF slope, metallicity, age, and velocity broadening, but the public baseFe grid does not provide independent `[Si/Fe]` or `[Mg/Fe]` response functions.

## 6. Yield Treatment

The standard baseline uses the Nomoto-family chemical-evolution setup inherited by the current relic model. The copied yield-channel tests add an opt-in PopIII/PISN-like channel in `yield_channel_tests/chemical_code_copy/`, controlled by environment variables such as `MIXED_POPIII_ENABLE`, `MIXED_POPIII_FRACTION`, `MIXED_POPIII_MASS`, `MIXED_POPIII_CUTOFF_MYR`, and `MIXED_POPIII_Z_CUTOFF`.

The mixed-channel implementation reads raw yields from `yield_tables/popIII_N13.txt` in the copied galIMF reference yield set. The current reports identify the key representative mass as `170 Msun`, but the exact yield row/table should still be verified before manuscript use.

## 7. Special PopIII/PISN-Like Si-Rich Channel

The key successful test is a timed PopIII/PISN-like Si-rich channel:

- model: `timed_s0_d40_m170_f0p35_e1p00`;
- start: `0 Myr`;
- duration: `40 Myr`;
- representative PopIII/PISN-like yield mass: `170 Msun`;
- fraction: `0.35`;
- efficiency/mixing: `1.0`;
- recorded injections: `5`.

It reaches E-MILES NIR-local `[Si/Mg]=0.499` with relic-fit deltas `d[M/H]=+0.095`, `d[Mg/Fe]=-0.070`, `dlogM=+0.137`, and `dlogM/L=+0.053`. This is accepted within the adopted relic-fit tolerance box but sits close to the boundary.

## 8. E-MILES/NIR Weighting And Index Tests

Two layers of observational comparison were tested:

- Generic weighting tests: formed mass, surviving stellar mass, stars plus remnants, and current code luminosity shift detailed-model `[Si/Mg]` by at most `0.011 dex`.
- E-MILES NIR-local flux weighting: public E-MILES BaSTI baseFe SSP fluxes in the MgI 1.18, SiI 1.20, and SiI 1.59 windows are used as local flux weights for stellar generations.

NIR-local weighting raises the clean baseline only from `[Si/Mg]=0.058` to about `0.075`. It can amplify chemically perturbed models more strongly, e.g. the mild mixed PopIII/PISN-like case reaches E-MILES NIR-local `[Si/Mg]~0.311`. This is still an abundance-weighting test, not a full spectral-index abundance inference.

The E-MILES NIR index inventory measures public baseFe SSP pseudo-equivalent widths, including the old metal-rich slope-3.0 case closest to the Eftekhari comparison: at 11.5 Gyr, `[M/H]=+0.26`, slope 3.0, and `sigma=440 km/s`, the measured values are `MgI1.18=0.4419 A`, `SiI1.20=1.3642 A`, and `SiI1.59=0.9216 A`.

## 9. Model Families Tested

- Clean relic baseline/control.
- Abundance weighting variants using available code outputs.
- E-MILES NIR-local flux weighting.
- Public E-MILES baseFe NIR index measurements.
- Pre-enriched initial gas with initial `[Si/Mg]` from 0.0 to 0.8.
- Two-component light-mixing toy models.
- Mixed PopIII/PISN-like yield-channel scans.
- Constrained timed Si-rich enrichment scans and local refinement.
- High-Si failure-mode/Pareto-style comparisons.

## 10. Accepted And Rejected Models

Accepted or final-enough for discussion:

- `clean_baseline`: preserves the relic fit but has low Si/Mg.
- `mixed_popiii170_v5_f0.1`: chemically useful mild case; code-light `[Si/Mg]=0.158`, E-MILES NIR-local `[Si/Mg]~0.311`; still below the lower-edge target.
- `timed_s0_d40_m170_f0p35_e1p00`: current best accepted boundary solution; E-MILES NIR-local `[Si/Mg]=0.499`.

Rejected or sensitivity-only:

- `timed_s0_d50_m170_f0p35_e1p00`: E-MILES NIR-local `[Si/Mg]=0.523`, rejected because total metallicity, `[Mg/Fe]`, and stellar mass degrade beyond the adopted tolerance box.
- `mixed_popiii170_v5_c100_z1_f0.3`: reaches E-MILES NIR-local `[Si/Mg]=0.574`, but fails through coupled mass, metallicity, and `[Mg/Fe]` shifts.
- Aggressive mixed-channel cases are sensitivity tests, not accepted physical models.

## 11. Final Interpretation

The current framework can reach the lower high-Si regime if a short, early, Si-rich PopIII/PISN-like channel operates. The accepted ceiling is effectively around E-MILES NIR-local `[Si/Mg]~0.5`. Reaching the nominal `[Si/Mg]~0.67` value requires either more Si-selective yields, a localized or aperture-dominant high-Si subpopulation, or caution about translating NIR SiI/MgI indices into absolute abundance ratios.

## 12. Connection To Relicness, Mg/Fe, And Si/Mg

Relicness should correlate robustly with `[Mg/Fe]` because compact relics form rapidly and avoid extended late-time star formation that would lower alpha-enhancement. Si/Mg is less automatic. It may correlate with relicness only if the early Si-rich channel was active during the compact formation episode and was not later diluted by accreted or extended star formation. Normal ETGs may dilute toward `[Si/Mg]~0` through later stellar populations, longer enrichment histories, and aperture mixtures, while relics preserve early abundance signatures more cleanly.

## 13. Remaining Caveats

- These are copied-code yield-channel experiments, not production-code replacements.
- The current `[Si/Mg]` values are chemical-evolution abundance proxies, not full spectral-index abundance inferences.
- E-MILES public baseFe spectra do not isolate independent Si and Mg response functions.
- The exact PopIII/PISN-like `170 Msun` yield row/table must be verified before publication.
- The best accepted model is a boundary solution with small remaining tolerance margins.
- The one-zone model cannot represent localized subpopulations, aperture gradients, or cluster-scale enrichment in detail.
- The nominal `[Si/Mg]~0.67` target remains unreproduced without breaking relic constraints.
