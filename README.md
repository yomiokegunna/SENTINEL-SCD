# SENTINEL-SCD

Surveillance and Evidence Network for Tracking, Intelligence, and Negating Excess Loss in Sickle Cell Disease

A privacy-preserving federated machine learning framework for predicting and reducing catastrophic healthcare utilisation in sickle cell disease (SCD) patients in Nigeria. SENTINEL-SCD implements a fully distributed logistic regression pipeline using the vantage6 federated learning platform, with all source data harmonised to the OMOP Common Data Model (CDM) v5.4 for interoperability with global federated research networks (OHDSI, EHDEN, INSPIRE).

Built on a real-world Nigerian SCD administrative dataset of 4,183 patients across two federated nodes, this repository documents the complete analytical pipeline — from OMOP CDM mapping and distributed feature selection through federated model training, validation, and result interpretation — without any raw patient data ever leaving its node of origin.

Key findings
Hydroxyurea receipt (12.8% coverage) is the dominant predictor of high healthcare utilisation (OR = 4.10, p < 0.001), interpreted as a confounding-by-indication marker of disease severity
Provider-level and ownership variables are non-significant after adjustment, indicating patient-level clinical factors — not health-system structure — drive utilisation patterns
Model AUC-ROC = 0.625; full federated pipeline reproducible end-to-end via vantage6
What's in this repository
Federated task configuration scripts (vantage6 client/node setup)
OMOP CDM mapping documentation and transformation scripts
Distributed feature selection pipeline (correlation filtering → L2 logistic regression → LONO cross-validation)
Analysis and visualisation code for descriptive statistics, regression outputs, and model evaluation
Manuscript and supplementary tables
