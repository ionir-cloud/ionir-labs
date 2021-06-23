NFS-provisioner and NFS server with ionir PV backend storage


Deploy ionir's block storageClass - ionir-default

Create NFS server and NFS provisioner using storageClass ionir-default - deploy helm chart: nfs-server-provisioner-1.1.3.tgz (https://docs.bitnami.com/tutorials/deploy-applications-nfs-kubernetes/)

-> helm install stable/nfs-server-provisioner --set persistence.enabled=true,persistence.size=20Gi,persistence.storageClass=ionir-default --generate-name

Create volumes - deploy PVCs using new NFS Provisioner

Create test pod to access the NFS volumes - Deploy busybox pods using PVCs, via Deployment or/and ReplicationController
