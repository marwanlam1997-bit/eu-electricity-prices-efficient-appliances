# EU household electricity prices & most energy-efficient appliances

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23540271.svg)](https://doi.org/10.5281/zenodo.23540271)

Open data maintained by **[EarlyDex](https://earlydex.com/)**, updated monthly. Also on
[Zenodo](https://doi.org/10.5281/zenodo.23540271) (archived release of each version) and [Kaggle](https://www.kaggle.com/datasets/marouanelamsalek/eu-electricity-prices-and-efficient-appliances).

- `data/electricity_prices_eu.csv`: average household electricity price in the 27 EU countries
  (€/kWh, all taxes included, Eurostat 2026-S1).
- `data/efficient_appliances.csv`: 3,894 fridge-freezers, refrigerators, washing machines, heat-pump
  tumble dryers and dishwashers from the official EU energy label database (EPREL), ranked by energy efficiency index, with
  the annual electricity cost in Germany and France.
- `data/report_2026_cost_by_country.csv` and `data/report_2026_models_by_class.csv`: the tables of the
  [EarlyDex report 2026](https://earlydex.com/fr/rapport-electromenager-electricite-ue/) (all 36,894 washing
  machines, dishwashers and tumble dryers registered in EPREL: share of each energy class and technology, same-size
  medians, and the yearly cost of three typical appliances in each EU country).

Last update: 2026-10-25.

## Report 2026: key figures

- The household price per kWh differs 3.4× across the EU, from Hungary (0.114 €) to Ireland (0.387 €) (Eurostat 2026-S1).
- 62 % of the washing machines registered in EPREL are energy class A, against 12 % of dishwashers and
  4 % of tumble dryers.
- At 8 kg, a heat-pump dryer uses a median 116 kWh per 100 cycles, against 307 for a conventional condenser dryer.
- Choosing class A instead of a typical model for the three appliances saves 46 € a year in Germany and
  31 € in France.

Full report: [Français](https://earlydex.com/fr/rapport-electromenager-electricite-ue/) ·
[Deutsch](https://earlydex.com/de/bericht-stromkosten-haushaltsgeraete-eu/).

## Electricity prices (2026-S1)

| Country | €/kWh |
|---|---|
| Ireland | 0.3871 |
| Germany | 0.3618 |
| Belgium | 0.3575 |
| Austria | 0.3260 |
| Italy | 0.3142 |
| Sweden | 0.3062 |
| Poland | 0.2999 |
| Czechia | 0.2884 |
| Romania | 0.2836 |
| Finland | 0.2694 |
| Cyprus | 0.2688 |
| Spain | 0.2509 |
| France | 0.2485 |
| Netherlands | 0.2440 |
| Latvia | 0.2415 |
| Greece | 0.2401 |
| Denmark | 0.2375 |
| Portugal | 0.2367 |
| Lithuania | 0.2162 |
| Estonia | 0.2118 |
| Slovenia | 0.2118 |
| Luxembourg | 0.2023 |
| Slovakia | 0.1985 |
| Croatia | 0.1816 |
| Bulgaria | 0.1341 |
| Malta | 0.1268 |
| Hungary | 0.1139 |

## Most efficient appliances (rank 1 in each category)

| Category | Model | Class | Label consumption | Cost per year (DE) |
|---|---|---|---|---|
| fridge freezer | [LG Electronics GBBSE261EV](https://earlydex.com/de/kuehl-gefrierkombination/lg-electronics-gbbse261ev-2801394/) | A | 73 kWh/year | 26.41 € |
| refrigerator | [Liebherr RBa30 425i_091624051](https://earlydex.com/de/kuehlschrank/liebherr-rba30-425i-091624051-1588553/) | A | 46 kWh/year | 16.64 € |
| washing machine | [Whirlpool WPM 912W ADS BE](https://earlydex.com/de/waschmaschine/whirlpool-wpm-912w-ads-be-2404815/) | A | 20 kWh/100 cycles (eco 40-60) | 15.05 € |
| heat pump tumble dryer | [AEG TR9XW80180 916900702](https://earlydex.com/de/waermepumpentrockner/aeg-tr9xw80180-916900702-2557560/) | A | 65 kWh/100 cycles | 36.69 € |
| dishwasher | [Bauknecht BK5IA5015BT1LS 7664597377](https://earlydex.com/de/geschirrspueler/bauknecht-bk5ia5015bt1ls-7664597377-2525912/) | A | 28 kWh/100 cycles (eco) | 26.34 € |

Full rankings with filters by brand and size: [earlydex.com/de/bestenlisten](https://earlydex.com/de/bestenlisten/)
(German) · [earlydex.com/fr/classements](https://earlydex.com/fr/classements/) (French).

## Method

- **Prices**: Eurostat table `nrg_pc_204`, household consumers with 2 500–4 999 kWh per year, all taxes and
  levies included, latest half-year.
- **Appliances**: models with status *published* in EPREL, from mainstream brands, with plausible values.
  Records whose declared energy class contradicts their energy efficiency index (EEI) are dropped.
  References with identical label values (same appliance sold under several model numbers, sometimes under a
  sister brand) are grouped into one row; `identical_references` counts the others.
- **Ranking**: by EEI (lower is better), then label consumption, then programme duration, then noise.
- **Annual cost**: label consumption × the country's average price. Washing machines assume 4 cycles per week,
  dishwashers 5, tumble dryers 3; refrigerating appliances use the label's annual value.
- `earlydex_page` is filled for the models that have their own page on EarlyDex; every row links to its
  official EPREL record.

Calculator for any appliance and country: [earlydex.com](https://earlydex.com/de/stromkosten-geraet/).

## License and citation

The data compilation is released under **CC BY 4.0**. Please cite:

> EarlyDex, *EU household electricity prices and energy-efficient appliances (EarlyDex open data)*,
> https://doi.org/10.5281/zenodo.23540271 (data: Eurostat; EU energy label database EPREL, European Commission).

Sources: Eurostat (CC BY 4.0) · EPREL, European Product Registry for Energy Labelling (European Commission).
EarlyDex is not affiliated with the European Commission or Eurostat.
