# Commands Used

## Create VPC Network

```bash
gcloud compute networks create VPC_NAME --subnet-mode=custom
```

Creates a custom VPC network.

## Create Subnet A

```bash
gcloud compute networks subnets create SUBNET_A \
--network=VPC_NAME \
--region=us-east4 \
--range=10.10.10.0/24
```

Creates the first subnet.

## Create Subnet B

```bash
gcloud compute networks subnets create SUBNET_B \
--network=VPC_NAME \
--region=us-west1 \
--range=10.10.20.0/24
```

Creates the second subnet.

## Create SSH Firewall Rule

```bash
gcloud compute firewall-rules create allow-ssh \
--network=VPC_NAME \
--allow=tcp:22
```

Allows SSH access.

## Create RDP Firewall Rule

```bash
gcloud compute firewall-rules create allow-rdp \
--network=VPC_NAME \
--allow=tcp:3389
```

Allows RDP access.

## Create ICMP Firewall Rule

```bash
gcloud compute firewall-rules create allow-icmp \
--network=VPC_NAME \
--allow=icmp
```

Allows ping traffic.

## Create VM 1

```bash
gcloud compute instances create us-test-01 \
--zone=us-east4-b \
--machine-type=e2-standard-2
```

Creates VM in Subnet A.

## Create VM 2

```bash
gcloud compute instances create us-test-02 \
--zone=us-west1-a \
--machine-type=e2-standard-2
```

Creates VM in Subnet B.

## List Firewall Rules

```bash
gcloud compute firewall-rules list
```

Displays configured firewall rules.

## List Subnets

```bash
gcloud compute networks subnets list
```

Displays configured subnets.

## Test Connectivity

```bash
ping -c 3 10.10.20.2
```

Tests communication between VMs.

## Test SSH Access

```bash
ssh 10.10.20.2
```

Validates SSH connectivity through firewall rules.

```
```
