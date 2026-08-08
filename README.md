**English** | [한국어](README.ko.md)

# Young Men and Women Are Drifting Apart in Space (South Korea, 1998–2025)

> ### **[▶ Open the map — wherewindstay.github.io/gendered-space](https://wherewindstay.github.io/gendered-space/)**
>
> *Follow the link to move the year slider and click districts. GitHub does not run interactive content inside a README.*

Put the country on a scale and find where it balances: that point is the **centre of population**. Give every district its centroid, weight each by how many people live there, and the average is a single point standing in for the whole group. Split the group by sex and age, compute a point for each, and you can see who moved further, and in which direction.

Over 1998–2025 the centre of population for **young women moved 22.9 km**, for **young men 18.1 km**, against **13.1 km** for the population as a whole — all of them northwest, toward the capital region. The distance between the young men's and young women's points widened from **2.2 km to 6.7 km**. Across the same years the gap for all ages stayed under 1 km. The divergence belongs to the young.

The map is an interactive rebuild of the three static figures in Sohyun Park, ["Deepening gender conflict shows up in space too"](https://www.pressian.com/pages/articles/2024110722251788361) (*Pressian*, November 2024), extended with the 2024 and 2025 data releases.

## What you see

| Panel | What it shows |
|---|---|
| Left map | Trajectories of three centres of population — total, young men, young women — from 1998 to the selected year, with the year-by-year distance between the two young cohorts |
| Right map | Sex ratio of the young population by district in the capital region (Seoul, Incheon, Gyeonggi), with a colour key. The trend panel shows the capital region as a whole until you click a district; click the same district again to go back |
| Slider | Moves both maps and both graphs together; ▶ plays the sequence |

Each map carries its own legend and its own small graph. There is nothing below the maps except the year slider.

Young = ages 19–34, following Korea's Framework Act on Youth. Sex ratio = men per 100 women.

## Data

| What | Source |
|---|---|
| Population | Statistics Korea (KOSIS), mid-year registered population by district, sex and 5-year age band, [101_DT_1B040M5](https://kosis.kr/), 1998–2025 |
| District boundaries | Statistics Korea SGIS, administrative boundaries, 2021 Q4 |
| Base map | CARTO light tiles, © OpenStreetMap contributors |

Centres of population for 1998–2023 come from the author's own `centroid_sgg.R`. The 2024 and 2025 points were computed here by the same method — district centroid weighted by population, on the 2021 Q4 boundaries. Recomputing 2023 with that code reproduces the original figures to within 0 m, so the two segments join without a step.

## What the map cannot tell you

- **Boundaries are fixed at the 2021 edition** so that the whole series is measured against one geography. Reorganisations after that date — including the 2026 creation of new districts in Incheon — are not reflected.
- **Absolute position mixes in where people are registered, not only where they live.** Military service and university enrolment both move a young person's registration. The trajectories are drawn to compare *how far each group travelled*, not to locate them.
- **Ansan and Yongin report population at city level while the boundary file is at ward level.** The city figure is shown for each of its wards, so differences within those two cities do not appear.
- **Merged cities are counted once.** Where a city and its wards both appear in the source, the city row is dropped — but only in years where ward rows actually exist. Bucheon abolished its wards in 2016 and restored them in 2024, so the rule has to be applied year by year rather than by name.
- **Old district codes are carried onto current boundaries** (Incheon Nam-gu → Michuhol-gu, Bucheon's three wards, five counties promoted to cities) so that moving the slider backwards does not open holes in the series. Two districts still begin late — Yeongtong-gu in 2003 and Ilsanseo-gu in 2005 — because they did not exist before then.
- **The initial view of the right map excludes Ongjin-gun** from its extent. Ongjin's islands reach 124.7°E, and including them squeezes Seoul and Gyeonggi into a corner. Ongjin is still drawn; zoom out one step to see it.
- **The centre of population is a summary, not a place.** Two very different distributions can share the same centre. It answers "which way did this group move" and nothing finer.

## Reading the sex ratio

In 1998 the extremes were Ongjin-gun at 140.2 and Ilsan-gu at 85.1. By 2025 they were Ongjin-gun at 241.4 and Mapo-gu at 80.8. Seoul and its inner suburbs have tilted toward women; the border counties (Ongjin, Yeoncheon, Pocheon, Gapyeong) and the manufacturing belt (Icheon) toward men. Ongjin's figure reflects a small resident population alongside military and fishing employment, so it should be read as a ratio, not as a count.

## Technical notes

- Single self-contained HTML file. Leaflet is embedded rather than loaded from a CDN, so the page works when opened directly from disk. Only the base-map tiles need a network.
- No build step and no framework: the charts are SVG written directly.
- Text on the page is generated from the data, so the figures quoted in the introduction stay correct when a new year is added.

## License and citation

| What | License |
|---|---|
| Source code | [MIT](LICENSE) |
| Written content, figures, analytical results | [CC BY 4.0](CONTENT-LICENSE.md) |
| Source data | Terms of each provider (see Data above) |
| Bundled Leaflet 1.9.4 | BSD-2-Clause, © Vladimir Agafonkin |
| Base-map tiles | © CARTO, © OpenStreetMap contributors |

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21842363.svg)](https://doi.org/10.5281/zenodo.21842363)

To cite this work:

> Park, S. (2026). *Young Men and Women Are Drifting Apart in Space (South Korea, 1998-2025)* (v1.0.0). Zenodo. https://doi.org/10.5281/zenodo.21842363

Reuse is welcome. Please credit Sohyun Park and cite the work. GitHub's
**Cite this repository** button reads [CITATION.cff](CITATION.cff) and will give you BibTeX.
