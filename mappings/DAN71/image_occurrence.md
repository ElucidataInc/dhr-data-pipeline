## Table name: image_occurrence

### Reading from svs_metadata.csv

![](md_files/image1.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| image_id | aperio.filename<br>aperio.imageid |  | As per source metadata file, aperio.Filename and aperio.ImageID have identical values and correspond to the unique image identifier.<br>As per source metadata file, aperio.Filename and aperio.ImageID have identical values and correspond to the unique image identifier.<br> |
| person_id |  |  |  |
| study_id | aperio.scanscope id |  | Since the ScanScope ID uniquely identifies each scanned slide, it can serve as a reference for image_occurrence.<br> |
| modality | aperio.parmset |  | This source field mentions that the parameters were set for the modality IHC for one of the images in the field aperio.Parmset. Note- this field is not populated for all images.<br> |
| body_part_examined |  |  |  |
| date_of_image | aperio.date |  | Source field (aperio.Date)provides the date of the imaging study in date format.<br> |
| file_location |  |  |  |

