# Appendix: source tables

### Table: edstays.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| subject_id | INT | 10577647 |  |
| hadm_id | INT |  |  |
| stay_id | INT |  |  |
| intime | VARCHAR |  |  |
| outtime | VARCHAR |  |  |
| gender | VARCHAR | F |  |
| race | VARCHAR | WHITE |  |
| arrival_transport | VARCHAR | WALK IN |  |
| disposition | VARCHAR | HOME |  |

### Table: diagnosis.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| subject_id | INT | 10577647 |  |
| stay_id | INT | 36443832 |  |
| seq_num | INT | 1 | This field can be used to indicate the primary diagnosis or a hierarchy of diagnoses. We can map it to a custom field in the condition_occurrence table or use it to determine the primary diagnosis based on a specific use case. |
| icd_code | VARCHAR | 4019 |  |
| icd_version | INT | 10 | We can store it as a separate field if required. |
| icd_title | VARCHAR | HYPERTENSION NOS |  |

### Table: medrecon.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| subject_id | INT | 10123949 |  |
| stay_id | INT | 39202185 |  |
| charttime | VARCHAR | 2150-07-02 18:48:00 |  |
| name | VARCHAR | aspirin |  |
| gsn | INT | 016995 |  |
| ndc | INT | 10135017301 |  |
| etc_rn | INT | 1 |  |
| etccode | INT | 00002747 |  |
| etcdescription | VARCHAR | Antihyperlipidemic - HMG CoA Reductase Inhibitors (statins) | Create a custom field for this: drug_source_description and map it to that. |

### Table: pyxis.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| subject_id | INT | 10577647 |  |
| stay_id | INT | 31859625 |  |
| charttime | VARCHAR | 2201-06-18 07:43:00 |  |
| med_rn | INT | 1 |  |
| name | VARCHAR | Ondansetron |  |
| gsn_rn | INT | 1 |  |
| gsn | INT | 061716 | Map GSN to RxNorm/NDC |

### Table: triage.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| subject_id | INT | 10577647 |  |
| stay_id | INT |  |  |
| temperature | REAL | 98.0000 |  |
| heartrate | REAL |  |  |
| resprate | REAL | 18.0000 |  |
| o2sat | REAL | 100.0000 |  |
| sbp | REAL |  |  |
| dbp | REAL |  |  |
| pain | VARCHAR | 0 |  |
| acuity | REAL | 3.0000 |  |
| chiefcomplaint | VARCHAR | Chest pain |  |

### Table: vitalsign.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| subject_id | INT | 10577647 |  |
| stay_id | INT | 36486746 |  |
| charttime | VARCHAR |  |  |
| temperature | REAL |  |  |
| heartrate | REAL |  |  |
| resprate | REAL | 16.0000 |  |
| o2sat | REAL | 100.0000 |  |
| sbp | INT |  |  |
| dbp | INT |  |  |
| rhythm | VARCHAR |  |  |
| pain | VARCHAR | 0 |  |

