https://yoshiki0705.medium.com/how-i-passed-cka-ckad-by-personal-interest-5d3f48411319


# Certified Kubernetes Application Developer (CKAD)

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



```
note
:set paste
kubectl explain <resource name> — recursive | less 
```
