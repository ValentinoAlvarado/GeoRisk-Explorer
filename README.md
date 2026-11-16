# GeoRisk-Explorer
## Satellite-Based Flood Mapping and Geospatial Intelligence

GeoRisk-Explorer is an experimental geospatial AI workflow for binary water/flood segmentation from Sentinel-1 SAR observations. The current research configuration uses Sen1Floods11 v1.1 HandLabeled, Sentinel-1 VV/VH inputs, a TerraMind v1 Base encoder and a U-Net decoder.

### Current experimental evidence
Validation report: **86 samples**. Reported global pixel-level metrics:
- Flood IoU: **0.7003**
- Water Dice: **0.8237**
- Water Precision: **0.8273**
- Water Recall: **0.8201**

Qualitative examples recorded in the experiment outputs:
- Chip 000: IoU 0.7250
- Chip 050: IoU 0.8898
- Chip 002: IoU 0.0000

These results demonstrate variable segmentation performance and are presented with their limitations.

### Research context
The intended territorial application is flood analysis in Bajo Piura, Peru, with Catacaos as a proposed pilot area. The research direction includes hydroclimatic context, exposure analysis and geographic generalization.

### Current scope and limitations
This repository describes an **experimental flood-segmentation prototype**, not an operational warning service. The current public submission does not implement long-term Earth-system trend detection, NASA data acquisition, Sen's slope estimation or Mann–Kendall significance testing. Those functions must not be represented as completed.

The trained checkpoint is not included in this public submission. Reproducing inference requires the checkpoint, compatible dependencies and the original dataset, subject to their respective access and licensing terms.

### Main components
- Python / PyTorch geospatial workflow
- TerraMind v1 Base + U-Net decoder
- Sen1Floods11 v1.1 HandLabeled
- Sentinel-1 VV/VH
- Quantitative and qualitative validation
- Jupyter experimental notebook

### Demo
See [NASA Space Apps project demonstration](NASA_Space_Apps_Demo/Project_Demo.md) (seven-slide web-readable version).

### Data and software references
- Sen1Floods11: https://github.com/cloudtostreet/Sen1Floods11
- TerraTorch: https://github.com/torchgeo/terratorch
- IBM TerraMind: https://github.com/IBM/terratorch
- Copernicus Data Space: https://dataspace.copernicus.eu/

### AI assistance disclosure
AI-assisted tools were used for research assistance, writing and presentation preparation. The reported model metrics are outputs of the project's experimental evaluation pipeline, not AI-generated estimates.