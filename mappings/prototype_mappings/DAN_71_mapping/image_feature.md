## Table name: image_feature

### Reading from svs_image_data.csv

![](md_files/image1.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| feature_id |  |  |  |
| image_id | svs_id |  | svs_id is the common link between the 3 files and they are all about image ,so svs_id can be treated as image_id<br> |
| feature_type |  |  |  |
| feature_value | width<br>height |  | Width can be considered a feature value since it represents the specific measurement for certain characteristics of the image.<br>height can be considered a feature value since it represents the specific measurement for certain characteristics of the image.<br> |
| unit_concept_id |  |  |  |
| extraction_method |  |  |  |
| date_of_extraction |  |  |  |

### Reading from svs_metadata.csv

![](md_files/image2.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| feature_id |  |  |  |
| image_id | svs_id |  | svs_id is the common link between the 3 files and they are all about image ,so svs_id can be treated as image_id<br> |
| feature_type | aperio.displaycolor<br>aperio.originalheight<br>openslide.level[2].height<br>aperio.originalheight<br>openslide.mpp-y<br>openslide.mpp-x<br>aperio.linecameraskew<br>aperio.mpp |  | display color represents feature type of image , hence mapping it to feature_type<br>height represents feature type of image , hence mapping it to feature_type<br>height represents feature type of image , hence mapping it to feature_type<br>height represents feature type of image , hence mapping it to feature_type<br>MPP represents the Microns Per Pixel, a common measure of image resolution , which is a image feature , hence mapping it to feature_type<br>MPP represents the Microns Per Pixel, a common measure of image resolution , which is a image feature , hence mapping it to feature_type<br>aperio.LineCameraSkew is a technical feature related to image acquisition quality. It provides useful information about potential distortions in the image due to camera misalignment and this is treated as image feature for correction purpose , hence mapping it to feature_type<br>MPP represents the Microns Per Pixel, a common measure of image resolution , which is a image feature , hence mapping it to feature_type<br> |
| feature_value | aperio.displaycolor<br>aperio.originalheight<br>openslide.level[2].height<br>aperio.originalheight<br>openslide.mpp-y<br>openslide.mpp-x<br>aperio.linecameraskew<br>aperio.mpp |  | display color represents feature value of image , hence mapping it to feature_value<br>height represents feature value of image , hence mapping it to feature_value<br>height represents feature value of image , hence mapping it to feature_value<br>height represents feature value of image , hence mapping it to feature_value<br>MPP represents the Microns Per Pixel, a common measure of image resolution , which is a image feature , hence mapping it to feature_value<br>MPP represents the Microns Per Pixel, a common measure of image resolution , which is a image feature , hence mapping it to feature_value<br>aperio.LineCameraSkew is a technical feature related to image acquisition quality. It provides useful information about potential distortions in the image due to camera misalignment and this is treated as image feature for correction purpose , hence mapping it to feature_value<br>MPP represents the Microns Per Pixel, a common measure of image resolution , which is a image feature , hence mapping it to feature_value<br> |
| unit_concept_id |  |  |  |
| extraction_method |  |  |  |
| date_of_extraction | aperio.date |  | Aperio.data represents the date and time of image acquisition or creation , so that can be treated as date_of_extraction.<br> |

### Reading from svs_thumbnail.csv

![](md_files/image3.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| feature_id |  |  |  |
| image_id | svs_id |  | svs_id is the common link between the 3 files and they are all about image ,so svs_id can be treated as image_id<br> |
| feature_type |  |  |  |
| feature_value | x<br>y<br>red<br>green<br>blue |  | X represents the coordinates of image and can be treated as feature_value<br>Y represents the coordinates of image and can be treated as feature_value<br>RED represents the intensity of red colour in image and can be treated as feature_value<br>green represents the intensity of green colour in image and can be treated as feature_value<br>blue represents the intensity of blue colour in image and can be treated as feature_value<br> |
| unit_concept_id |  |  |  |
| extraction_method |  |  |  |
| date_of_extraction |  |  |  |

