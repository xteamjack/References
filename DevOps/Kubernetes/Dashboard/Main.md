Ref: https://komodor.com/learn/kubernetes-dashboard/


## Install

1. Add dashboard to cluster using recommended configuration

```
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.6.1/aio/deploy/recommended.yaml

kubectl get all -n kubernetes-dashboard
```

2. Create service accounnt config/dashboard-user.yaml
3. Create cluster role binding config/dashboard-clusterrolebinding.yaml
4. Create bearer token config/dashboard-user-token.yaml

```
kubectl apply -f config/dashboard-user.yaml

kubectl apply -f config/dashboard-clusterrolebinding.yaml

kubectl apply -f config/dashboard-user-token-yaml

kubectl get secrets -n kubernetes-dashboard

```

```


NAME                              TYPE                                  DATA   AGE
dashboard-user-token              kubernetes.io/service-account-token   3      46h
kubernetes-dashboard-certs        Opaque                                0      47h
kubernetes-dashboard-csrf         Opaque                                1      47h
kubernetes-dashboard-key-holder   Opaque                                2      47h
```

## Start Dashboard

```
kubectl proxy
```

## Generate Token

```
kubectl get secret dashboard-user-token -n kubernetes-dashboard -o jsonpath={.data.token}” | base64 --decode
```

## Access Dashboard

http://127.0.0.1:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/#/login

### Stop Dashboard

```
kubectl delete -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.6.1/aio/deploy/recommended.yaml
```

