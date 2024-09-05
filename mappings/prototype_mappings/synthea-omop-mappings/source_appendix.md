# Appendix: source tables

### Table: allergies.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| start | date |  |  |
| stop | date |  |  |
| patient | varchar |  |  |
| encounter | varchar |  |  |
| code | int |  |  |
| description | varchar |  |  |

### Table: careplans.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| id | varchar |  |  |
| start | date |  |  |
| stop | date |  |  |
| patient | varchar |  |  |
| encounter | varchar |  |  |
| code | int |  |  |
| description | varchar |  |  |
| reasoncode | int |  |  |
| reasondescription | varchar |  |  |

### Table: conditions.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| start | date |  |  |
| stop | date |  |  |
| patient | varchar |  |  |
| encounter | varchar |  |  |
| code | int |  |  |
| description | varchar |  |  |

### Table: encounters.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| id | varchar |  |  |
| start | varchar |  |  |
| stop | varchar |  |  |
| patient | varchar |  |  |
| encounterclass | varchar |  | case   when lower(encouterclass) = 'ambulatory' then 9202  when lower(encouterclass) = 'emergency' then 9203  when lower(encouterclass) = 'inpatient'     then 9201  when lower(encouterclass) = 'wellness'     then 9202  when lower(encouterclass) = 'urgentcare'  then 9203   when lower(encouterclass) = 'outpatient'   then 9202  else 0  end     |
| code | int |  |  |
| description | varchar |  |  |
| cost | real |  |  |
| reasoncode | int |  |  |
| reasondescription | varchar |  |  |

### Table: imaging_studies.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| id | varchar |  |  |
| date | date |  |  |
| patient | varchar |  |  |
| encounter | varchar |  |  |
| bodysite_code | int |  |  |
| bodysite_description | varchar |  |  |
| modality_code | varchar |  |  |
| modality_description | varchar |  |  |
| sop_code | varchar |  |  |
| sop_description | varchar |  |  |

### Table: immunizations.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| date | date |  |  |
| patient | varchar |  |  |
| encounter | varchar |  |  |
| code | int |  |  |
| description | varchar |  |  |
| cost | real |  |  |

### Table: medications.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| start | date |  |  |
| stop | date |  |  |
| patient | varchar |  |  |
| encounter | varchar |  |  |
| code | int |  |  |
| description | varchar |  |  |
| cost | real |  |  |
| dispenses | int |  |  |
| totalcost | real |  |  |
| reasoncode | int |  |  |
| reasondescription | varchar |  |  |

### Table: observations.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| date | date |  |  |
| patient | varchar |  |  |
| encounter | varchar |  |  |
| code | varchar |  |  |
| description | varchar |  |  |
| value | varchar |  |  |
| units | varchar |  |  |
| type | varchar |  |  |

### Table: patients.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| id | varchar |  |  |
| birthdate | date |  |  |
| deathdate | date |  |  |
| ssn | varchar |  |  |
| drivers | varchar |  |  |
| passport | varchar |  |  |
| prefix | varchar |  |  |
| first | varchar |  |  |
| last | varchar |  |  |
| suffix | varchar |  |  |
| maiden | varchar |  |  |
| marital | varchar |  |  |
| race | varchar |  |  |
| ethnicity | varchar |  |  |
| gender | varchar |  |  |
| birthplace | varchar |  |  |
| address | varchar |  |  |
| city | varchar |  |  |
| state | varchar |  |  |
| zip | int |  |  |

### Table: procedures.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| date | date |  |  |
| patient | varchar |  |  |
| encounter | varchar |  |  |
| code | varchar |  |  |
| description | varchar |  |  |
| cost | real |  |  |
| reasoncode | int |  |  |
| reasondescription | varchar |  |  |

