helm install vote . -n vote --create-namespace --set role.create=true --set rolebinding.create=true

kubectl get po -n vote --watch

helm list -A

kubectl get po -n vote

kubectl logs \` kubectl get po -n vote | grep pre-install-job | awk '{print $1}' \` -n vote

helm uninstall vote -n vote

kubectl delete ns vote
