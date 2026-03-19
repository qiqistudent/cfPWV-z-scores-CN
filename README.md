# Reference Materials for cfPWV Z-Score Calculation in Chinese Children and Adolescents

This repository provides the code and reference materials used to calculate carotid-femoral pulse wave velocity (cfPWV) z-scores, based on sex-, age-, and height-specific reference models derived from a healthy population of Chinese children and adolescents.

## Contents

- `code/calculate_cfPWV_zscores.R`: calculates sex-specific cfPWV z-scores using the fitted models
- `models/cfPWV_Reference_Models.rds`: saved fitted reference models


## How to Use

1. Download the repository files.
2. Open R and load the `gamlss` package.
3. Load `models/cfPWV_Reference_Models.rds`.
4. Prepare an input dataset containing:
   - `sex`
   - `age`
   - `ht`
   - `cfPWV`
5. Run `code/calculate_cfPWV_zscores.R`.

## Input Variables

The input dataset must contain:
- `sex`: coded as `1/2` or `Male/Female`
- `age`: age in years
- `ht`: height in cm
- `cfPWV`: carotid-femoral pulse wave velocity

## Output Variables

The script returns:
- `z_score`: standardized cfPWV z-score
- `percentile`: percentile of observed cfPWV in the reference distribution
- `pred_median`: predicted median cfPWV for the participant’s sex, age, and height

## Notes

- The reference models were developed in Chinese children and adolescents aged 6–14 years.
- Predictions outside the original age or height range should be interpreted cautiously.
- This repository does not include raw participant-level data.

## Citation

If you use these scripts or reference values, please cite:

[Add your full paper citation here after publication]

## Contact

For questions, please contact:

qiqistudent@126.com or donghongbo@mail.ccmu.edu.cn
