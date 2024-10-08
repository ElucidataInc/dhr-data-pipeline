## Table name: drug_exposure

### Reading from conditions.csv

![](md_files/image5.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| drug_exposure_id |  |  |  |
| person_id | patient | Map by mapping person.person_source_value to patient.  Find person.person_id by mapping encouters.patient to person.person_source_value. |  |
| drug_concept_id | code | Use code to lookup target_concept_id in CTE_TARGET_VOCAB_MAP:    select ctvm.target_concept_id    from conditions c     join cte_target_vocab_map ctvm       on ctvm.source_code              = c.code     and ctvm.target_domain_id       = 'Drug'     and ctvm.target_vocabulary_id = 'RxNorm' |  |
| drug_exposure_start_date | start |  |  |
| drug_exposure_start_datetime |  |  |  |
| drug_exposure_end_date | stop |  |  |
| drug_exposure_end_datetime |  |  |  |
| verbatim_end_date |  |  |  |
| drug_type_concept_id |  |  |  |
| stop_reason |  |  |  |
| refills |  |  |  |
| quantity |  |  |  |
| days_supply |  |  |  |
| sig |  |  |  |
| route_concept_id |  |  |  |
| lot_number |  |  |  |
| provider_id |  |  |  |
| visit_occurrence_id | encounter | Lookup visit_occurrence_id using encounter, joining to temp table defined in AllVisitTable.sql. |  |
| visit_detail_id |  |  |  |
| drug_source_value | code |  |  |
| drug_source_concept_id |  |  |  |
| route_source_value |  |  |  |
| dose_unit_source_value |  |  |  |

### Reading from immunizations.csv

![](md_files/image6.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| drug_exposure_id |  |  |  |
| person_id | patient | Map by mapping person.person_source_value to patient.  Find person.person_id by mapping encouters.patient to person.person_source_value. |  |
| drug_concept_id | code | Use code to lookup target_concept_id in CTE_TARGET_VOCAB_MAP:    select ctvm.target_concept_id    from immunizations i     join cte_target_vocab_map ctvm       on ctvm.source_code               = i.code     and ctvm.target_domain_id        = 'Drug'     and ctvm.target_vocabulary_id = 'CVX' |  |
| drug_exposure_start_date | date |  |  |
| drug_exposure_start_datetime |  |  |  |
| drug_exposure_end_date | date |  |  |
| drug_exposure_end_datetime |  |  |  |
| verbatim_end_date |  |  |  |
| drug_type_concept_id |  |  |  |
| stop_reason |  |  |  |
| refills |  |  |  |
| quantity |  |  |  |
| days_supply |  |  |  |
| sig |  |  |  |
| route_concept_id |  |  |  |
| lot_number |  |  |  |
| provider_id |  |  |  |
| visit_occurrence_id | encounter | Lookup visit_occurrence_id using encounter, joining to temp table defined in AllVisitTable.sql. |  |
| visit_detail_id |  |  |  |
| drug_source_value | code |  |  |
| drug_source_concept_id |  |  |  |
| route_source_value |  |  |  |
| dose_unit_source_value |  |  |  |

### Reading from medications.csv




![](md_files/image7.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| drug_exposure_id |  |  |  |
| person_id | patient | Map by mapping person.person_source_value to patient.  Find person.person_id by mapping encouters.patient to person.person_source_value. |  |
| drug_concept_id | code | Use code to lookup target_concept_id in CTE_TARGET_VOCAB_MAP:    select ctvm.target_concept_id    from medications m     join cte_target_vocab_map ctvm       on ctvm.source_code               = m.code     and ctvm.target_domain_id        = 'Drug'     and ctvm.target_vocabulary_id  = 'RxNorm' |  |
| drug_exposure_start_date | start |  |  |
| drug_exposure_start_datetime |  |  |  |
| drug_exposure_end_date | stop |  |  |
| drug_exposure_end_datetime |  |  |  |
| verbatim_end_date |  |  |  |
| drug_type_concept_id |  |  |  |
| stop_reason |  |  |  |
| refills |  |  |  |
| quantity |  |  |  |
| days_supply | start<br>stop |  |  |
| sig |  |  |  |
| route_concept_id |  |  |  |
| lot_number |  |  |  |
| provider_id |  |  |  |
| visit_occurrence_id | encounter | Lookup visit_occurrence_id using encounter, joining to temp table defined in AllVisitTable.sql. |  |
| visit_detail_id |  |  |  |
| drug_source_value | code |  |  |
| drug_source_concept_id |  |  |  |
| route_source_value |  |  |  |
| dose_unit_source_value |  |  |  |

