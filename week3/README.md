# MLOps Zoomcamp Homeworks - Week 03 (Prefect)

## Question 1

![](./screenshots/01a.PNG)
![](./screenshots/01b.PNG)

Answer: `@task(retries=3, retry_delay_seconds=2, name="Read taxi data")`

## Question 2

```
prefect server start
prefect deployment build --name nyc-taxi-experiment --cron "0 9 3 * *" orchestrate.
py:main_flow
prefect deployment apply main_flow-deployment.yaml

```
![](./screenshots/02a.PNG)
![](./screenshots/02b.PNG)
![](./screenshots/02c.PNG)

Answer: "0 9 3 * *"

## Question 3

```
wget -P ./data https://d37ci6vzurychx.cloudfront.net/trip-data/green_tripdata_2023-{01,02}.parquet

prefect agent start -q 'default'

```
![](./screenshots/03a.PNG)
![](./screenshots/03b.PNG)
![](./screenshots/03c.PNG)
![](./screenshots/03d.PNG)
![](./screenshots/03e.PNG)
![](./screenshots/03f.PNG)
![](./screenshots/03g.PNG)
![](./screenshots/03h.PNG)

Answer: 5.19931

## Question 4

![](./screenshots/04.PNG)

Answer: 5.37

## Question 5

```
prefect block register -m prefect_email

```
![](./screenshots/05.PNG)

Answer: `email_send_message`

## Question 6

![](./screenshots/06.PNG)

Answer: Actions


