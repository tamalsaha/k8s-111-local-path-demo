# k8s-111-local-path-demo

To get dynamic PVC provisioning working on GitHub actions with K8s 1.11, I had to make 2 changes:

1. Fix the selected node annotation is external-storage repo https://github.com/kmodules/external-storage/commit/e55adbadb4e859b525b0e22b1838822905503a1c and build my own rancher provisioner. appscode/local-path-provisioner:dev

2. Fix the kubeadmpatches for MasterConfiguration and NodeConfiguration https://github.com/tamalsaha/k8s-111-local-path-demo/blob/master/hack/kubernetes/kind.yaml
