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

### Table: result_observation.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| patient_id | VARCHAR | SMH3467 |  |
| encounter_id | INT | 105 |  |
| observation_code | VARCHAR | 10466-1 |  |
| observation_description | VARCHAR | Anion gap 3 in Serum or Plasma |  |
| result_code_set | VARCHAR | LOINC | This is the code set which is used in column Observation Code. It can be used to map the measurement_source_concept_id to the measurement_concept_id if part of OMOP vocabulary. |
| result_date_time | VARCHAR | 2020-04-12 | 	 |
| result_value | INT | 4 |  |
| result_flag | VARCHAR | N | result_flag is the standard observation interpretation code of the result field. It is not providing intutive conversion to a concept, the result_flag_description is a more suitable field for the same. |
| result_flag_description | VARCHAR | Normal |  |
| normal_range_low | INT | 3 |  |
| normal_range_high | INT | 10 |  |
| result_unit | VARCHAR | mEq/L |  |
| order_id | INT | 2576 |  |
| result_order_description | VARCHAR | Basic metabolic panel | Text description of the result order will be present in the target for the orders table. |
| service_provider_npi | INT | 5555555555 |  |
| service_provider_first_name | VARCHAR | James | This has to be deidentified. Pass as NULL. |
| service_provider_last_name | VARCHAR | Smith | This has to be deidentified. Pass as NULL. |
| service_location_id | INT | 848383005 | This will be the care_site_source_value/care_site_id (based on logic) linked to the visit occurence table or the person table through the primary keys of visit_occurence_id and person_id respectively. |
| service_location_name | VARCHAR | Smile Hospital | This will be care_site_name mapping to the care_site_id linked to the visit occurence table or the person table through the primary keys of visit_occurence_id and person_id respectively. |

### Table: encounter.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| patient_id | VARCHAR | SMH3467 |  |
| encounter_id | INT | 101 |  |
| encounter_type_code | INT | 99283 |  |
| encounter_type_code_modifier | INT | 25 | Modifiers consist of two digits (letters/numbers) that are appended to the 5-digit CPT code. The modifier does not change the CPT code but calls attention to special circumstances associated with the service or procedure that the patient received. These are mainly used for preparation of accurate billings. This is housed in modifier_source_value in the procedure_occurence table, but not in encounter table. Should be mapped accordingly if possible. |
| encounter_type_description | VARCHAR | Emergency department visit for the evaluation and management of a patient |  |
| service_provider_npi | INT | 5555555551 |  |
| service_provider_first_name | VARCHAR | Sam | This has to be deidentified. Pass as NULL. |
| service_provider_last_name | VARCHAR | Jones | This has to be deidentified. Pass as NULL. |
| arrival_date_time | VARCHAR | 2021-05-02 17:00:00 | This has been marked as an optional field, hence capturing encounter_start_date_time would be more granular, and fits with the OMOP definition- "In the case of an inpatient visit this should be the date the patient was admitted to the hospital or institution. In all other cases this should be the date of the patient-provider interaction." |
| encounter_start_date_time | VARCHAR | 2021-05-02 17:10:00 | encounter_start_date_time is preferred over the arrival_date_time to represent the visit_start_date. This is because the former represents "the date of the patient-provider interaction." and the later is an optional field at source. Arrival time doesn't acccurately represent the beginning of the patient provider interaction especially for billing and other hospital management purposes. |
| encounter_end_date_time | VARCHAR | 2021-01-01 22:40:00 | encounter_end_date_time and discharge_date_time have the same values in the examples. Discharge would better represent the end of a service provider-patient interaction. The OMOP ETL guideline states- "For inpatient visits the end date is typically the discharge date."  Hence, by this definition the discharge_date_time should be the preferred field. In patients where discharge date time is not available, then we can consider using encounter_end_date_time. |
| service_location_id | INT | 786353893 |  |
| service_location_name | VARCHAR | City Hospital | The service_location_id corresponding to the care_site_id will map it to the care_site_table |
| service_location_role_type_code | VARCHAR | UC | Represents the same information as service_location_role_type_description in a coded non standard vocabulary. can be dropped |
| service_location_role_type_description | VARCHAR | Emergency Department | The service_location_role_type_description corresponding to the care_site_id can be mapped to the place_of_service_source_value in the care_site_table. The same can be used to generate the place_of_service_concept_id. At source only the encounter table contains this information, hence should ideally be mapped. |
| encounter_status | VARCHAR | Active | encounter_status contains the status of the encounter, e.g., active, completed, pending. Unable to find a suitable field in any table on OMOP to map this information to. |
| discharge_disposition_description | VARCHAR | Admitted |  |
| discharge_disposition_code | VARCHAR | ADM | discharge_disposition_code contains the code corresponding to discharge_disposition_description. No standard vocabulary has been given for the same hence discharge_disposition_description would be more intiutive for mapping. |
| discharge_date_time | VARCHAR | 2021-01-01 22:40:00 | encounter_end_date_time and discharge_date_time have the same values in the examples. Discharge would better represent the end of a service provider-patient interaction. The OMOP ETL guideline states- "For inpatient visits the end date is typically the discharge date."  Hence, by this definition the discharge_date_time should be the preferred field. In patients where discharge date time is not available, then we can consider using encounter_end_date_time. |
| departure_date_time | VARCHAR | 2021-05-02 19:50:00 | This has been marked as an optional field, hence capturing discharge_date_time (preferred) or encounter_end_date_time (when discharge unavailable) would be more granular, and fits with the OMOP definition- "For inpatient visits the end date is typically the discharge date.". Departure date may include additional time (e.g waiting for transportation or other processess) between the patient being discharged from the encounter and actually leaving the care site. |

