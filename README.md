# kubernetes



\# créer un deploiment

k create deployment my-first-deployment --image=nginx:alpine



\# voir le deploiemnt

k get deployment my-first-deployment



\# scaler les replicas

k scale deployment/my-first-deployment --replicas=3



\# attriuer une image

k set image deployment my-first-deployment nginx=httpd:alpine



\# delete le depliement

k delete deployment my-first-deployment



================================================================



\# lancer un POD

k run my-pod --image=nginx:alpine



\# supprimer un POD

k delete pod my-pod



===================================================================

installer un tableau de bord



kubectl apply -f /root/dashboard.yaml



kubectl apply -f /root/dashboard.yaml

kubectl -n kubernetes-dashboard wait --for=condition=ready pod --all



service acoun

kubectl -n kubernetes-dashboard create sa admin-user

kubectl create clusterrolebinding admin-user --clusterrole cluster-admin --serviceaccount kubernetes-dashboard:admin-user

kubectl -n kubernetes-dashboard create token admin-user



kubectl -n kubernetes-dashboard port-forward service/kubernetes-dashboard 9090:9090 --address 0.0.0.0







