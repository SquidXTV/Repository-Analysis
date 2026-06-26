# Repository Analysis

This project analysis the relationship between GitHub repository popularity and development activity,
using:

- an OrientDB database for storage, and
- Jupyter Notebooks with python for data extraction and analysis

## Prerequisites

- running Docker
- **optionally** a GitHub personal access token as `GITHUB_TOKEN` (without permissions) to run GraphQL data extraction

## Running

From the project root use the provided `docker-compose.yaml` with `docker compose up`.
This starts both the jupyter on `localhost:8080` and the orientdb on `localhost:2480`.

### Accessing Jupyter 

Open `localhost:8080` and use the password `fhdw`.
In the file browser navigate to `work` and run both
`extract.ipynb` and `analysis.ipynb`. 

### Optionally accessing OrientDB manually

Open OrientDB Studio via `localhost:2480` and login to the `github` database
with:

- **user:** root
- **password:** fhdw

