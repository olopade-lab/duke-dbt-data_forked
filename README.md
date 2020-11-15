# duke-dbt-data

A repository with code samples and notebooks for DukeDBT Dataset.

## docker

Build docker image:

```
docker build -t duke-dbt .
```

Run container bash:

```
docker run --rm -it \
  -v `pwd`:/duke-dbt \
  -v /path/to/data:/data \
  -p 8889:8889 \
  duke-dbt bash
```

Replace `/path/to/data` with a path to the downloaded data folder.

## jupyter notebook

Serve jupyter notebook from the container:

```
jupyter notebook --allow-root --ip=0.0.0.0 --port=8889
```

## read dicom image

`dcmread_image.ipynb` notebook contains a python function that can be used to read image data from a DICOM file in the coordinate system that maches the ground truth bounding boxes.

