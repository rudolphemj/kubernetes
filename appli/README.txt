##### Installation des repos #####################################################
# metalLB
helm repo add metallb https://metallb.github.io/metallb

# ingress nginx
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx

# nginx


helm repo update


#### creation des namespace ####################################################### 
# Loadbalancer
kubectl create namespace metallb-system

# ingress





# installer le LB
kubectl create namespace metallb-system
helm install metallb metallb/metallb -n metallb-system


