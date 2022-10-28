1. 修改`plc4x_edgedevice.yaml`下的`address`为设备IP地址
2. 使用命令`kubectl apply -f shifu-modbus-rtu`安装deviceshifu
3. 使用`kubectl run nginx --image=nginx:1.21`命令在集群中启动一个nginx
4. 使用命令`kubectl exec -it nginx -- curl "deviceshifu-plc4x.deviceshifu.svc.cluster.local/read?40003:UINT[1]&40004:UINT[1]"` 尝试获取温湿度
