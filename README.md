# centos7_rs
#--------centos7系统专用，其他的系统用不了-------------------------
#更新内核
wget --no-check-certificate -O rskernel.sh https://raw.githubusercontent.com/nsyncxy/centos7_rs/master/rskernel.sh && bash rskernel.sh
更新内核会重启系统
安装加速
yum install net-tools -y && wget --no-check-certificate -O serverspeeder.sh https://raw.githubusercontent.com/nsyncxy/centos7_rs/master/serverspeeder.sh && bash serverspeeder.sh

/etc/systemd/system/v*.service 内容改为
CapabilityBoundingSet=CAP_NET_ADMIN CAP_NET_BIND_SERVICE
#AmbientCapabilities=CAP_NET_ADMIN CAP_NET_BIND_SERVICE



