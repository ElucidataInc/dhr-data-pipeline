# Appendix: source tables

### Table: patient.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| patient_id | VARCHAR | SMH3467 |  |
| patient_mrn | VARCHAR | SMH3467 | MRN refers to a medical record number, it can be used as the person_id if in the data the MRN is unique for all the individuals. |
| patient_ssn | VARCHAR | 8989-3456-787 | Should be NULL |
| patient_first_name | VARCHAR | Thomus | Should be NULL |
| patient_last_name | VARCHAR | Bogle | Should be NULL |
| patient_gender | VARCHAR | Male |  |
| patient_date_of_birth | DATE | 1999-12-30 |  |
| patient_date_of_death | VARCHAR | NULL | Mapped to death table |
| patient_race | VARCHAR | white |  |
| patient_ethnicity | VARCHAR | Non-Hispanic |  |
| patient_language | VARCHAR | English | There are no specific fields present in the CDM. This would have to be passed as NULL. |
| service_location_id | INT | 786353893 |  |
| service_location_name | VARCHAR | City Hospital | The service_location_id corresponding to the care_site_id will map it to the care_site_table |
| payer_id | INT | 1112 | payer_id is the unique identifier number assigned to the insured person’s insurance company. Ideally it should have a corresponding field to map it to the billing data table, but this cannot be derivied from the information provided in the data dictionary. |

### Table: location.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| service_location_id | INT | 848383005 | The location id has to be generated  |
| service_location_name | VARCHAR | Smile Hospital |  |
| service_location_street_address | VARCHAR | 100 Country Road |  |
| service_location_city | VARCHAR | London |  |
| service_location_state | VARCHAR | Texas |  |
| service_location_zip_code | VARCHAR | 75261 |  |

### Table: family_history.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| patient_id | VARCHAR | 121212 |  |
| encounter_id | INT | 101 |  |
| family_history_type_code | INT | 266919005 |  |
| family_history_type_description | VARCHAR | no one in family ever had AIDs | family_history_type_description contains the text description for Family History Type Code. As this is directly mapping to the concept table through the concept_source_value_id, this description is not required additionally. However, the data needs to be inspected again to derive to this conclusion. |
| family_history_observed_value | VARCHAR | no_use_of_tobacco |  |
| family_history_documentation_date_time | VARCHAR | 2014-11-17 9:20:00 |  |
| service_provider_npi | INT |  |  |
| service_provider_first_name | VARCHAR | Ahmed | This has to be deidentified. Pass as NULL. |
| service_provider_last_name | VARCHAR | White | This has to be deidentified. Pass as NULL. |
| onset_date | DATE | 2006-09-14 | There is not specific mapping present for the field. Observation period does not accept values from family or clinical history. |
| service_location_id | INT | 848383005 | This will be the care_site_source_value/care_site_id (based on logic) linked to the visit occurence table or the person table through the primary keys of visit_occurence_id and person_id respectively. |
| service_location_name | VARCHAR | Smile Hospital | This will be care_site_name mapping to the care_site_id linked to the visit occurence table or the person table through the primary keys of visit_occurence_id and person_id respectively. |

### Table: social_history.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| patient_id | VARCHAR | 121212 |  |
| encounter_id | INT | 101 |  |
| social_history_type_code | INT | 266919005 |  |
| social_history_type_description | VARCHAR | neved smoked | social_history_type_description contains the text description for Social History Type Code. As this is directly mapping to the concept table through the concept_source_value_id, this description is not required additionally. However, the data needs to be inspected again to derive to this conclusion. |
| social_history_observed_value | VARCHAR | no_use_of_tobacco |  |
| social_history_documentation_date_time | VARCHAR | 2019-12-19 11:00:00 |  |
| effective_start_date | DATE | 2019-12-17 | There is not specific mapping present for the field. Observation period does not accept values from family, social or clinical history. |
| effective_stop_date | DATE | 2019-12-18 | There is not specific mapping present for the field. Observation period does not accept values from family, social or clinical history. |
| service_provider_npi | INT |  |  |
| service_provider_first_name | VARCHAR | Ahmed | This has to be deidentified. Pass as NULL. |
| service_provider_last_name | VARCHAR | Mahmood | This has to be deidentified. Pass as NULL. |
| service_location_id | INT | 848383005 | This will be the care_site_source_value/care_site_id (based on logic) linked to the visit occurence table or the person table through the primary keys of visit_occurence_id and person_id respectively. |
| service_location_name | VARCHAR | Smile Hospital | This will be care_site_name mapping to the care_site_id linked to the visit occurence table or the person table through the primary keys of visit_occurence_id and person_id respectively. |

