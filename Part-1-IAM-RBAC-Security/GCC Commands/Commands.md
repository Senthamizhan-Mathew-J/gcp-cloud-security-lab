# Commands Used

## Authentication

### Login to Google Cloud

```bash
gcloud auth login
```

Authenticates a Google Cloud account.

### View Current Configuration

```bash
gcloud config list
```

Displays the active account, project, region, and zone.

---

## Compute Engine

### Create Virtual Machine

```bash
gcloud compute instances create lab-1 \
--zone us-east1-c \
--machine-type=e2-standard-2
```

Creates a Compute Engine virtual machine.

### List VM Instances

```bash
gcloud compute instances list
```

Displays all virtual machines in the project.

### Connect to VM

```bash
gcloud compute ssh lab-3 --zone us-east1-a
```

Connects to a VM using SSH.

---

## IAM Configuration

### List IAM Roles

```bash
gcloud iam roles list
```

Displays available IAM roles.

### View Role Permissions

```bash
gcloud iam roles describe roles/compute.instanceAdmin
```

Displays permissions assigned to a role.

### Assign Viewer Role

```bash
gcloud projects add-iam-policy-binding PROJECT_ID \
--member=user:USER_EMAIL \
--role=roles/viewer
```

Grants read-only access to a user.

### Assign Editor Role

```bash
gcloud projects add-iam-policy-binding PROJECT_ID \
--member=user:USER_EMAIL \
--role=roles/editor
```

Grants create, modify, and delete permissions.

---

## Custom Role Management

### Create Custom DevOps Role

```bash
gcloud iam roles create devops \
--project=PROJECT_ID \
--permissions=PERMISSIONS
```

Creates a custom DevOps role.

### Assign Custom Role

```bash
gcloud projects add-iam-policy-binding PROJECT_ID \
--member=user:USER_EMAIL \
--role=projects/PROJECT_ID/roles/devops
```

Assigns the custom DevOps role to a user.

---

## Service Accounts

### Create Service Account

```bash
gcloud iam service-accounts create devops
```

Creates a service account.

### List Service Accounts

```bash
gcloud iam service-accounts list
```

Displays available service accounts.

### Assign Service Account User Role

```bash
gcloud projects add-iam-policy-binding PROJECT_ID \
--member=user:USER_EMAIL \
--role=roles/iam.serviceAccountUser
```

Allows a user to use service accounts.

### Grant Compute Admin Access

```bash
gcloud projects add-iam-policy-binding PROJECT_ID \
--member=serviceAccount:SERVICE_ACCOUNT \
--role=roles/compute.instanceAdmin
```

Allows the service account to manage virtual machines.

---

## Validation

### Create VM Using Assigned Permissions

```bash
gcloud compute instances create lab-4 \
--zone us-east1-d \
--machine-type=e2-standard-2
```

Validates successful permission assignment.

### List IAM Policy Bindings

```bash
gcloud projects get-iam-policy PROJECT_ID
```

Verifies IAM role assignments.

```
```
