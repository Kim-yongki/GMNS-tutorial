# GMNS+ tutorial

A walking-and-transit network example for 30 TAZs in MORPC Traffic District 92, Central Ohio. The notebook converts and connects network data, checks the combined network, and compares 30-minute accessibility using free-flow and illustrative demand-dependent travel times.

## Contents

- `GMNS_Tutorial.ipynb`: tutorial code and explanations, without saved outputs.
- `raw_data/`: the OSM extract, COTA GTFS feed and MORPC TAZs used by the notebook. The archived bicycle inventory is retained as supplementary data.

## Run

1. Clone this repository or download and extract it.
2. Open `GMNS_Tutorial.ipynb` and run it from the repository folder.
3. Install the versions listed in Setup, restart the kernel, and run the cells in order.

The transfer and merge functions are installed from the [`importable` branch of the OSU GMNS repository](https://github.com/osu-travelbehavior/gmns/tree/importable):

```python
%pip install git+https://github.com/osu-travelbehavior/gmns.git@importable
```

Import them with `from osu_gmns import network_update, transfer_connector_builder, network_merge`.

Generated files are written to `step1_data/`, `step2_networks/`, `step3_zones/`, `step4_merge/` and `step6_accessibility/`. These folders are excluded from Git. The Setup cleanup cell removes existing generated step folders when `REMOVE=True`, while retaining the notebook and `raw_data/`.

## Data and interpretation

- OpenStreetMap data: © OpenStreetMap contributors, available under the [Open Database License](https://www.openstreetmap.org/copyright).
- Transit data: Central Ohio Transit Authority (COTA).
- TAZ and bicycle inventory data: Mid-Ohio Regional Planning Commission (MORPC).
