# Paper 1 / Paper 2 interpretation from the weak/moderate sequence

## Main Result

The weak/moderate full ETG mass-sequence campaign shows that the environmentally varying IMF models can preserve the calibrated mass-metallicity and mass-[Mg/Fe] relations while allowing a controlled range of early PopIII/PISN-like Si-rich enrichment. Compatibility is not judged by [Si/Mg] alone: the accepted rows also satisfy stellar mass, metallicity, and [Mg/Fe] residual checks.

The safest normal-ETG preserved Si-rich channel is `d20_f0p10`. It is compatible for M1e10, M1e11, and M1e12, and it changes [Si/Mg] without breaking the global ETG calibration. M1e11 and M1e12 tolerate weak/moderate channels most naturally. M1e9 is a useful low-mass upper-limit diagnostic, but it is not a good anchor for the normal massive ETG interpretation because it begins near the upper normal [Si/Mg] range and has low [Mg/Fe].

## Paper 1 Paragraph

The weak/moderate sequence demonstrates that the updated environmentally varying IMF ETG models remain on the calibrated mass-metallicity and mass-[Mg/Fe] relations while allowing a controlled range of early Si-rich enrichment. This motivates a two-phase interpretation for normal ETGs, in which weak preserved Si-rich enrichment is compatible with the normal massive ETG locus, whereas stronger preservation is reserved for compact relics.

## Paper 2 Paragraph

The full ETG sequence provides the control population for the NGC1277 Si/Mg experiment. Normal massive ETGs are compatible only with weak or moderately preserved Si-rich enrichment, while relic-strength channels are expected to stand out only in high-preservation systems such as NGC1277.

## Differential Preservation Interpretation

[Mg/Fe] and [Si/Mg] are not redundant. [Mg/Fe] traces rapid formation generally, so both compact cores and old high-redshift envelope material can remain Mg-enhanced. [Si/Mg] is more selective: it tracks how strongly the brief early PopIII/PISN-like Si-rich enrichment phase is preserved. Normal ETGs can therefore remain alpha-enhanced while having lower [Si/Mg] than NGC1277-like relics.

## Channel Use

- `d20_f0p10`: preferred weak normal-ETG preserved channel.
- `d40_f0p10`: still useful as a moderate normal-ETG channel, especially for M1e11/M1e12.
- `d20_f0p20`: compatible for M1e11/M1e12, borderline for M1e10.
- `d40_f0p20`: boundary/upper-normal case.
- `d40_f0p35`: keep reserved for NGC1277/relic-strength testing, not normal ETG calibration.

## Collaborator Summary For Alex/Elham

The completed weak/moderate ETG sequence supports a differential-preservation picture. The normal massive ETG controls can keep their mass-metallicity and mass-[Mg/Fe] calibration while accepting only weak or moderate early Si-rich enrichment. The most conservative normal-ETG channel is `d20_f0p10`; stronger channels become boundary cases, and relic-strength preservation should be reserved for NGC1277-like systems. This means [Mg/Fe] remains the rapid-formation diagnostic, while [Si/Mg] is a more selective tracer of whether the brief early Si-rich PopIII/PISN-like phase was preserved.

## Counts

- Paper-facing normal-ETG-compatible rows: 12
- Borderline rows: 3
- Low-mass upper-limit rows: 5
- Too-strong-for-normal-ETG rows in the weak/moderate set: 0

## Caveats

These are copied-code fixed diagnostics, not new optimizations and not production-code replacements. M1e9, M1e10, and M1e11 use existing total-mass ETG rows as fixed upper-limit diagnostics; M1e12 uses the validated f_core=0.8 core model. The next physical step for the two-phase interpretation is to run core-mass fits for the lower-mass ETG sequence or refine f_core=0.6 before treating those rows as final two-phase models.
