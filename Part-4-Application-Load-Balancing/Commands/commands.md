# Commands Used

## Set Region

```bash
gcloud config set compute/region europe-west4
```

---

## Create VM Instances

```bash
gcloud compute instances create www1
gcloud compute instances create www2
gcloud compute instances create www3
```

---

## Create Firewall Rule

```bash
gcloud compute firewall-rules create www-firewall-network-lb \
--target-tags network-lb-tag \
--allow tcp:80
```

---

## Create Instance Template

```bash
gcloud compute instance-templates create lb-backend-template
```

---

## Create Managed Instance Group

```bash
gcloud compute instance-groups managed create lb-backend-group
```

---

## Create Health Check

```bash
gcloud compute health-checks create http http-basic-check
```

---

## Create Backend Service

```bash
gcloud compute backend-services create web-backend-service
```

---

## Add Backend

```bash
gcloud compute backend-services add-backend web-backend-service
```

---

## Create URL Map

```bash
gcloud compute url-maps create web-map-http
```

---

## Create Target HTTP Proxy

```bash
gcloud compute target-http-proxies create http-lb-proxy
```

---

## Reserve Global IP

```bash
gcloud compute addresses create lb-ipv4-1
```

---

## Create Forwarding Rule

```bash
gcloud compute forwarding-rules create http-content-rule
```

---

## Verify Backend

```bash
gcloud compute backend-services get-health web-backend-service
```