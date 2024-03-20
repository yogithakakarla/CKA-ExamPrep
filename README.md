# CKA-ExamPrep
CKA exam prep material

**Last min prep notes from **

https://arkalim.notion.site/Kubernetes-c64b2976b0364cc69864490edef33717

**fetch custom columns from pods with headers **

kubectl get pods -n namespace -o=custom-columns='POD_NAME:metadata.name,IP_ADDR:status.podIP' --sort-by=status.podIP

**Debug commands**

journalctl -e | grep 'error'

journalctl -u kubelet | grep 'fail'

journalctl -u kubelet -f

journalctl -u kubelet --since "30 min ago" | grep 'Error:'


kubectl get event --field-selector involvedObject.name=kube-controller-manager-cluster4-controlplane -n kube-system


****Certificate expiry or validity details ****

openssl x509 --noout -text -on <certficate-path >

**Api Resources:**

kubectl api-resources --namespaced
kubectl api-resources --namespaced -o name

**kubectl explain <RESOURCE>**

kubectl explain pv.spec.persistentVolumeReclaimPolicy
kubectl explain pv.spec.nodeAffinity.required

**Run test pod to check svc running in that namespace**

 kubectl --context cluster3 run --rm  -i test-curl-pod --image=curlimages/curl --restart=Never -- curl -m 2 external-webserver-cka03-svcn
