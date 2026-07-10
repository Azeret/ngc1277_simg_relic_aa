# Si/Mg Paper Figure And Table Plan

## Proposed Figures

### Figure 1. Baseline Relic Formation And Abundance History

- Existing source file if available: no final figure found in the Si/Mg analysis directory; source outputs likely under copied yield-channel output directories referenced by `mixed_popiii_channel_scan_v5.csv` and `preenriched_initial_gas_outputs_v1/`.
- Exists or needs remake: needs remake.
- Required columns: time or stellar generation age, formed mass or SFR, `[M/H]`, `[Mg/Fe]`, `[Si/Fe]`, `[Si/Mg]`, code luminosity or mass weight.
- Caption idea: Clean NGC1277-like relic formation history showing rapid enrichment and high `[Mg/Fe]`, but low `[Si/Mg]`.

### Figure 2. Clean vs Mild vs Best Accepted vs Rejected Si/Mg Comparison

- Existing source file if available: `/home/tereza/early_type_galaxies/results/yield_channel_tests/analysis/final_relic_simg_key_models.png`.
- Exists or needs remake: exists as a compact current figure; likely needs manuscript styling.
- Required columns: `model_name`, `model_type`, `current_code_light_SiMg`, `E_MILES_NIR_SiMg`, `accepted`, `primary_limiting_constraint`.
- Caption idea: Key Si/Mg ladder from clean baseline to mild enrichment, best accepted timed enrichment, and rejected high-Si models.

### Figure 3. Si/Mg Versus Relic-Fit Degradation / Pareto Plot

- Existing source file if available: no dedicated figure found; source tables are `constrained_simg_local_refinement_v1.csv` and `high_simg_failure_modes_v1.csv`.
- Exists or needs remake: needs remake.
- Required columns: `model_name`, `emiles_nir_SiMg`, `degradation_score`, `delta_MH`, `delta_MgFe`, `delta_logM`, `delta_logML`, `accepted`, `primary_rejection_reason`.
- Caption idea: Raising Si/Mg is possible, but accepted models terminate near `[Si/Mg]_NIR~0.5` because higher-Si cases cross coupled relic-fit constraints.

### Figure 4. E-MILES NIR-Local Weighting Effect

- Existing source file if available: no final figure found; source table is `emiles_nir_flux_weighted_abundances_v1.csv`.
- Exists or needs remake: needs remake.
- Required columns: `model_name`, `experiment_type`, `imf_slope_for_weights`, `weighting_region`, `final_weighted_SiMg`, `current_code_light_weighted_SiMg`, `delta_SiMg_from_current_code_light_weighted`.
- Caption idea: NIR-local weighting barely changes the clean baseline but amplifies models that already contain chemically Si-rich stellar generations.

### Figure 5. Timing-Window Boundary: 40 Myr Accepted vs 50 Myr Rejected

- Existing source file if available: no dedicated figure found; source table is `constrained_simg_local_refinement_v1.csv`.
- Exists or needs remake: needs remake.
- Required columns: `injection_start_time_Myr`, `injection_duration_Myr`, `popiii_mass`, `popiii_fraction`, `mixing_efficiency`, `emiles_nir_SiMg`, `delta_MH`, `delta_MgFe`, `delta_logM`, `delta_logML`, `accepted`.
- Caption idea: Extending the same early Si-rich channel from 40 to 50 Myr raises Si/Mg but crosses the metallicity, Mg/Fe, and mass boundaries.

### Figure 6. Conceptual Si/Mg And Mg/Fe Versus Relicness Prediction

- Existing source file if available: no existing quantitative figure found.
- Exists or needs remake: needs new conceptual or data-backed figure.
- Required columns: relicness metric or proxy, `[Mg/Fe]`, `[Si/Mg]`, age, accreted/light fraction, model family.
- Caption idea: `[Mg/Fe]` should correlate robustly with relicness, while `[Si/Mg]` is predicted to correlate only when an early Si-rich channel operated and was not diluted.

## Proposed Tables

### Table 1. Key Model Comparison Table

- Existing source file if available: `final_relic_simg_key_models.csv`.
- Exists or needs remake: exists; verify numbers before manuscript use.
- Required columns: `model_name`, `model_type`, `current_code_light_SiMg`, `E_MILES_NIR_SiMg`, `dMH`, `dMgFe`, `dlogM`, `dlogML`, `accepted`, `primary_limiting_constraint`, `interpretation`.
- Caption idea: Clean, mild, accepted, and rejected models defining the current Si/Mg result.

### Table 2. Yield-Channel Parameter Table

- Existing source file if available: `best_accepted_relic_simg_model_card.csv`, `mixed_popiii_channel_scan_v5.csv`, and `constrained_simg_local_refinement_v1.csv`.
- Exists or needs remake: needs manuscript table built from existing CSVs.
- Required columns: model name, injection start, duration, representative PopIII/PISN-like mass, fraction, mixing efficiency, cutoff settings if applicable, source table, copied-code flag.
- Caption idea: Parameters of the PopIII/PISN-like Si-rich yield-channel experiments.

### Table 3. Acceptance/Rejection Criteria Table

- Existing source file if available: values documented in `BEST_ACCEPTED_RELIC_SIMG_MODEL_CARD.md`, `CONSTRAINED_SIMG_LOCAL_REFINEMENT_V1.md`, and `HIGH_SIMG_FAILURE_MODES_V1.md`.
- Exists or needs remake: needs manuscript table.
- Required columns: observable, tolerance, best accepted delta, first rejected delta, limiting status.
- Caption idea: Adopted relic-fit tolerance box and how the 40 Myr accepted model and 50 Myr rejected model compare.

### Table 4. Caveat/Systematic Table

- Existing source file if available: caveats spread across `ABUNDANCE_WEIGHTING_BAND_COMPARISON_V1.md`, `EMILES_NIR_FLUX_WEIGHTED_ABUNDANCES_V1.md`, `EMILES_EFTEKHARI_NIR_INDICES_V1.md`, and `BEST_ACCEPTED_RELIC_SIMG_MODEL_CARD.md`.
- Exists or needs remake: needs manuscript table.
- Required columns: systematic, current treatment, impact on conclusion, required future check.
- Caption idea: Current limitations separating chemical-evolution abundance proxies from full NIR spectral-index abundance inference.
