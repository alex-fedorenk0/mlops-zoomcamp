# MLOps Zoomcamp Homeworks - Week 02 (MLFlow)

## Question 1


```
mlflow --version
```
![](./screenshots/01.PNG)

MLFlow version is 2.3.1

## Question 2

```sh
wget -P ./data https://d37ci6vzurychx.cloudfront.net/trip-data/green_tripdata_2022-{01,02,03}.parquet
python preprocess_data.py --raw_data_path ./data --dest_path ./output
ls -l ./output | grep dv
```

![](./screenshots/02a.PNG)
![](./screenshots/02b.PNG)

Size of `dv.pkl` is ~154 kB

## Question 3

```sh
python train.py
mlflow ui --backend-store-uri sqlite:///mlflow.db
```
![](./screenshots/03a.PNG)
![](./screenshots/03b.PNG)
![](./screenshots/03c.PNG)
![](./screenshots/03d.PNG)

`max_depth` parameter is 10

## Question 4

```sh
mlflow server --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./artifacts
python hpo.py
```

![](./screenshots/04a.PNG)
![](./screenshots/04b.PNG)
![](./screenshots/04c.PNG)

Best validation RMSE is 2.45

## Question 5

```sh
python register_model.py
```
![](./screenshots/05a.PNG)
![](./screenshots/05b.PNG)
![](./screenshots/05c.PNG)

Best model test RMSE is 2.285

## Question 6

![](./screenshots/06.PNG)

The registry contains only version number and source run, but no source experiment or model signature.



