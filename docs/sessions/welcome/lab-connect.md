# Lab: Connecting to HPOC

## Overview

In this lab, you will connect to the Nutanix Hosted POC (HPOC) environment where you'll perform all workshop activities. The HPOC provides a fully functional Nutanix cluster with all the necessary components pre-installed.

## Prerequisites

- Laptop with a modern web browser (Chrome, Firefox, or Edge recommended)
- Workshop access credentials (provided by your instructor)

## Steps

### 1. Connect to the Nutanix HPOC Environment

1. Open your web browser and navigate to the HPOC URL provided by your instructor
2. Enter the credentials provided to you:
   - Username: `adminuser@workshop.com` (example)
   - Password: `Workshop-Password` (example)

!!! note
    The actual credentials will be provided by your workshop instructor.

### 2. Access Prism Central

1. Once logged in, you will see the Prism Central dashboard
2. Take a moment to familiarize yourself with the interface
3. Note the following components:
   - Cluster health indicators
   - Resource utilization metrics
   - Navigation menu

![Prism Central Dashboard](https://via.placeholder.com/800x400?text=Prism+Central+Dashboard)

### 3. Verify Kubernetes Platform Access

1. In Prism Central, navigate to the "Kubernetes" section in the left menu
2. Verify that you can see the pre-deployed Kubernetes clusters
3. Click on the workshop cluster to view its details

### 4. Test Command Line Access

1. Open the Console or Terminal access method provided by your instructor
2. Log in using the provided credentials
3. Test connectivity by running:

```bash
kubectl get nodes
```

You should see a list of Kubernetes nodes in the cluster.

## Validation

You have successfully completed this lab if:

- [x] You can access Prism Central
- [x] You can view the Kubernetes cluster details
- [x] You can run basic kubectl commands

## Troubleshooting

If you encounter any issues connecting to the environment:

1. Verify that you're using the correct URL and credentials
2. Check your network connectivity
3. Clear your browser cache and cookies
4. Ask your instructor for assistance

## Next Steps

Now that you're connected to the environment, you're ready to learn about [LLMs and GenAI fundamentals](../fundamentals/index.md).
