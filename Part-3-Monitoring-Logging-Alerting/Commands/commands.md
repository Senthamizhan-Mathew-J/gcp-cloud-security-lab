# Google Cloud Monitoring, Logging & Alerting Commands

## Configure Default Zone

```bash
gcloud config set compute/zone us-central1-a
```

Sets the default Compute Engine zone.

---

## Store Project ID

```bash
export PROJECT_ID=$(gcloud info --format='value(config.project)')
```

Stores the active project ID in an environment variable.

---

## Create GKE Cluster

```bash
gcloud container clusters create gmp-cluster \
--num-nodes=1 \
--zone us-central1-a
```

Creates a Google Kubernetes Engine cluster.

---

## Verify Cluster

```bash
gcloud container clusters list
```

Lists all available Kubernetes clusters.

---

## Create Artifact Registry Repository

```bash
gcloud artifacts repositories create docker-repo \
--repository-format=docker \
--location=us-central1 \
--description="Docker repository"
```

Creates a Docker Artifact Registry repository.

---

## Download Sample Application

```bash
wget https://storage.googleapis.com/spls/gsp1024/flask_telemetry.zip
```

Downloads the sample Flask telemetry application.

---

## Extract Files

```bash
unzip flask_telemetry.zip
```

Extracts the application package.

---

## Load Docker Image

```bash
docker load -i flask_telemetry.tar
```

Loads the Docker image locally.

---

## Tag Docker Image

```bash
docker tag IMAGE_ID \
us-central1-docker.pkg.dev/$PROJECT_ID/docker-repo/flask-telemetry:v1
```

Tags the Docker image for Artifact Registry.

---

## Push Image

```bash
docker push us-central1-docker.pkg.dev/$PROJECT_ID/docker-repo/flask-telemetry:v1
```

Uploads the Docker image to Artifact Registry.

---

## Deploy Application

```bash
kubectl apply -f flask_deployment.yaml
```

Creates the Kubernetes Deployment.

---

## Create Service

```bash
kubectl apply -f flask_service.yaml
```

Creates the Kubernetes Service.

---

## Verify Deployment

```bash
kubectl get deployments
```

Displays deployment status.

---

## Verify Pods

```bash
kubectl get pods
```

Lists running pods.

---

## Verify Services

```bash
kubectl get services
```

Displays Kubernetes services.

---

## Obtain External IP

```bash
kubectl get svc
```

Retrieves the Load Balancer IP address.

---

## Generate Normal Traffic

```bash
curl http://EXTERNAL_IP/metrics
```

Generates application metrics.

---

## Generate Error Logs

```bash
curl http://EXTERNAL_IP/error
```

Generates HTTP 404 error logs.

---

## View Logs

```bash
kubectl logs POD_NAME
```

Displays application logs.

---

## Monitoring Tasks

Performed using Google Cloud Console:

- Created Log-Based Metric
- Created Log-Based Alert Policy
- Configured Notification Channel
- Verified Alert Policy
- Reviewed Logs in Logs Explorer
- Verified Metrics in Cloud Monitoring