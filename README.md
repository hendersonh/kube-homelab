Installing NFS client (nfs-subdir-external-provioner)
URL: https://artifacthub.io/packages/helm/nfs-subdir-external-provisioner/nfs-subdir-external-provisioner

$ helm repo add nfs-subdir-external-provisioner https://kubernetes-sigs.github.io/nfs-subdir-external-provisioner/
$ helm install nfs-subdir-external-provisioner nfs-subdir-external-provisioner/nfs-subdir-external-provisioner \
    --create-namespace 
    --namespace nfs-subdir
    --set nfs.server=192.168.58.41 \
    --set nfs.path=/volume1/k3s-nfs
