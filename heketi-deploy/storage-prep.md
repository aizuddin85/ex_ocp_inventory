oc create  -f gluster-endpoint.yaml 
oc get ep
oc create  -f  gluster-service.yaml 
oc get svc
oc create  -f gluster-volume.yaml 
oc create  -f gluster-claim.yaml 
oc get pv
oc get pvc


oc patch storageclass  gluster-dyn -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'