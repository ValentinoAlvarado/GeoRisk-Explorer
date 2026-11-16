# GeoRisk-Explorer — NASA Space Apps Challenge Demo

The seven-slide project demonstration is provided as a PDF and editable PowerPoint in this folder.

**Project:** Satellite-based flood mapping and geospatial intelligence using Sentinel-1 SAR, Sen1Floods11, and TerraMind v1 Base with a U-Net decoder.

**Current scope:** Experimental binary water segmentation, qualitative diagnostics, and quantitative validation. Long-term Earth-system trend analysis and statistical significance testing are future work, not implemented features.

## Files
- `GeoRisk_Explorer_NASA_Space_Apps_Demo.pdf` — submission-ready seven-slide demo.
- `GeoRisk_Explorer_NASA_Space_Apps_Demo.pptx` — editable source presentation.

## Evidence
The validation report covers 86 samples. Reported global pixel-level metrics: Flood IoU 0.7003, Water Dice 0.8237, Water Precision 0.8273, and Water Recall 0.8201. Individual examples include chip 000 (IoU 0.7250), chip 050 (0.8898), and chip 002 (0.0000).

## Limitations
The selected model checkpoint is not included. The repository does not currently implement NASA data acquisition, time-series trend estimation, or statistical significance testing. Do not interpret this demo as a completed Earth System Trend Detector.

## Data and software attribution
- Sen1Floods11: https://github.com/cloudtostreet/Sen1Floods11
- TerraMind: https://github.com/IBM/terratorch (TerraMind model documentation and implementation references should be checked against the actual installed package/version)
- TerraTorch: https://github.com/torchgeo/terratorch
- Copernicus Data Space: https://dataspace.copernicus.eu/

AI assistance was used for drafting and presentation preparation. Model predictions and reported metrics are experimental outputs of the project pipeline.