


# Apache Spark Project – Lending Club Data Engineering (Part 2)

## Overview

This part extends the Part 1 pipeline by adding "loan scoring, Hive integration, modularized PySpark code, virtual environments, unit testing, and logging".



## Key Objectives

1. "Loan Score Calculation"

   * Based on:

     * Repayment history (20%)
     * Default history (45%)
     * Financial health (35%)
   * Higher score = higher chances of loan approval.

2. "Hive External Tables"

   * Permanent tables created on top of cleaned Parquet datasets:

     * `customers`
     * `loans`
     * `loans_repayments`
     * `loans_defaulters_delinq`
     * `loans_defaulters_detail_rec_enq`
   * Managed & external table usage explained.

3. "Data Consolidation"

   * Unified dataset combining 5 cleaned sources.
   * Weekly jobs for aggregated loan risk analysis.

4. "Project Environment Setup"

   * Python virtual environments via "pipenv".
   * Each project isolated with its own Python & PySpark versions.

5. "Modularized Project Structure"

   * `ConfigReader.py` → Reads environment configs.
   * `DataReader.py` → Loads customers & loans data.
   * `DataManipulation.py` → Transformations (joins, filters, aggregations).
   * `Utils.py` → Spark session creation with Hive support.
   * `application_main.py` → Entry point for the pipeline.

6. "Unit Testing"

   * Framework: "pytest"
   * Test cases cover:

     * Data counts
     * Aggregations
     * Filter functions
   * Fixtures used for Spark session setup/teardown.

7. "Logging"

   * Integrated with "log4j" for better application monitoring.
   * Configurable logging levels: `DEBUG`, `INFO`, `WARN`, `ERROR`, `FATAL`.

---

## Tools & Technologies

* "PySpark"
* "Hive (Metastore + External Tables)"
* "Pipenv" (virtual environment)
* "Pytest" (unit testing)
* "Log4j" (logging)
* "VSCode  for development

