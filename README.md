# AAVAIL_Capstone_Project
## Project Overview

This project applies the AI workflow to the AAVAIL business problem. It covers data ingestion, exploratory data analysis (EDA), machine learning model development, API deployment, automated testing, logging, and performance monitoring.

## Peer Review Checklist

### 1. Are there unit tests for the API?
**Answer:** Yes, if implemented.

API unit tests verify that endpoints accept valid inputs, handle invalid requests, and return the expected predictions and response formats.

### 2. Are there unit tests for the model?
**Answer:** Yes, if implemented.

Model unit tests check that the trained model loads correctly, accepts the expected input features, and returns valid predictions.

### 3. Are there unit tests for the logging?
**Answer:** Yes, if implemented.

Logging tests verify that API requests, predictions, timestamps, model versions, and execution times are recorded correctly.

### 4. Can all unit tests be run with a single script, and do all tests pass?
**Answer:** Yes, if implemented and verified.

All unit tests can be executed using a single test script. The script should report whether the API, model, and logging tests pass.

### 5. Is there a mechanism to monitor performance?
**Answer:** Yes, if implemented.

The project records prediction-related information and execution times to support monitoring. Model performance can be evaluated periodically using appropriate metrics and available ground-truth outcomes.

### 6. Was there an attempt to isolate read/write unit tests from production models and logs?
**Answer:** Yes, if implemented.

Tests use separate test data, temporary files, and isolated test logs to avoid modifying production models, datasets, or logs.

### 7. Does the API work as expected, including predictions for a specific country and all countries combined?
**Answer:** Yes, if implemented and verified.

The API supports country-specific predictions and an aggregated response for all supported countries, using the documented request parameters.

### 8. Does data ingestion exist as a function or script to facilitate automation?
**Answer:** Yes, if implemented.

A dedicated data-ingestion function or script loads the source data and prepares it for exploratory analysis and model training.

### 9. Were multiple models compared?
**Answer:** Yes, if implemented.

Multiple candidate models are evaluated using the same evaluation procedure and suitable metrics. Their results are compared to identify a model that performs better than the baseline.

### 10. Did the EDA investigation use visualizations?
**Answer:** Yes, if implemented.

EDA visualizations help investigate data quality, missing values, customer churn, and differences in customer behavior across countries.

### 11. Is everything containerized within a working Docker image?
**Answer:** Yes, if implemented and verified.

A Dockerfile defines the application environment and dependencies. The container can be built and run using the documented instructions.

### 12. Was a visualization used to compare the model with the baseline model?
**Answer:** Yes, if implemented.

A comparison chart presents the baseline and candidate model results using a suitable evaluation metric, making their relative performance easier to assess.

## How to Run the Tests

After configuring the project environment and installing the dependencies, run:

```bash
bash run_tests.sh
```

## How to Run with Docker

Build the image:

```bash
docker build -t aavail-capstone .
```

Run the container:

```bash
docker run -p 8000:8000 aavail-capstone
```

## Project Structure

```text
aavail-capstone/
├── data/
├── src/
│   ├── ingest_data.py
│   ├── eda.py
│   ├── train_model.py
│   ├── predict.py
│   ├── api.py
│   └── logging_utils.py
├── tests/
│   ├── test_api.py
│   ├── test_model.py
│   └── test_logging.py
├── visualizations/
├── Dockerfile
├── requirements.txt
├── run_tests.sh
└── README.md
```

## Conclusion

This project aims to demonstrate an end-to-end AI workflow, from data preparation and model evaluation to API deployment, testing, logging, and monitoring. The implementation and test results should be verified before marking each peer-review criterion as complete.
