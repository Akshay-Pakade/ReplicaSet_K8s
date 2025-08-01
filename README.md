# ReplicaSet_K8s
ReplicaSet Practices and how to write replicaSet.yaml  and pod.yaml

Firstly we to create pod.yaml file
inside the pod.yaml file we write the code for creation of pod.
how to write yaml file ?
firstly we run the command kubectl explain pod --recursive > pod.txt
this command is create one pod.txt file 
after that with help of the pod.txt file
we write the pod.yaml file with help of pod.txt file
we need to create 4 pods in the k8s cluster so we write 4 times same code and pod name should be different
after that we simple give command in terminal kubectl apply -f pod.yaml
our pods are created
to check the created pods so simple give the command kubectl get pods
-----------------------------------------
follow same process for replicaSet creation
after that give the command kubectl apply -f replicaste.yaml
we see that our rs is created
after that for check our rs run the command kubectl get rs
-----------------------------------------
ImportantNote : Inside metadata labels should be mention in pod.yaml and same labels are write in replicaSet
-----------------------------------------
to check how replicaSet are working?
firstly we are delete one pod, and after that we are check the pod is delete or not.
we saw our pod is deleted and replicaSet is creates new pod replacement of the deleted pod.
-----------------------------------------