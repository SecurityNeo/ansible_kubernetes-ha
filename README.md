# ansible_kubernetes-ha
使用ansible离线安装kubernetes HA集群

## 测试版本
- Centos7
- [Ansible](http://docs.ansible.com/intro_installation.html) 2.6.0

## 组件版本
组件名称|版本
--------------------|----------------
Kubernetes|1.10.4
Docker|18.03.1
Etcd|3.3.7
Flanneld|0.10.0
keepalived_version|2.0.5
haproxy_version|1.8.12
python_rhsm_version|1.19.9 

## 变量定义
变量名|含义
------|------
package_dir|
k8s_home_kube|
root_home_kube|
local_package_dir|
local_template_dir|
kubernetes_log_dir|
kubernetes_conf_dir|
kubernetes_cert_dir|
flanneld_cert_dir|
etcd_cert_dir|
etcd_lib_dir|
docker_conf_dir|
keepalived_src_dir|
keepalived_prefix_dir|
keepalived_conf_dir|
haproxy_src_dir|
haproxy_prefix_dir|
haproxy_conf_dir|
pod_infrastructure|
haproxy_user|
haproxy_group|
haproxy_auth_name|
haproxy_auth_pass|
docker_group|
k8s_user|
haproxy_bind_port|
bind_interface|
service_cidr|
cluster_cidr|
node_port_range|
master_vip|
kube_apiserver|
etcd_endpoints|
etcd_nodes|
flannel_etcd_prefix|
cluster_kubernetes_svc_ip|
cluster_dns_svc_ip|
cluster_dns_domain|
haproxy_make_option|
encryption_key|
docker_registry_mirrors|
master_servers|
worker_servers|