expressso pvc
```
kind: PersistentVolumeClaim
apiVersion: v1
metadata:
  name: storage-elite
  namespace: expressolite-dev
  annotations:
    volume.beta.kubernetes.io/storage-class: sfs-storage-class
spec:
  accessModes:
  - ReadWriteOnce
  resources:
    requests:
      storage: 30Gi
```
deploy sftp
```
helm repo add emberstack https://emberstack.github.io/helm-charts
helm repo update
helm upgrade --install sftp emberstack/sftp
```
