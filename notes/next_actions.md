# Si/Mg Project Next Actions

## Must Do Before Manuscript Draft

- Verify the exact yield file, table, and row used for the `170 Msun` PopIII/PISN-like Si-rich channel.
- Verify every number in `final_relic_simg_key_models.csv` against the source scan CSVs.
- Confirm and label whether each reported `[Si/Mg]` value is code-light, E-MILES NIR-local, or an Eftekhari-style index-inferred target.
- Clearly separate copied-code yield-channel tests from the production baseline model.
- Make a manuscript-ready key model comparison figure from `final_relic_simg_key_models.csv`.
- Make a Pareto/failure-mode figure from `constrained_simg_local_refinement_v1.csv` and `high_simg_failure_modes_v1.csv`.
- State the adopted relic-fit tolerance box explicitly wherever the best accepted model is discussed.
- Add the caveat that the reported model abundances are chemical-evolution abundance proxies, not full spectral-index abundance inferences.
- Prepare a short response to Alex: Mg/Fe should correlate robustly with relicness; Si/Mg may correlate with relicness only if early Si-rich enrichment occurred and was not diluted by later accreted or extended populations.

## Useful But Optional

- Build a small table comparing E-MILES slope 1.3 versus 3.0 weighting for the clean baseline.
- Add a visual timing-window boundary plot showing the 40 Myr accepted and 50 Myr rejected models.
- Cross-check whether any current-best Paper I cluster/epoch outputs can support a physical origin for the early Si-rich channel.
- Add a collaborator-facing one-page model card with the best accepted model and first rejected counterpart.
- Check whether published PISN yield grids offer a more Si-selective channel than the current copied-table implementation.

## Do Not Do Now

- Do not run new models.
- Do not rerun optimizations.
- Do not modify production code.
- Do not modify production outputs.
- Do not replace the current baseline or yield-channel outputs.
- Do not claim a full match to nominal `[Si/Mg]~0.67`.
- Do not present E-MILES baseFe index measurements as independent `[Si/Fe]` or `[Mg/Fe]` response modeling.

## Checks Before Talking To Collaborators

- Confirm the best accepted model name: `timed_s0_d40_m170_f0p35_e1p00`.
- Confirm the first rejected model name: `timed_s0_d50_m170_f0p35_e1p00`.
- Confirm the best accepted values: E-MILES NIR-local `[Si/Mg]=0.499`, `d[M/H]=+0.095`, `d[Mg/Fe]=-0.070`, `dlogM=+0.137`, `dlogM/L=+0.053`.
- Confirm the first rejected values: E-MILES NIR-local `[Si/Mg]=0.523`, `d[M/H]=+0.113`, `d[Mg/Fe]=-0.085`, `dlogM=+0.168`, `dlogM/L=+0.072`.
- Rehearse the caveat: this is a PopIII/PISN-like Si-rich channel in copied code, not a production-code replacement.
- Rehearse the interpretation: lower high-Si regime is reachable; nominal Eftekhari-like `[Si/Mg]~0.67` is not reached without breaking relic constraints or invoking more localized/selective physics.

## Short Alex Response

The clean relic model remains strongly Mg-enhanced, so Mg/Fe is still the robust relicness tracer: systems that formed quickly and avoided later dilution should stay high in Mg/Fe. Si/Mg is more conditional. In these tests, Si/Mg becomes high only if a very early Si-rich PopIII/PISN-like channel operates during the compact formation episode. A true relic could preserve that signal, while normal ETGs may dilute it toward `[Si/Mg]~0` through later star formation, accretion, and aperture mixing. So the prediction is strong for Mg/Fe versus relicness, and conditional but interesting for Si/Mg versus relicness.

## Current Five Most Important Scientific Conclusions

1. The clean NGC1277-like relic baseline does not reach high Si/Mg: code-light `[Si/Mg]=0.058`, E-MILES NIR-local `[Si/Mg]=0.075`.
2. E-MILES NIR-local weighting and generic abundance reweighting do not rescue the clean baseline.
3. Pre-enriched initial gas is diluted, and mild two-component light mixing cannot reach nominal `[Si/Mg]~0.67`.
4. The best accepted timed Si-rich model reaches E-MILES NIR-local `[Si/Mg]=0.499` within the adopted relic-fit tolerance box.
5. Pushing the same channel higher reaches more Si/Mg but breaks relic constraints; the current framework does not reach nominal `[Si/Mg]~0.67` without additional physics or NIR abundance-response caveats.
