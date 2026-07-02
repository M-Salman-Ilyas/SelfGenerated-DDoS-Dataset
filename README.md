

=======
# Self-Generated DDoS Network Traffic Dataset

Self-generated DDoS network traffic dataset for cross-dataset intrusion detection and domain shift analysis

## Overview
This repository contains a self-generated network traffic dataset developed for
research on the generalization capability of machine learning-based Network
Intrusion Detection Systems (NIDS). The dataset was created in a controlled
VMware-based enterprise-like laboratory environment and is intended to support
cross-dataset evaluation and domain shift analysis against the CICIDS2017
benchmark dataset.

The dataset contains both raw packet capture (PCAP) files and flow-based CSV
files generated using CICFlowMeter.

## Repository Structure

Dataset/
├── PCAP_Files/
│   ├── benign_*.pcap
│   ├── goldeneye_*.pcap
│   ├── http_dos_hulk_*.pcap
│   ├── slowhttptest_*.pcap
│   └── slowloris_*.pcap
├── CSV_Files/
│   ├── *_merged.csv
│   ├── *_labeled.csv
│   ├── final_combined.csv
│   ├── final_binary_eval_large.csv
│   └── xfinal_combined.csv
└── README.md

## Traffic Categories
- BENIGN
- HTTP DoS Hulk
- GoldenEye
- Slowloris
- SlowHTTPTest

For binary classification:
- BENIGN = Normal traffic
- ATTACK = Aggregation of all DDoS attack classes

## Flow Generation
CSV files were generated from the PCAP captures using CICFlowMeter. The tool
converts packet captures into bidirectional network flows and extracts a rich
set of statistical features, including timing, packet-length, TCP flag, bulk
transfer, and window-size attributes.

General procedure:
1. Capture raw traffic and save as PCAP.
2. Process each PCAP using CICFlowMeter.
3. Export flow records to CSV.
4. Merge CSV files and assign labels.
5. Perform preprocessing (remove invalid values, handle missing values, etc.).

## Intended Use
The dataset is intended for:
- Cross-dataset IDS evaluation.
- Domain shift analysis.
- DDoS detection research.
- Domain adaptation and transfer learning studies.
- Benchmarking ML/DL intrusion detection models.

## Citation
If you use this dataset, please cite the associated publication and the Zenodo
dataset DOI https://doi.org/10.5281/zenodo.21128283.

## License
This dataset is released under the Creative Commons Attribution 4.0
International (CC BY 4.0) License for academic and research use.
>>>>>>> 4c3cf74 (Clean dataset upload using Git LFS)
