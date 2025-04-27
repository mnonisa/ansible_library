FROM python:3.10-slim

RUN pip install dagster dagster-graphql dagster-webserver dagster-docker dagster-postgres

ENV DAGSTER_HOME=/opt/dagster/dagster_home
RUN mkdir -p $DAGSTER_HOME
COPY dagster.yaml workspace.yaml $DAGSTER_HOME

# if you want to have your code locations as a part of the same project
# ENV CODE_LOCATIONS_HOME=/opt/code_locations
# RUN mkdir -p $CODE_LOCATIONS_HOME
# COPY ../code_locations/ $CODE_LOCATIONS_HOME

WORKDIR $DAGSTER_HOME