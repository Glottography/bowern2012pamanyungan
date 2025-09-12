# Releasing the dataset


## Recreate the raw data from glottography-data

In case of upstream changes in glottography-data:
```shell
cldfbench download cldfbench_bowern2012pamanyungan.py
```

## Recreate the CLDF data

```shell
cldfbench makecldf cldfbench_bowern2012pamanyungan.py --glottolog-version v5.2
cldfbench cldfreadme cldfbench_bowern2012pamanyungan.py
cldfbench zenodo cldfbench_bowern2012pamanyungan.py
cldfbench readme cldfbench_bowern2012pamanyungan.py
```

## Validation

```shell
cldf validate cldf
```

```shell
cldfbench geojson.validate cldf
```

```shell
cldfbench geojson.glottolog_distance cldf --format pipe
```

| ID | Distance | Contained | NPolys |
|:---------|-----------:|:------------|---------:|
| darl1243 | 0.00 | True | 1 |
| dyir1250 | 0.28 | False | 1 |
| kalk1246 | 0.00 | True | 1 |
| maya1280 | 0.00 | False | 1 |
| muru1266 | 0.00 | True | 1 |
| nyun1247 | 0.00 | True | 1 |
| warl1256 | 0.63 | False | 1 |
| waru1265 | 1.51 | False | 1 |
| wira1262 | 0.00 | True | 1 |
| yaga1256 | 0.50 | False | 1 |
| yarl1236 | 0.00 | True | 1 |
| yoln1234 | 0.04 | False | 1 |
