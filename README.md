# US Pay Transparency — Disclosure Rates from Live Job Postings

Open data on how often US job postings actually include a salary range, measured from live postings rather than surveys.

**As of 2026-08-14** · 197,384 live US postings · Source: [forgeapply.com/pay-transparency-report](https://forgeapply.com/pay-transparency-report)

## Headline

| | disclosure rate |
|---|---|
| States that require a pay range in the posting | **42.2%** |
| States with no such law | **16.1%** |
| **Ratio** | **2.6x** |
| All tracked US postings | 32.8% |

**The ten highest-disclosing states are all posting-law states.** Ranked by the share of live postings containing a pay range, positions 1 through 10 are Colorado, California, New York, Minnesota, Illinois, Washington, Massachusetts, DC, New Jersey and Vermont — every one a jurisdiction that requires a range in the listing. Virginia, with no such law, is the first non-law state at #11.

The two posting-law states that don't make the top 10 are worth naming:

- **Maryland** — 27.9%, 14th
- **Hawaii** — 21.9%, 19th, and it carries the strictest employer-size exemption of any of these laws (50+ employees), so a large share of Hawaii postings in this sample come from employers the law doesn't reach

At the bottom: Montana 3.5%, Nebraska 4.1%, South Dakota 4.7%, Rhode Island 6.8%, Kansas 7.3% — none with a posting requirement.

## Files

| file | contents |
|---|---|
| `disclosure_by_state.csv` | Per-state disclosure rates, whether the state has a posting law, the year the posting requirement took effect, and the employer-size threshold |

Columns: `state_code`, `state_name`, `posting_law`, `law_effective_year`, `employer_size_threshold`, `live_postings`, `postings_with_pay`, `disclosure_pct`

States with fewer than 100 live postings are omitted rather than shown noisy.

## Method

Every figure is computed from job postings **live at the time of measurement**, pulled directly from employers' applicant-tracking systems: Greenhouse, Lever, Ashby, Workable and Workday.

A posting counts as disclosing pay when the employer includes a salary range **in the posting text itself** — not on request, not at offer.

State assignment uses the posting's listed location. Fully remote roles without a state are excluded from state-level figures.

## Limitations — please read before citing

**This is a disclosure rate, not a compliance rate.** It counts every posting located in a posting-law state, including employers small enough to be exempt. Compliance requires knowing which employers the law actually binds.

The closest prior work is Audoly & Xing, [*Do Employers Comply with Pay Transparency Requirements in Job Postings?*](https://libertystreeteconomics.newyorkfed.org/2025/10/do-employers-comply-with-pay-transparency-requirements-in-job-postings) (Liberty Street Economics, Federal Reserve Bank of New York, October 2025). They found roughly **24% non-compliance** across Colorado, California, Washington and New York City, using Lightcast data through March 2025, with employer-size exemptions explicitly modelled. That is a stricter and narrower measure than this dataset, and the two numbers should not be compared directly. Where they agree is the part that matters: disclosure is several times more common where a posting law exists, and a substantial share of postings still omit pay years after the law took effect.

**The sample is not a random sample of US employers.** It covers employers publishing through those five ATS platforms, which skews toward technology and technology-adjacent companies and toward employers large enough to run a modern applicant-tracking system. Small businesses, government postings, and companies on legacy or custom career sites are essentially absent. Read this as *disclosure rates among ATS-published postings*, not *disclosure rates among all US jobs*.

**Employer-size thresholds are not modelled.** Almost every posting law binds only employers above a headcount — Hawaii 50+, Minnesota 30+, Massachusetts 25+, California and Washington 15+, New Jersey 10+, Vermont 5+, New York 4+ — and only Colorado and DC cover employers of any size. Because the sample skews large, most employers here do clear those thresholds, so the true rate among legally-covered employers is somewhat *higher* than shown, not lower.

**Figures move daily.** These describe currently-open roles and change as postings churn. Note the as-of date when citing, and prefer linking to the source over hardcoding a number.

**Posting-law status is a snapshot, not legal advice.** State pay-transparency law changes frequently. The twelve jurisdictions treated here as requiring a range in the posting are California, Colorado, Hawaii, Illinois, Maryland, Massachusetts, Minnesota, New Jersey, New York, Vermont, Washington and Washington DC. Check current statutes before relying on this for compliance purposes.

## Citation

> ForgeApply, *US Pay Transparency Report*, August 2026. https://forgeapply.com/pay-transparency-report

Free to cite and republish with attribution and a link.

For custom cuts — a specific state, metro, industry, employer, or time window — email support@forgeapply.com. We can usually turn queries around same day.
