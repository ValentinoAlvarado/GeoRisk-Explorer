# GeoRisk-Explorer — Project Demo
### NASA Space Apps Challenge | Be an Earth System Trend Detective!

> **Scope clarification:** This demo presents the current GeoAI flood-segmentation prototype and its research pathway. It does not claim that long-term Earth-system trend analysis or significance testing has already been implemented.

---

## Slide 1 — GeoRisk-Explorer
**Satellite-Based Flood Mapping and Geospatial Intelligence**

An experimental geospatial AI workflow for mapping water-affected areas from Sentinel-1 SAR observations.

Research application: Bajo Piura, Peru; Catacaos as a proposed pilot area.

## Slide 2 — The Earth Observation Problem
Flood extent is difficult to observe consistently during cloudy conditions and across large territories. Synthetic Aperture Radar (SAR) provides an observation source that can support flood mapping independent of daylight and with reduced dependence on cloud-free optical imagery.

**Current input:** Sentinel-1 VV/VH SAR imagery.

## Slide 3 — Data and GeoAI Architecture
- Dataset: Sen1Floods11 v1.1 HandLabeled
- Inputs: Sentinel-1 VV/VH
- Encoder: TerraMind v1 Base
- Decoder: U-Net
- Task: binary semantic segmentation
- Positive class: water
- Ignore index: -1

The notebook and source modules organize experiment inspection, validation and visualization.

## Slide 4 — Qualitative Results
The experiment includes per-chip comparisons of SAR input, reference mask and model prediction.

Recorded examples:
- Chip 000: IoU 0.7250
- Chip 050: IoU 0.8898
- Chip 002: IoU 0.0000

The examples intentionally show both successful and failed segmentation cases. Performance is not uniform across scenes.

## Slide 5 — Quantitative Validation
Validation report: **86 samples**.

| Metric | Result |
|---|---:|
| Flood IoU | 0.7003 |
| Water Dice | 0.8237 |
| Water Precision | 0.8273 |
| Water Recall | 0.8201 |

Metrics are global pixel-level results from the recorded validation report. They should not be interpreted as geographic generalization or operational accuracy.

## Slide 6 — From Flood Mapping to Earth-System Understanding
The current prototype addresses the flood-observation and segmentation component. A scientifically grounded extension would connect independently acquired NASA Earth-science time series (for example, precipitation) with the mapped flood observations and territorial context.

**Not yet implemented:** NASA time-series ingestion, trend estimation, Sen's slope, Mann–Kendall testing and statistical significance assessment.

## Slide 7 — Impact and Next Steps
GeoRisk-Explorer establishes an experimental workflow that can support further research into satellite-based flood mapping and territorial analysis.

Next steps:
1. Integrate a documented NASA Earth-science variable and region-specific time series.
2. Estimate temporal trends and test significance while accounting for seasonality and autocorrelation.
3. Extend geographic validation and exposure analysis.
4. Translate validated outputs into interpretable information for disaster-risk research.

**The current contribution is an experimental flood-segmentation prototype, with trend analytics identified as future work.**

---

### Data and software references
- Sen1Floods11: https://github.com/cloudtostreet/Sen1Floods11
- TerraTorch: https://github.com/torchgeo/terratorch
- Copernicus Data Space: https://dataspace.copernicus.eu/

### AI assistance
AI-assisted tools were used for research assistance and preparation of written materials. See the repository README for scope and limitations.