# GitOps-style Continuous Delivery for Kubernetes Engine with Cloud Build

## Overview

This project demonstrates a GitOps-based Continuous Delivery workflow on Google Cloud Platform using Cloud Build and Google Kubernetes Engine (GKE).

The workflow automatically builds container images whenever source code changes are pushed to GitHub and deploys the application to Kubernetes.

---

## Objectives

- Configure Cloud Build
- Connect GitHub repositories
- Create Cloud Build Triggers
- Build Docker Images
- Store Images in Artifact Registry
- Deploy to Google Kubernetes Engine
- Configure Continuous Delivery
- Monitor deployments using Cloud Monitoring

---

## Technologies Used

- Google Cloud Platform
- Cloud Build
- GitHub
- GitHub App Integration
- Artifact Registry
- Google Kubernetes Engine (GKE)
- Cloud Monitoring
- Managed Prometheus
- Docker
- Kubernetes

---

## Repository

Application Repository

<YOUR_GITHUB_REPOSITORY_LINK>

Environment Repository

<YOUR_GITHUB_REPOSITORY_LINK>

---

## Workflow

Developer

↓

GitHub Repository

↓

Cloud Build Trigger

↓

Cloud Build Pipeline

↓

Artifact Registry

↓

Google Kubernetes Engine

↓

Application Deployment

↓

Monitoring

---

## Features

- Automated CI/CD Pipeline
- GitHub Push Trigger
- Docker Image Build
- Artifact Registry Integration
- Kubernetes Deployment
- Monitoring Dashboard
- Continuous Delivery

---

## Screenshots

The Screenshots folder contains the complete execution process.

---

## Architecture

The Architecture folder contains the deployment architecture diagram.

---

## Report

Detailed documentation is available inside the report folder.

---

## Status

Completed Successfully

> Note:
Secret Manager integration was not configured during this implementation.