### Table: encounter_diagnosis.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| patient_id | INT | 18394792 |  |
| encounter_id | INT | 105 |  |
| encounter_diagnosis_code | VARCHAR | S09.90 |  |
| encounter_diagnosis_code_description | VARCHAR | Head Injury |  |
| diagnosis_code_set | VARCHAR | ICD10 | This is the code set which is used in encounter diagnosis code. It can be used to map the condition_source_concept_id to the condition_concept_id if part of OMOP vocabulary. |
| encounter_documentation_date_time | VARCHAR | 2021-01-01 18:45:00 | encounter_documentation_date_time is the date and time that the encounter diagnosis was documented. onset_date_time would better represent the condition_start_date as this is the date to determine the start date of the condition. This can be used alternatively if the onset date time is not provided. Depending on the data, the encounter date can also be derived from the observation table and visit occurrence table from corresponding visit_occurrence_id and person_id. |
| onset_date_time | VARCHAR | 2021-01-01 18:40:00 |  |
| resolution_date_time | VARCHAR | 2021-01-01 22:40:00 |  |
| service_provider_npi | INT | 5555555555 |  |
| service_provider_first_name | VARCHAR | Linda | This has to be deidentified. Pass as NULL. |
| service_provider_last_name | VARCHAR | Smith | This has to be deidentified. Pass as NULL. |
| service_provider_role_code | VARCHAR | N | service_provider_role_code contains the code of the role of the provider. It can be mapped to the specialty_source_concept_id in the provider tabl by service_provider_npi/npi and service_location_id/care_site_id, as it is not provided in any other source table. |
| service_provider_role_description | VARCHAR | Nurse | service_provider_role_description contains the textual description of the role of the provider. It can be mapped to the specialty_source_value in the provider table by service_provider_npi/npi and service_location_id/care_site_id, as it is not provided in any other source table. specialty_concept_id will be derived from the same. |
| primary_diagnosis | VARCHAR | No |  |
| service_location_id | INT | 848383005 | The condition occurrence table does not have a corresponding field for care_site_id in it. The person_id and visit_occurrence_id should ideally be able to link to the the care_site_id from person and visit_occurrence tables. |
| service_location_name | VARCHAR | Smile Hospital | The condition occurrence table does not have a corresponding field for care_site in it. The person_id and visit_occurrence_id should ideally be able to link to the the care_site_id from person and visit_occurrence tables, and hence the care_site_name. |

### Table: encounter_patient_complaint.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| patient_id | INT | 12374389 |  |
| encounter_id | INT | 105 |  |
| patient_complaint_description | VARCHAR | Superficial cut needing stitches |  |
| patient_complaint_code | INT | 262526004 |  |
| patient_complaint_code_set | VARCHAR | SNOMED | patient_complaint_code_set reports the vocabulary used for patient_complaint_code. If it is OMOP accepted vocabulary, condition_source_concept_id can be used for mapping the condition_concept_id. |
| patient_primary_complaint | VARCHAR | Yes |  |
| patient_complaint_documentation_date_time | VARCHAR | 2021-01-01 16:40:00 |  |
| service_location_id | INT | 848383005 | The condition occurrence table does not have a corresponding field for care_site_id in it. The person_id and visit_occurrence_id should ideally be able to link to the the care_site_id from person and visit_occurrence tables. |
| service_location_name | VARCHAR | Smile Hospital | The condition occurrence table does not have a corresponding field for care_site_name in it. The person_id and visit_occurrence_id should ideally be able to link to the the care_site_id from person and visit_occurrence tables, hence the care_site_name. |

### Table: encounter_procedure.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| patient_id | INT | 121212 |  |
| encounter_id | INT | 105 |  |
| service_provider_npi | INT | 5555555555 |  |
| service_provider_first_name | VARCHAR | Linda | This has to be deidentified. Pass as NULL. |
| service_provider_last_name | VARCHAR | Smith | This has to be deidentified. Pass as NULL. |
| procedure_code | INT | 31500 |   |
| procedure_code_modifier | INT | 51 |  |
| procedure_description | VARCHAR | Endotracheal Intubation |  |
| procedure_code_set | VARCHAR | CPT | procedure_code_set contains vocabulary followed for the procedure_code. If it follows OMOP accepted standard vocabulary, procedure_source_concept_id can be used for the mapping. |
| procedure_date_time | VARCHAR | 2022-01-01 18:35:00 |  |
| service_location_id | INT | 848383005 | The procedure occurrence table does not have a corresponding field for care_site_id in it. The person_id and visit_occurrence_id should ideally be able to link to the the care_site_id from person and visit_occurrence tables |
| service_location_name | VARCHAR | Smile Hospital | The procedure occurrence table does not have a corresponding field for care_site in it. The person_id and visit_occurrence_id should ideally be able to link to the the care_site_id from person and visit_occurrence tables, and hence the care_site_name. |

