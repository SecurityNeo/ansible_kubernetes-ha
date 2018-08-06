# ansible_kubernetes-ha
使用ansible离线安装kubernetes HA集群

## 测试版本
- [Centos7](https://www.centos.org/)
- [Ansible](http://docs.ansible.com/intro_installation.html) 2.6.0

## 组件版本
组件名称|版本
--------------------|----------------
Kubernetes|1.10.4
Docker|18.03.1
Etcd|3.3.7
Flanneld|0.10.0
keepalived|2.0.5
haproxy|1.8.12
python_rhsm|1.19.9

## 变量定义
变量名|含义
------|------
package_dir|被控节点上存放安装集群所需二进制文件，脚本等的目录。
k8s_home_kube|k8s用户中存放kubeconfig文件的目录
root_home_kube|root用户中存放kubeconfig文件的目录
local_package_dir|ansible控制机上存放软件包的目录
local_template_dir|ansible控制机上存放一些证书,渲染的模板文件等的目录
kubernetes_log_dir|kubernetes组件日志文件目录
kubernetes_conf_dir|kubernetes配置文件目录
kubernetes_cert_dir|kubernetes证书目录
flanneld_cert_dir|flannel组件证书目录
etcd_cert_dir|ETCD组件证书目录
etcd_lib_dir|ETCD数据目录
docker_conf_dir|Docker配置文件目录
keepalived_src_dir|keepalived源码编译目录
keepalived_prefix_dir|keepalived文件存放目录
keepalived_conf_dir|keepalived配置文件目录
haproxy_src_dir|haproxy源码编译目录
haproxy_prefix_dir|haproxy文件存放目录
haproxy_conf_dir|haproxy配置文件目录
pod_infrastructure|infrastructure镜像地址
haproxy_user|运行haproxy组件的用户
haproxy_group|运行haproxy组件的用户组
haproxy_auth_name|haproxy认证用户
haproxy_auth_pass|haproxy认证密码
docker_group|docker用户组
k8s_user|kubernetes部分组件运行用户
haproxy_bind_port|haproxy绑定端口，kube-API端口
bind_interface|VIP绑定的接口
service_cidr|kubernetes service CIDR地址段
cluster_cidr|kubernetes 集群CIDR地址段
node_port_range|kubernetes端口范围
master_vip|集群虚IP地址
kube_apiserver|kubernetes API服务器URL
etcd_endpoints|ETCD endpoints URL
etcd_nodes|ETCD节点
flannel_etcd_prefix|
cluster_kubernetes_svc_ip|
cluster_dns_svc_ip|
cluster_dns_domain|
haproxy_make_option|
encryption_key|
docker_registry_mirrors|
master_servers|
worker_servers|