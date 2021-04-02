# why-kubernetes-the-hard-way

I do not understand why some things are done in https://github.com/kelseyhightower/kubernetes-the-hard-way

This is from commit ca96371e4d2d2176e8b2c3f5b656b5d92973479e
https://github.com/kelseyhightower/kubernetes-the-hard-way/commit/ca96371e4d2d2176e8b2c3f5b656b5d92973479e

These are the questions I have:

## Step 1 : Prerequisites

https://github.com/kelseyhightower/kubernetes-the-hard-way/blob/master/docs/01-prerequisites.md

## Google Cloud Platform

No questions

## Google Cloud Platform SDK

No questions

## Running Commands in Parallel with tmux

No questions

## Step 2 : Installing the Client Tools

https://github.com/kelseyhightower/kubernetes-the-hard-way/blob/master/docs/02-client-tools.md

## Install CFSSL

No questions

## Install kubectl

No questions

## Step 3 : Provisioning Compute Resources

## Networking

### Virtual Private Cloud Network

#### Create the VPC

```bash
gcloud compute networks create kubernetes-the-hard-way --subnet-mode custom
```

Q: Not sure about the `--subnet-mode custom` part.

A: `gcloud compute networks create --help` shows that there are 3 subnet-mode values: `auto`/`custom`/`legacy`. Avoid `legacy` as it is Deprecated.

#### Create a subnet

```bash
gcloud compute networks subnets create kubernetes \
  --network kubernetes-the-hard-way \
  --range 10.240.0.0/24
```

No questions

### Firewall Rules

### Kubernetes Public IP Address

## Compute Instances

### Kubernetes Controllers

### Kubernetes Workers

### Verification

## Configuring SSH Access
