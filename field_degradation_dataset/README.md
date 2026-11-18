# Global PV field degradation database (release v1.0)

Field-measured annual degradation rates of PV modules and systems, extracted from 662 peer-reviewed papers and conference proceedings (1980-2026) with a large language model and validated against each source PDF. This is the dataset behind:

> B. Li, D. C. Jordan, M. Springer, D. Chin, R. Daxini, A. Jain, [title], [journal], [year]. DOI: [to add]

Download: [DuraMAT DataHub](https://datahub-duramat.nlr.gov/data-repo/projects/8c329288-3b34-46ad-9ec5-d62bb06dd664/datasets/9d8e61a8-652b-4de0-949c-dd83010f516d)

## Files

| File | Content |
|---|---|
| `pv_field_degradation_records.csv` | 2,210 records, one per reported degradation rate, sorted by publication year and paper |

## pv_field_degradation_records.csv

| Column | Content |
|---|---|
| paper_id | source paper (Scopus EID, EU PVSEC paper number, or `ext-` ID for papers taken from earlier reviews) |
| paper_authors, paper_title, publication_year, publication_source, paper_doi | source paper |
| found_via | Scopus, EU PVSEC proceedings, or reference list of an earlier review |
| degradation_rate_pct_per_year | annual degradation rate, %/year; negative = loss |
| duration_years | field exposure covered by the rate, years |
| start_year, end_year | first and last year of the data behind the rate |
| rate_metric | performance metric behind the rate: Power, Performance Ratio, Outdoor I-V, Indoor I-V, Efficiency, PVUSA (`; `-separated if several) |
| rate_stated_by_author | true if the paper states the annual rate itself |
| number_of_measurements | number of measurements behind the rate |
| initial_power_source | reference for the initial power: nameplate or field measurement |
| total_power_loss_pct | total power loss reported by the paper, % (may cover a different window or population than the rate) |
| pv_technology | mono-c-Si, multi-c-Si, c-Si (type not stated), HJT, a-Si, CdTe, CIGS, thin film (type not stated), mixed, other; blank if not stated |
| pv_module_name | module make and model |
| module_nominal_power_w | module nameplate power, W |
| number_of_modules | number of modules behind the rate |
| system_capacity_w | system capacity, W |
| study_scope | module or system |
| mounting | ground-rack, roof-rack, roof-flush, roof-unspecified, rack-unspecified, tracker, facade, other, not_reported |
| tilt_deg | module tilt, degrees |
| location_name | site name (test facility, plant or city with region), written from the paper's location statement; `multiple sites` for multi-site records; blank if the paper names no site |
| country, continent | exposure site (`multiple (...)` for multi-country records) |
| latitude, longitude | exposure site, decimal degrees; blank if the paper does not name the site (the analysis-set flags and climate zones of 38 such records follow the paper, which used region-level coordinates) |
| pvcz_temperature_zone, pvcz_humidity_zone | PV climate zone (Karin et al., 2019): T1-T8, H1-H5 |
| faults_observed | faults reported for the modules or system (`; `-separated) |
| faults_attributed | faults the authors link to the degradation |
| reversible_losses | soiling, shading, snow or ice cover |
| reversible_loss_in_rate | whether a reversible loss is included in the rate: yes, possibly, no, none reported |
| note | caveat of a kept value (bound, qualitative zero, one-off failure, internal inconsistency of the paper, shading loss instead of degradation) |
| in_complete_info_set | rate, PV technology, duration and coordinates available (1,710 records) |
| in_rate_distribution_set | used for the rate distribution: duration > 1 yr, rate >= -10 %/yr, no reversible loss in the rate (1,473 records) |
| in_model_set | used for the LightGBM/SHAP model (1,033 records; filters in the paper, Table 2) |

## Scope

Included: field-measured power, energy or performance-ratio degradation of PV modules or systems, including rates affected by reversible losses (flagged). Not included: values cited from other studies, model inputs or simulations, laboratory or accelerated tests, Isc-only or optical losses, rates relative to another technology or string, non-power metrics.

Extraction accuracy (independent re-extraction of 303 randomly selected papers with every disagreement resolved against the PDF): degradation rate 95.9%, PV technology 97.5%, study scope 97.5%, country 99.3%.

## License and citation

[License: CC BY 4.0, to confirm.] Please cite the paper above. The extraction prompts and analysis code are at https://github.com/lbj2011/PV-LLM; an interactive view is at https://pvtools.lbl.gov/field-degradation.
