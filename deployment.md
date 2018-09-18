deploy files in service dir to 
> /usr/lib/systemd/system/


```
// master
# systemctl daemon-reload
# systemctl enable kube-apiserver.service
# systemctl start kube-apiserver.service
# systemctl enable kube-controller-manager.service
# systemctl start kube-controller-manager.service
# systemctl enable kube-scheduler.service
# systemctl start kube-scheduler.service

// node
# systemctl daemon-reload
# systemctl enable kubelet.service
# systemctl start kubelet.service
# systemctl enable kube-proxy.service
# systemctl start kube-proxy.service


```