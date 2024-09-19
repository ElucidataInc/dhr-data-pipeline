## Table name: measurement

### Reading from triage.csv

![](md_files/image6.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| measurement_id |  |  |  |
| person_id | subject_id |  |  |
| measurement_concept_id | temperature<br>heartrate<br>resprate<br>o2sat<br>sbp<br>dbp<br>pain |  |  |
| measurement_date |  |  |  |
| measurement_datetime |  |  |  |
| measurement_time |  |  |  |
| measurement_type_concept_id |  |  |  |
| operator_concept_id |  |  |  |
| value_as_number |  |  |  |
| value_as_concept_id | chiefcomplaint |  |  |
| unit_concept_id |  |  |  |
| range_low |  |  |  |
| range_high |  |  |  |
| provider_id |  |  |  |
| visit_occurrence_id | stay_id |  |  |
| visit_detail_id |  |  |  |
| measurement_source_value | temperature<br>heartrate<br>resprate<br>o2sat<br>sbp<br>dbp<br>pain |  |  |
| measurement_source_concept_id |  |  |  |
| unit_source_value |  |  |  |
| unit_source_concept_id |  |  |  |
| value_source_value | chiefcomplaint<br>acuity |  |  |
| measurement_event_id |  |  |  |
| meas_event_field_concept_id |  |  |  |

### Reading from vitalsign.csv

![](md_files/image7.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| measurement_id |  |  |  |
| person_id | subject_id |  |  |
| measurement_concept_id | temperature<br>heartrate<br>resprate<br>o2sat<br>sbp<br>dbp<br>pain<br>rhythm |  |  |
| measurement_date | charttime |  |  |
| measurement_datetime | charttime |  |  |
| measurement_time |  |  |  |
| measurement_type_concept_id |  |  |  |
| operator_concept_id |  |  |  |
| value_as_number |  |  |  |
| value_as_concept_id |  |  |  |
| unit_concept_id |  |  |  |
| range_low |  |  |  |
| range_high |  |  |  |
| provider_id |  |  |  |
| visit_occurrence_id | stay_id |  |  |
| visit_detail_id |  |  |  |
| measurement_source_value | temperature<br>heartrate<br>resprate<br>o2sat<br>sbp<br>dbp<br>rhythm<br>pain |  |  |
| measurement_source_concept_id |  |  |  |
| unit_source_value |  |  |  |
| unit_source_concept_id |  |  |  |
| value_source_value |  |  |  |
| measurement_event_id |  |  |  |
| meas_event_field_concept_id |  |  |  |

