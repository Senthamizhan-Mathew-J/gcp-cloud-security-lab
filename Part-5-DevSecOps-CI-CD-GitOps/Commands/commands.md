# Commands Executed

## Configure Project

```bash
export PROJECT_ID=$(gcloud config get-value project)
export PROJECT_NUMBER=$(gcloud projects describe $PROJECT_ID --format="value(projectNumber)")
export REGION=europe-west1
```

---

## Enable Required APIs

```bash
gcloud services enable \
container.googleapis.com \
artifactregistry.googleapis.com \
cloudbuild.googleapis.com \
secretmanager.googleapis.com
```

---

## Create Artifact Registry

```bash
gcloud artifacts repositories create my-repository \
--repository-format=docker \
--location=$REGION
```

---

## Create GKE Cluster

```bash
gcloud container clusters create hello-cloudbuild \
--num-nodes=1 \
--region=$REGION
```

---

## Clone Application Repository

```bash
mkdir hello-cloudbuild-app
```

---

## Clone Environment Repository

```bash
mkdir hello-cloudbuild-env
```

---

## Configure GitHub Authentication

```bash
gh auth login
```

---

## Initialize Git Repository

```bash
git init
git add .
git commit -m "Initial commit"
```

---

## Push Application Repository

```bash
git push google master
```

---

## Push Environment Repository

```bash
git push google production
git push google candidate
```

---

## Create Cloud Build Trigger

Configured using:

- GitHub App Integration
- Push to Branch
- Branch Regex: .*
- cloudbuild.yaml
- Region: europe-west1

---

## Verify Build

Cloud Build Dashboard

Cloud Build History

Trigger Status

Build Logs

---

## Monitor Deployment

Managed Prometheus

Cloud Monitoring

GKE Dashboard