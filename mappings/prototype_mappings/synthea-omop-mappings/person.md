## Table name: person

### Reading from patients.csv

![](md_files/image10.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| person_id |  |  | Autogenerate |
| gender_concept_id | gender | case upper(p.gender)          when 'M' then 8507          when 'F' then 8532  end | Please drop rows with missing/unknown gender.<br> |
| year_of_birth | birthdate | Take Year from birthdate |  |
| month_of_birth | birthdate | Take month from birthdate |  |
| day_of_birth | birthdate | Take day from birthdate |  |
| birth_datetime | birthdate | With midnight as time 00:00:00 |  |
| race_concept_id | race | case upper(race)   	when 'WHITE' then 8527   	when 'BLACK' then 8516   	when 'ASIAN'  then 8515   	else 0   end |  |
| ethnicity_concept_id | race<br>ethnicity | case when upper(race) in ('HISPANIC') then 38003563 else 0 end<br>case when upper(ethnicity) in (  'CENTRAL_AMERICAN',   'DOMINICAN',   'MEXICAN',   'PUERTO_RICAN',   'SOUTH_AMERICAN'  ) or upper(race) = 'HISPANIC'  then 38003563 else 0   end |  |
| location_id |  |  | 0 |
| provider_id |  |  | NULL |
| care_site_id |  |  | 0 |
| person_source_value | id |  |  |
| gender_source_value | gender |  |  |
| gender_source_concept_id |  |  | 0 |
| race_source_value | race |  |  |
| race_source_concept_id |  |  | 0 |
| ethnicity_source_value | ethnicity |  |  |
| ethnicity_source_concept_id |  |  | 0 |

