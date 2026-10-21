# EU household electricity prices & most energy-efficient appliances

Open data maintained by **[EarlyDex](https://earlydex.com/)**, updated monthly.

- `data/electricity_prices_eu.csv`: average household electricity price in the 27 EU countries
  (€/kWh, all taxes included, Eurostat 2025-S2).
- `data/efficient_appliances.csv`: 3,894 fridge-freezers, refrigerators, washing machines, heat-pump
  tumble dryers and dishwashers from the official EU energy label database (EPREL), ranked by energy efficiency index, with
  the annual electricity cost in Germany and France.
- `data/report_2026_cost_by_country.csv` and `data/report_2026_models_by_class.csv`: the tables of the
  [EarlyDex report 2026](https://earlydex.com/fr/rapport-electromenager-electricite-ue/) (all 36,894 washing
  machines, dishwashers and tumble dryers registered in EPREL: share of each energy class and technology, same-size
  medians, and the yearly cost of three typical appliances in each EU country).

Last update: 2026-10-21.

## Report 2026: key figures

- The household price per kWh differs 3.7× across the EU, from Hungary (0.108 €) to Ireland (0.404 €) (Eurostat 2025-S2).
- 62 % of the washing machines registered in EPREL are energy class A, against 12 % of dishwashers and
  4 % of tumble dryers.
- At 8 kg, a heat-pump dryer uses a median 116 kWh per 100 cycles, against 307 for a conventional condenser dryer.
- Choosing class A instead of a typical model for the three appliances saves 49 € a year in Germany and
  32 € in France.

Full report: [Français](https://earlydex.com/fr/rapport-electromenager-electricite-ue/) ·
[Deutsch](https://earlydex.com/de/bericht-stromkosten-haushaltsgeraete-eu/).

## Electricity prices (2025-S2)

| Country | €/kWh |
|---|---|
| Ireland | 0.4042 |
| Germany | 0.3869 |
| Belgium | 0.3499 |
| Denmark | 0.3312 |
| Austria | 0.3272 |
| Czechia | 0.3217 |
| Italy | 0.2966 |
| Romania | 0.2893 |
| Cyprus | 0.2774 |
| Sweden | 0.2711 |
| Poland | 0.2709 |
| Spain | 0.2669 |
| Luxembourg | 0.2665 |
| France | 0.2561 |
| Netherlands | 0.2558 |
| Latvia | 0.2452 |
| Portugal | 0.2435 |
| Greece | 0.2381 |
| Estonia | 0.2303 |
| Finland | 0.2254 |
| Slovenia | 0.2121 |
| Lithuania | 0.1955 |
| Slovakia | 0.1853 |
| Croatia | 0.1658 |
| Bulgaria | 0.1355 |
| Malta | 0.1282 |
| Hungary | 0.1082 |

## Most efficient appliances (rank 1 in each category)

| Category | Model | Class | Label consumption | Cost per year (DE) |
|---|---|---|---|---|
| fridge freezer | [LG Electronics GBBSE261EV](https://earlydex.com/de/kuehl-gefrierkombination/lg-electronics-gbbse261ev-2801394/) | A | 73 kWh/year | 28.24 € |
| refrigerator | [Liebherr RBa30 425i_091624051](https://earlydex.com/de/kuehlschrank/liebherr-rba30-425i-091624051-1588553/) | A | 46 kWh/year | 17.80 € |
| washing machine | [Whirlpool WPM 912W ADS BE](https://earlydex.com/de/waschmaschine/whirlpool-wpm-912w-ads-be-2404815/) | A | 20 kWh/100 cycles (eco 40-60) | 16.10 € |
| heat pump tumble dryer | [AEG TR9XW80180 916900702](https://earlydex.com/de/waermepumpentrockner/aeg-tr9xw80180-916900702-2557560/) | A | 65 kWh/100 cycles | 39.23 € |
| dishwasher | [Bauknecht BK5IA5015BT1LS 7664597377](https://earlydex.com/de/geschirrspueler/bauknecht-bk5ia5015bt1ls-7664597377-2525912/) | A | 28 kWh/100 cycles (eco) | 28.17 € |

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

> EarlyDex, *EU household electricity prices & most energy-efficient appliances*, https://earlydex.com/ (data:
> Eurostat; EU energy label database EPREL, European Commission).

Sources: Eurostat (CC BY 4.0) · EPREL, European Product Registry for Energy Labelling (European Commission).
EarlyDex is not affiliated with the European Commission or Eurostat.
