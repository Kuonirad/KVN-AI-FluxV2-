# KVN-AI FluxV2 Migration Project

This repository is dedicated to the migration from Flux v1 to Flux v2 for our Kubernetes GitOps workflow.

## Prerequisites

- Kubernetes cluster version 1.20 or newer
- Flux v2 CLI installed
- kubectl installed and configured to interact with your cluster

## Setup Instructions

1. Ensure your Kubernetes cluster is running and accessible.
2. Install the Flux v2 CLI:
   ```
   curl -s https://fluxcd.io/install.sh | sudo bash
   ```
3. Verify the Flux v2 installation:
   ```
   flux check --pre
   ```
4. Bootstrap Flux v2 on your cluster:
   ```
   flux bootstrap github \
     --owner=Kuonirad \
     --repository=KVN-AI-FluxV2- \
     --branch=main \
     --path=clusters/my-cluster
   ```

## Project Structure

- `/clusters`: Contains cluster-specific configurations
- `/apps`: Holds application manifests
- `/infrastructure`: Defines infrastructure components

## Next Steps

1. Define your cluster configuration in the `/clusters` directory.
2. Add your application manifests to the `/apps` directory.
3. Configure any necessary infrastructure components in the `/infrastructure` directory.
4. Commit and push your changes to trigger Flux v2 synchronization.

For more detailed information on Flux v2, refer to the [official documentation](https://fluxcd.io/flux/).
