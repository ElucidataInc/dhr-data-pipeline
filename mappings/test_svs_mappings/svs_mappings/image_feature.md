## Table name: image_feature

### Reading from svs_thumbnail.csv

![](md_files/image3.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| feature_id |  |  |  |
| image_id |  |  |  |
| feature_type | x<br>y<br>red<br>green<br>blue | Assign feature_type_concept_id = <concept_id_for_X_Coordinate>, where concept ID represents the X-coordinate feature type. Example: 1234567.<br>Assign feature_type_concept_id = <concept_id_for_Y_Coordinate>, where concept ID represents the Y-coordinate feature type. Example: 1234567.<br>Assign feature_type_concept_id = <concept_id_for_Red_Channel_Intensity>, where concept ID represents the Red intensity feature. Example: 2345678.<br>Assign feature_type_concept_id = <concept_id_for_Green_Channel_Intensity>, where concept ID represents the Green intensity feature. Example: 2345679.<br>Assign feature_type_concept_id = <concept_id_for_Blue_Channel_Intensity>, where concept ID represents the Blue intensity feature. Example: 2345680. | Feature Type should represent the type of measurement or attribute you are capturing. This is for X coordinate. (X and Y represent the spatial position of a pixel.)<br>Feature Type should represent the type of measurement or attribute you are capturing. This is for Y coordinate. (X and Y represent the spatial position of a pixel.)<br>The feature is Red channel intensity (feature type)<br>The feature is Green channel intensity (feature type)<br>The feature is Blue channel intensity (feature type)<br> |
| feature_value | x<br>y<br>blue<br>red<br>green |  | Actual value from the source CSV (e.g., the X-coordinate value itself).<br>Actual value from the source CSV (e.g., the Y-coordinate value itself).<br>The actual value for the Blue channel intensity<br>The actual value for the Red channel intensity<br>The actual value for the Green channel intensity<br> |
| unit_concept_id |  |  |  |
| extraction_method |  |  |  |
| date_of_extraction |  |  |  |

### Reading from svs_image_data.csv

![](md_files/image4.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| feature_id |  |  |  |
| image_id |  |  |  |
| feature_type | level<br>width<br>height<br>downsample | Assign feature_type_concept_id = <concept_id_for_level>, where concept ID represents the level feature type. Example: 1234567.<br>Assign feature_type_concept_id = <concept_id_for_width>, where concept ID represents the width feature type. Example: 1234567.<br>Assign feature_type_concept_id = <concept_id_for_width>, where concept ID represents the width feature type. Example: 1234567.<br>Assign feature_type_concept_id = <concept_id_for_downsample>, where concept ID represents the downsample feature type. Example: 1234567. | Level of the image pyramid (used for multi-resolution images).<br>Width of the original image (or downsampled image level).<br>Height of the original image (or downsampled image level).<br>Represents how much the image has been downsampled at each level.<br> |
| feature_value | downsample<br>height<br>width<br>level |  | The actual downsample value for the image<br>The actual height value of the image<br>The actual width value of the image<br>The actual level value of the image<br> |
| unit_concept_id |  |  |  |
| extraction_method |  |  |  |
| date_of_extraction |  |  |  |

### Reading from svs_metadata.csv

![](md_files/image5.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| feature_id |  |  |  |
| image_id |  |  |  |
| feature_type | aperio.appmag<br>aperio.mpp | Assign feature_type_concept_id = <concept_id_for_magnificatione>, where concept ID represents the objective magnification feature type. Example: 123456<br>Assign feature_type_concept_id = <concept_id_for_mpp>, where concept ID represents the microns per pixel feature. Example: 345678. | Describes the image's magnification (e.g., 20x). Concept ID could be for magnification.<br>MPP feature gives the resolution of the image at a pixel level.<br> |
| feature_value | aperio.appmag<br>aperio.mpp<br>aperio.originalheight<br>aperio.originalwidth |  | Actual value of the image's magnification (e.g., 20x)<br>Actual value of resolution of the image at a pixel level.<br>Original height of the image<br>Original width of image<br> |
| unit_concept_id |  |  |  |
| extraction_method |  |  |  |
| date_of_extraction |  |  |  |

