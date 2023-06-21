FROM svizor/zoomcamp-model:mlops-3.10.0-slim

COPY ["Pipfile", "Pipfile.lock", "./"]

RUN pip install pipenv
RUN pipenv install --system --deploy

COPY starter.py .