# Summary

This repository contains data and some code for the research paper "[Regulatory Costs of Being Public: Evidence from Bunching Estimation](https://osf.io/preprints/socarxiv/pdv8n/)" (Ewens, Xiao and Xu).

## Public float data

We collect public float data from firms' 10-K filings.  These filings disclose the market value of all outstanding common equity (voting and non-voting) held by non-affiliates at the end of the second fiscal quarter.  [The data](https://github.com/michaelewens/public_float_regulation/blob/main/public_float.csv) (`public_float.csv`) contains `cik` (SEC identifier), the year (`publicfloat_year`) and public float in millions (`publicfloat_mil`)

## Length of 10-K and 10-KSB parts: small firms, 1994-2007

Coming soon.

## Urls to 10-K filings

This data contains the URLs to all 10-K and 10-KSB links from 1994 to 2020 (last update 12/1/2020).  We used a subset of these links to build the 10-K(SB) length data posted on the repository.  The variables in the file are:

- `cik`: SEC identifier
- `reportingdate`: date of 10-K fiscal year
- `form`: form type 
- `filedate`: date of filing 
- `fname`: the URL to the filing
- `coname`: company name


## Citation

Please use the following citation if you use this data:

Ewens, Michael, Kairong Xiao, and Ting Xu. 2020. “Regulatory Costs of Being Public: Evidence from Bunching Estimation.”  doi:10.31235/osf.io/pdv8n.

### Bibtex
`@article{ewens_xiao_xu_bunching,
title={Regulatory Costs of Being Public: Evidence from Bunching Estimation},
author={Ewens, Michael and Kairong Xiao and Ting Xu},
journal={Working paper},
year=2020
}`

