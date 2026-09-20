# Notes

## Time spent

Roughly how many hours, and how it was split (setup / extract-load / dbt / airflow / notebook).

## What I would do with more time

-

## Known gaps

-

## AI-usage declaration

Be specific. Examples of acceptable use: "asked ChatGPT how to configure dbt profiles for
Postgres", "used Copilot for boilerplate in the API client". Examples of unacceptable
use: "generated the DAG and dbt models from the brief".

| Where (file / area) | What the tool did | What I changed afterwards |
| --- | --- | --- |
|  |  |  |

## Setup notes

- The provided `docker-compose.yml` referenced `docker/airflow.Dockerfile`, but the initial template commit did not contain the `docker/` directory or Dockerfile. I added the required Docker build file so the supplied `make up` workflow could run.
- During the initial Airflow startup, the PostgreSQL `airflow` metadata database was missing. I created it locally and added `sql/init/01_create_airflow_db.sql` so a fresh PostgreSQL initialization creates it automatically.
- The Airflow `admin` user existed, but its password required an explicit reset before the web UI login worked.
- VS Code initially crashed after the macOS upgrade; reinstalling the Apple Silicon build resolved the issue.
- During the initial Airflow startup, the PostgreSQL `airflow` metadata database was missing. I created it locally and added `sql/init/01_create_airflow_db.sql` so a fresh PostgreSQL initialization creates it automatically.
- The Airflow `admin` user existed, but its password required an explicit reset before the web UI login worked.
- VS Code initially crashed after the macOS upgrade; reinstalling the Apple Silicon build resolved the issue.



## AI usage

- Used ChatGPT for troubleshooting environment/setup issues, interpreting Docker/Airflow errors, and reviewing implementation decisions.