
<a href="projects.html" class="backButton">
  <img src="images/whitearrowleft.png" alt="back arrow">
</a>

# Kubernetes Reference Design
---

This project was performed on request from Cybercom, a company in the front of development of it solutions working with microservices and it-infrastructure. 
Because some customers can't or won't host their kubernetes cluster on the cloud due to several different reasons, a local kubernetes solution is often the way to go. 
This solution or at least a base of the solution was developed through this project. 

To setup the infrastructure Terraform was used, in development it was setup with AWS, but has the ability to be used locally. 
Ansible with ansible-playbooks as well as Helm was used to setup monitoring 
tools such as Prometheus, Grafana, and alertmanager. These were placed in a monitoring namespace which can be seen below


```text
NAME                                                        TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)                      AGE
alertmanager-operated                                       ClusterIP   None             <none>        9093/TCP,9094/TCP,9094/UDP   3m29s
monitoring-kube-prometheus-alertmanager                     ClusterIP   10.110.153.109   <none>        9093/TCP                     3m41s
monitoring-kube-prometheus-operator                         ClusterIP   10.110.15.253    <none>        443/TCP                      3m41s
monitoring-kube-prometheus-prometheus                       NodePort    10.105.207.36    <none>        9090:30090/TCP               3m41s
monitoring-kube-prometheus-stack-grafana                    NodePort    10.99.117.41     <none>        80:32461/TCP                 3m41s
monitoring-kube-prometheus-stack-kube-state-metrics         ClusterIP   10.99.39.35      <none>        8080/TCP                     3m41s
monitoring-kube-prometheus-stack-prometheus-node-exporter   ClusterIP   10.103.223.85    <none>        9100/TCP                     3m41s
prometheus-operated                                         ClusterIP   None             <none>        9090/TCP                     3m29s
```

The logging solution consisted of EFL-stack (elasticsearch, fluentd, and logstash). Flux was used for continuous integration and deployed resources from the `releases/` and `namespaces/`
directories in the git repository.

<a href="https://github.com/Cladnic/K8sReferenceDesign" target="_blank" class="repository">
    <span>source code</span>
    <img src="images/whitegithubbtnimg.png" alt="github image">
</a>