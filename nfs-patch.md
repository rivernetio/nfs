1. 下载patch文件：
   
   ```
   链接: https://pan.baidu.com/s/1hshFd0S 密码: d9mh
   // 压缩包中包括 yaml和images两个文件夹
   ```

2. 上传镜像：

   ```
   解压压缩文件，执行命令上传镜像：
   docker load < ./images/nfs.tar
   ```

3. 创建nfs资源：

   ```
   // 修改./yaml/deployments.yaml 中的 192.168.254.42 为nfs server的地址，
   // /home/nfs 为nfs的共享路径，（每个都有两处要修改）。执行命令创建nfs资源：
   kubectl create -f ./yaml
   ```