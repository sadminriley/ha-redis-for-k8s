## High Availibility Redis for Kubernetes

This was originally inspired by a talented developer https://github.com/reallyenglish/k8s-redis-ha who also developed the lookup-srv found in both of these repos, I mostly changed and refined the implementation to compliment most microservice models/container patterns.

* This sets up redis using redis server and redis sentinel to create a HA redis pod to be used by other k8s services.

* Docker images for Redis and Sentinel
* Kubernetes configuration
* Runs on standard redis sentinel/server ports.

### Usage
* Change the ${SERVICE_NAME} in the deployment file(or set it as build or env variable in your CI/CD to create the images)
