
# prometheus-monitoring-alertmanager-on-kubernetes
all yaml to do monitor k8s(kubernetes) use prometheus and send alert  use alertmanager

notes:

the prometheus version is: prometheus-2.26.1.linux-amd64


-------------------------------------------------------------------

you have additional to do:

0，create namespace kube-ops，all resource in this namespace，use command：

kubectl create ns kube-ops

1, create configmap from dir prometheus-config ， use command:

kubectl --kubeconfig=kube/config   create configmap pro-config --from-file=proconfig/ -n namespace

so,you can use theconfigmap name pro-config in prometheus-pod.yaml

2,you must know the k8s rbac

3,you must have pvc and pv。and the pvc name is：cce-evs-prometheus
  this used in prometheus-pod.yaml.and notes you pvc must in the same availability zone (az) in the cloud environment。
  see the topic in https://stackoverflow.com/  ，https://stackoverflow.com/questions/51946393/kubernetes-pod-warning-1-nodes-had-volume-node-affinity-conflict


------------------------------------------------------------
you can get prometheus alert rules in here:https://awesome-prometheus-alerts.grep.to/

中文比较细致的文档，

https://github.com/yunlzheng/prometheus-book/blob/master/kubernetes/service-discovery-with-kubernetes.md

https://github.com/yunlzheng/prometheus-book/blob/master/kubernetes/use-prometheus-monitor-kubernetes.md

