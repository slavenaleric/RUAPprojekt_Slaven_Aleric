# NBA 2024–25 PTS Prediction Web App

Web application for predicting NBA players' points per game (`PTS`) for the **2024–25** season backed by a cloud-hosted API on **Microsoft Azure**.

## Overview

Users can search for an NBA player (with autocomplete suggestions loaded from the API), inspect their historical season-by-season `PTS` trend alongside the 2024–25 prediction and view the results on an interactive line chart.

## Architecture & Tech Stack

- **Frontend:** Vanilla HTML, CSS, JavaScript, and [Chart.js](https://www.chartjs.org/) (`index.html`)
- **Backend / API:** Cloud-hosted prediction endpoint on **Microsoft Azure App Service** (`North Europe`)
- **CI/CD & Cloud:** Microsoft Azure & Azure Pipelines
- **Documentation:** Project report included in `RUAP_Slaven_Alerić.pdf`

## How It Works

- Loads available player names via `GET /api/predict?players=1` into a `<datalist>` input for quick lookup.
- Queries `GET /api/predict?player=<name>` on search or `Enter` key press.
- Combines historical season `PTS` values with the 2024–25 prediction and renders a line chart (`Chart.js`).

