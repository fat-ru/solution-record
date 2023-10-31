## 1、克隆代码时SSL连接失败
   ![SSL连接失败](images/git-opration/ssl连接失败.jpg)
   - 正常网络访问github，会有访问失败的情况，需要开启vpn，vpn又导致克隆项目失败
   - **解决办法**：修改设置，解除ssl验证  
   `git config --global http.sslVerify "false"`