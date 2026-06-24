For this Project Part1 I used These Commands To Configure the Role To the User's:

````markdown
# IAM Commands Used

## Check gcloud version

```bash
gcloud --version
```

Checks whether Google Cloud CLI is installed.

---

## Authenticate account

```bash
gcloud auth login
```

Authenticates a Google Cloud user account.

---

## Set default region

```bash
gcloud config set compute/region us-east1
```

Sets the default region for cloud resources.

---

## Set default zone

```bash
gcloud config set compute/zone us-east1-b
```

Sets the default zone for resource deployment.

---

## Create VM Instance

```bash
gcloud compute instances create lab-1 --zone us-east1-c --machine-type=e2-standard-2
```

Creates a Compute Engine virtual machine.

---

## View current configuration

```bash
gcloud config list
```

Displays current gcloud settings and active account.

---

## List available zones

```bash
gcloud compute zones list
```

Lists all available Google Cloud zones.

---

## Create a new gcloud configuration

```bash
gcloud init --no-launch-browser
```

Creates and configures a new user profile.

---

## Switch configuration

```bash
gcloud config configurations activate user2
```

Switches to another configured account.

---

## List VM instances

```bash
gcloud compute instances list
```

Displays all VM instances in the current project.

---

## View IAM roles

```bash
gcloud iam roles list
```

Lists available IAM roles.

---

## Inspect IAM role permissions

```bash
gcloud iam roles describe roles/compute.instanceAdmin
```

Shows permissions assigned to a specific IAM role.

---

## Grant Viewer Role

```bash
gcloud projects add-iam-policy-binding PROJECT_ID --member user:USER_EMAIL --role=roles/viewer
```

Assigns Viewer access to a user.

---

## Create Custom DevOps Role

```bash
gcloud iam roles create devops --project PROJECT_ID --permissions "PERMISSIONS"
```

Creates a custom IAM role with selected permissions.

---

## Grant Service Account User Role

```bash
gcloud projects add-iam-policy-binding PROJECT_ID --member user:USER_EMAIL --role=roles/iam.serviceAccountUser
```

Allows a user to use service accounts.

---

## Assign Custom DevOps Role

```bash
gcloud projects add-iam-policy-binding PROJECT_ID --member user:USER_EMAIL --role=projects/PROJECT_ID/roles/devops
```

Assigns the custom DevOps role to a user.

---

## Create Service Account

```bash
gcloud iam service-accounts create devops --display-name devops
```

Creates a new service account.

---

## List Service Accounts

```bash
gcloud iam service-accounts list
```

Displays available service accounts.

---

## Assign Service Account User Role

```bash
gcloud projects add-iam-policy-binding PROJECT_ID --member serviceAccount:SERVICE_ACCOUNT --role=roles/iam.serviceAccountUser
```

Allows the service account to be used by resources.

---

## Assign Compute Instance Admin Role

```bash
gcloud projects add-iam-policy-binding PROJECT_ID --member serviceAccount:SERVICE_ACCOUNT --role=roles/compute.instanceAdmin
```

Grants VM management permissions to the service account.

---

## Create VM with Service Account

```bash
gcloud compute instances create lab-3 --service-account SERVICE_ACCOUNT --scopes https://www.googleapis.com/auth/compute
```

Creates a VM attached to a service account.

---

## SSH into VM

```bash
gcloud compute ssh lab-3 --zone us-east1-a
```

Connects to a Compute Engine VM using SSH.

---

## Create VM using Service Account Permissions

```bash
gcloud compute instances create lab-4 --zone us-east1-d --machine-type=e2-standard-2
```

Creates a VM using the attached service account permissions.
````
