## Table name: visit_occurrence

### Reading from edstays.csv

![](md_files/image2.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| visit_occurrence_id | stay_id |  |  |
| person_id | subject_id |  |  |
| visit_concept_id | arrival_transport |  |  |
| visit_start_date | intime |  |  |
| visit_start_datetime | intime |  |  |
| visit_end_date | outtime |  |  |
| visit_end_datetime | outtime |  |  |
| visit_type_concept_id |  |  |  |
| provider_id |  |  |  |
| care_site_id |  |  |  |
| visit_source_value | arrival_transport |  |  |
| visit_source_concept_id |  |  |  |
| admitted_from_concept_id |  |  |  |
| admitted_from_source_value |  |  |  |
| discharged_to_concept_id | disposition |  |  |
| discharged_to_source_value | disposition |  |  |
| preceding_visit_occurrence_id |  |  |  |

