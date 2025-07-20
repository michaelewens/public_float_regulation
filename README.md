# Summary

This repository contains data and some code for the research paper "[Regulatory Costs of Being Public: Evidence from Bunching Estimation](https://osf.io/preprints/socarxiv/pdv8n/)" (Ewens, Xiao and Xu 2024).

## Public float data

We collect public float data from firms' 10-K filings.  These filings disclose the market value of all outstanding common equity (voting and non-voting) held by non-affiliates at the end of the second fiscal quarter.  [The data](https://github.com/michaelewens/public_float_regulation/blob/main/public_float.csv.zip  ) (`public_float.csv`) contains `cik` (SEC identifier), link_txt	`link_htm_index` (link to filing that contains the accession number),	`comissionfileno` (html version of previous) the date of reporting (`publicfloat_date`), the year of the float (publicfloat_year`) and public float in millions (`publicfloat_mil`). This dataset contains all CIK-years with a positive public float. Firms that did not file a 10-K, did not disclose public float, or had no publicly traded shares are excluded from the dataset.

## Length of 10-K and 10-KSB parts: small firms, 1994-2007

For the set of public firms with $25m or less public float, we collected all the 10-K and 10-KSB filings from 1994-2007.  We then parsed each file (after removing html and line breaks) to create simple string lengths of each of the 4 parts of the annual report.  The goal of this exercise was to determine the real differences in total disclosure (in characters) for "small business issuers" vs. other firms during the sample period.   [The data is available here](https://github.com/michaelewens/public_float_regulation/blob/main/length10K_less25m_float.csv) and has the following variables:

- `cik`: SEC identifier
- `form`: form type
- `coname`: company name
- `fyear`: fiscal year
- `fsize`: the raw file size (in MB) of the 10-K or 10-KSB filing
- `url`: the link to the filing
- `sbi`: equal to one if the company was a "small business issuer" in that year, 0 otherwise.
- `lengthpart*`: the length (i.e., non-html or line break characters) for sections n=1,2,3 and 4
- `missingPart*`: equal to 1 if the part reference -- 1,2,3 or 4 -- was not found in the filing

## Urls to 10-K filings

[This data(zipped csv)](https://github.com/michaelewens/public_float_regulation/blob/main/sec_10Klinks_all.csv.zip) contains the URLs to all 10-K and 10-KSB links from 1994 to 2020 (last update 12/1/2020).  We used a subset of these links to build the 10-K(SB) length data posted on the repository.  The variables in the file are:

- `cik`: SEC identifier
- `reportingdate`: date of 10-K fiscal year
- `form`: form type 
- `filedate`: date of filing 
- `fname`: the URL to the filing
- `coname`: company name


## Citation

Please use the following citation if you use this data:

Ewens, Michael, Kairong Xiao, and Ting Xu. "Regulatory costs of being public: Evidence from bunching estimation." Journal of Financial Economics 153 (2024): 103775.

### Bibtex
`@article{ewens2024regulatory,
  title={Regulatory costs of being public: Evidence from bunching estimation},
  author={Ewens, Michael and Xiao, Kairong and Xu, Ting},
  journal={Journal of Financial Economics},
  volume={153},
  pages={103775},
  year={2024},
  publisher={Elsevier}
}`

