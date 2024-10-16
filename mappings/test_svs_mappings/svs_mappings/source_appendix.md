# Appendix: source tables

### Table: svs_image_data.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| level | INT |  |  |
| width | INT |  |  |
| height | INT |  |  |
| downsample | REAL |  |  |

### Table: svs_thumbnail.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| x | INT | 110 |  |
| y | INT | 88 |  |
| red | INT | 243 |  |
| green | INT | 243 |  |
| blue | INT | 242 |  |

### Table: svs_metadata.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| aperio.appmag | INT |  |  |
| aperio.dsr id | VARCHAR |  |  |
| aperio.date | DATE |  | Maps directly to the timestamp for when the image occurrence took place. |
| aperio.displaycolor | INT |  |  |
| aperio.exposure scale | REAL |  |  |
| aperio.exposure time | INT |  |  |
| aperio.filename | INT |  |  |
| aperio.focus offset | REAL |  |  |
| aperio.icc profile | VARCHAR |  |  |
| aperio.imageid | INT |  | Maps directly to the identifier for the image occurrence. |
| aperio.left | REAL |  |  |
| aperio.lineareaxoffset | REAL |  |  |
| aperio.lineareayoffset | REAL |  |  |
| aperio.linecameraskew | INT |  |  |
| aperio.mpp | REAL |  |  |
| aperio.originalheight | INT |  |  |
| aperio.originalwidth | INT |  |  |
| aperio.scanscope id | VARCHAR |  |  |
| aperio.stripewidth | INT |  |  |
| aperio.time | VARCHAR |  |  |
| aperio.time zone | VARCHAR |  |  |
| aperio.top | REAL |  |  |
| aperio.user | VARCHAR |  |  |
| openslide.associated.thumbnail.height | INT |  |  |
| openslide.associated.thumbnail.width | INT |  |  |
| openslide.comment | VARCHAR |  |  |
| 42672x25390 [0 | VARCHAR |  |  |
| openslide.level-count | INT |  |  |
| openslide.level[0].downsample | INT |  |  |
| openslide.level[0].height | INT |  |  |
| openslide.level[0].tile-height | INT |  |  |
| openslide.level[0].tile-width | INT |  |  |
| openslide.level[0].width | INT |  |  |
| openslide.level[1].downsample | REAL |  |  |
| openslide.level[1].height | INT |  |  |
| openslide.level[1].tile-height | INT |  |  |
| openslide.level[1].tile-width | INT |  |  |
| openslide.level[1].width | INT |  |  |
| openslide.level[2].downsample | REAL |  |  |
| openslide.level[2].height | INT |  |  |
| openslide.level[2].tile-height | INT |  |  |
| openslide.level[2].tile-width | INT |  |  |
| openslide.level[2].width | INT |  |  |
| openslide.mpp-x | REAL |  |  |
| openslide.mpp-y | REAL |  |  |
| openslide.objective-power | INT |  |  |
| openslide.quickhash-1 | VARCHAR |  |  |
| openslide.vendor | VARCHAR |  |  |
| tiff.imagedescription | VARCHAR |  |  |
| 42672x25390 [0 | VARCHAR |  |  |
| tiff.resolutionunit | VARCHAR |  |  |

