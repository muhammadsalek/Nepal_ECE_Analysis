# Survey design notes

## Current
- svyset hv021 [pw=hv005/1000000], strata(hv022)
- use subpop() in some analyses
- filtering with keep before svy can affect representation

## Recommendation
- Use svyset on full dataset when possible; use subpop() for domains
- Document eligible population and filters
- Check consistency across Stata/R
