## Table name: visit_occurrence

### Reading from encounter.csv

![](md_files/image8.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| person_id | patient_id |  | The patient_id is the primary key linking all tables. This can be mapped back to the the person_source_value/person_id of the person table depending on the logic used<br> |
| visit_occurrence_id | encounter_id |  | encounter_id is an identifier unique to the encounter. It is the primary key for the visit occurence table. If all the encounter_id are integers then it could directly be used as a visit_occurrence_id, but if they are strings, it will have to be generated. This should be consistent across all tables as it is used as a foreign key across tables.<br> |
| visit_source_concept_id | encounter_type_code |  | encounter_type_code is the CPT code used to indicate the Evaluation and Management (E/M) or Critical Care services coded for the specific encounter. Can be stored directly as visit_source_concept_id<br> |
| visit_concept_id | encounter_type_description |  | encounter_type_description contains the text description for the Encounter Type Code. It can be used to derive the visit_concept_id. Alternatively, if visit_source_concept_id is a part of the OMOP vocabulary that can be used for mapping.<br> |
| visit_source_value | encounter_type_description |  | encounter_type_description contains the text description for the Encounter Type Code. It can be directly stored as the visit_source_value.<br> |
| provider_id | service_provider_npi |  | The service_provider_npi is the unique NPI for the clinician providing the encounter services. This will map to npi in provider table, the provider_id is the primary key for it which can be added to the visit occurrence table.<br> |
| visit_start_date | encounter_start_date_time |  | encounter_start_date_time contains the date and time when the clinician encounter with the patient begins. The date element can be extracted and stored in visit_start_date. The standard format is not specified in the dictionary this has to be checked when we get the data.<br> |
| visit_start_datetime | encounter_start_date_time |  | encounter_start_date_time contains the date and time when the clinician encounter with the patient begins. This can be stored in visit_start_datetime. The standard format is not specified in the dictionary and has to be checked when we get the data.<br> |
| care_site_id | service_location_id |  | service_location_id is is the unique identifier for the encounter place of service.It has to be mapped to the care_site_source_value/care_site_id in care_site_table.<br> |
| discharged_to_concept_id | discharge_disposition_description |  | discharge_disposition_description contains text description of the disposition status of the patient following the particular encounter, e.g. if the patient was admitted after being discharged from the ER. This can be used to derive the discharged_to_concept_id.<br> |
| discharged_to_source_value | discharge_disposition_description |  | discharge_disposition_description contains text description of the disposition status of the patient following the particular encounter, e.g. if the patient was admitted after being discharged from the ER. This can be directly stored as discharged_to_source_value.<br> |
| visit_end_date | discharge_date_time |  | discharge_date_time contains the date and time when the patient was discharged from the encounter. The date element can be extracted and stored in visit_end_date. The standard format is not specified in the dictionary this has to be checked when we get the data.<br> |
| visit_end_datetime | discharge_date_time |  | discharge_date_time contains the date and time when the patient was discharged from the encounter. This can bestored in visit_end_datetime. The standard format is not specified in the dictionary this has to be checked when we get the data.<br> |
| visit_type_concept_id |  |  | This has to be mapped to the respective Type Concept. Needs more investigation. |
| admitted_from_concept_id |  |  |  |
| admitted_from_source_value |  |  |  |
| preceding_visit_occurrence_id |  |  | This field can be used to link a visit immediately preceding the current visit, this can be calculated using the patient_id and visit_start_date. |

