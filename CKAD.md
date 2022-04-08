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




```
note
:set paste
kubectl explain <resource name> — recursive | less 
```
