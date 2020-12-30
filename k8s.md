Pods
---

list pods

    kubectl get pods

view log

    kubectl logs podName

stream log

    kubectl logs -f podName
    
view env

    kubectl exec podName -- printenv

execute command interactive

    kubectl exec -i podName -- bash
