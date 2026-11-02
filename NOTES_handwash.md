# Notes on handwashing variables (investigation)

## Construction
- handwash_basic: 1 if hv230b == 1, else 0
- handwash_place: 1 if inlist(hv230a,1,6), else 0 if hv230a==2
- handwash_env: 1 if handwash_basic == 1 & handwash_place == 1, else 0 if missing

## Issue
- handwash_env set to 0 when either component missing (line ~231) - conflates Limited with unknown/missing
- Complete-case filter does not include handwash_env
- Models use handwash_env - need consistency

## Recommendation
- Do not force missing to 0. Keep missing or create explicit category. Consider missingness analysis.
- Require both components or treat as missing.
