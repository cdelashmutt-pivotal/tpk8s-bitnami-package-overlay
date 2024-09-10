Patch your bitnami package install with the following:
tanzu project use <your-project>
tanzu operations clustergroup use <your-cg>

KUBECONFIG="$HOME/.config/tanzu/kube/config" kubectl create -f overlay-secret.yaml
KUBECONFIG="$HOME/.config/tanzu/kube/config" kubectl annotate pkgi bitnami.services.tanzu.vmware.com ext.packaging.carvel.dev/ytt-paths-from-secret-name.0=bitnami-overlay