# CKA-ExamPrep
CKA exam prep material

**Last min prep notes from **

https://arkalim.notion.site/Kubernetes-c64b2976b0364cc69864490edef33717

**fetch custom columns from pods with headers **

kubectl get pods -n namespace -o=custom-columns='POD_NAME:metadata.name,IP_ADDR:status.podIP' --sort-by=status.podIP

**Debug commands**

journalctl -e | grep 'error'

journalctl -u kubelet | grep 'fail'


****Certificate expiry or validity details ****

openssl x509 --noout -text -on <certficate-path >

**Api Resources:**

kubectl api-resources --namespaced
kubectl api-resources --namespaced -o name

**kubectl explain <RESOURCE>**

kubectl explain pv.spec.persistentVolumeReclaimPolicy
kubectl explain pv.spec.nodeAffinity.required

