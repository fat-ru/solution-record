# Ubuntu系统  
ubuntu apt命令安装的nodejs版本老旧。
使用nvm管理Node版本，支持管理多个node版本。

## 安装nvm

下载安装脚本并执行。
```shell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

重新加载shell
```shell
source ~/.bashrc
```

验证nvm版本
```shell
nvm -v
```

## 安装Node

使用nvm安装node
```shell
nvm install 20
nvm use 20
node -v
npm -v
```
