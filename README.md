# DHR Data Pipeline

This repository contains the key components to build the DHR ETL pipeline in order to standardise and harmonise multi-modal patient data using a unified data standard.

## DHR pipeline components

The various components of the pipeline are as follows;

1. **Data Model**: Contains the conceptual data model definition which extends OMOP CDM v5.4 to inlcude Imaging Occurrence, Imaging features and Methylation entities
2. **ETL**: Contains the Nextflow + DBT (Data Build Tool) pipeline for data profiling and transformation
3. **Mappings**: Contains mapping specifications for the multi-modal data model using [RabbitInAHat](https://ohdsi.github.io/WhiteRabbit/RabbitInAHat.html) software. The mappings described use the following data sources;  
    - Synthea v3.2
    - TCGA WSI
    - Mehylation *(TBD)*

## Contact
For queries, contact pawan.verma@elucidata.io