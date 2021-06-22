
# prometheus-monitoring-alertmanager-on-kubernetes
all yaml to do monitor k8s(kubernetes) use prometheus and send alert  use alertmanager

notes:

the prometheus version is: prometheus-2.26.1.linux-amd64

create configmap from dir prometheus-config  use command:
kubectl --kubeconfig=kube/config   create configmap pro-config --from-file=proconfig/ -n namespace

so,you can use the configmap name pro-config in prometheus-pod.yaml

1,you must know the k8s rbac

2,you must have pvc and pv

3,you can get prometheus alert rules in here:https://awesome-prometheus-alerts.grep.to/


4,中文比较细致的文档，

https://github.com/yunlzheng/prometheus-book/blob/master/kubernetes/service-discovery-with-kubernetes.md

https://github.com/yunlzheng/prometheus-book/blob/master/kubernetes/use-prometheus-monitor-kubernetes.md

