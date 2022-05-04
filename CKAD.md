https://yoshiki0705.medium.com/how-i-passed-cka-ckad-by-personal-interest-5d3f48411319


# Certified Kubernetes Application Developer (CKAD)
```
https://docs.linuxfoundation.org/tc-docs/certification/lf-candidate-handbook
https://docs.linuxfoundation.org/tc-docs/certification/tips-cka-and-ckad

https://helm.sh/docs/ 
https://kubernetes.io/docs/ 
https://kubernetes.io/blog/
https://github.com/kubernetes/
```
# Architecture
```
API Server
etcd
scheduler
controller
container runtime :docker
kubelet : agent 

```

<img width="290" alt="image" src="https://user-images.githubusercontent.com/24234662/166631826-ab1bada8-5caa-47e6-b90a-3da95d9ff74e.png">
copy from :  https://kodekloud.com/topic/recap-architecture/


```
Application Design and Build (2:30)
Application Deployment (2:00)
Application Observability and Maintenance (2:00)

Application Environment, Configurations, and Security (2:30)

Services and Networking (1:30)
```

# Application Design and Build 08-Apr-22
```
Job
CronJob

Init Container

Volumn : external stroage for containers outside the container file system
  volumn : defined in Pod spec
  volumnMounts : defined in Container spec pointing to volumn name
volumnType
  hostPath
    - Directory
    - DirectoryOrCreate
    - File
    - FileOrCreate
  emptyDir
  persistentVolumnClaim
```
# Application Deployment 08-Apr-22
```
Deployments
  - deployments : desired status for set of replica pods
Rolling Updates
  - kubectl set image deployment/nginx-deployment nginx=nginx:1.161 
  - kubectl rollout status deployment/nginx-deployment
  - kubectl rollout undo deployment/nginx-deployment
Deployment Strategies
  - blue/green : whole switch
  - canary : portion of user switch
Helm
  - package management tool
  - helm repository = collection of helm charts 
```

# Application Observability and Maintenance
```
API deprecation Policy
- k8s API
  - apiVersion
  - depreciateion window : 12months or 3 releases
  - migration guide
probes adn health checks
  - probe
    - part of container spec, detects the status of a container
    - types
      - liveness
      - readiness
      - startup
montitoring
  - install matrics server
  - kubectl top pod|node
Container logging
  - container log -> kubectl logs <pod_name> -c <container_name>
Debugging
  - check object status
  - check object config -> 
      kubectl describe
      kubectl get pod .. --all-namespace
  - check logs
    - container log : sudo cat /var/log/containers/kube...
  
```
# Application Environment, Configurations, and Security
```
CRD : Custom Resources : extension of kubernates API
  - CustomResourceDefinition
Service Account and Authentication
  - 
Admission Control
Compute Resource Management
Application Config
  - configMap
    an object that stores configuration data for application (key-value), passes to containers at runtime
  - secret
  - volume mounts vs environment variables
    volume mounts => data appers in the container's file system, eac top-level key in the config data becomes a file name
    environment variable => 
SecurityContext
  - part of pod and container spec, control advanced secuirty-related settings for container
  - user id 
```


```
note
:set paste
kubectl explain <resource name> — recursive | less 
```
