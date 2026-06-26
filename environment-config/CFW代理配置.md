# 代理配置



## 网络卡顿

### 测试配置不合理

测速间隔建议设置为300s
```yaml
- { name: 自动选择, type: url-test, ..., interval: 300 }
```

默认的测速URL是google域名，从国内访问本身就慢、不稳定，且可能不准确，测速URL选择稳定的地址
```yaml
# 默认地址
url: 'http://www.gstatic.com/generate_204'

# 稳定地址
url: 'https://www.qualcomm.cn/generate_204'
```


### 直连域名未配置为DIRECT

在规则最前面加缺失的DIRECT域名

```yaml
rules:
    - 'DOMAIN,access.shandiancn.com,DIRECT'
    - 'DOMAIN-SUFFIX,huaweicloud.com,DIRECT'
    - 'DOMAIN-SUFFIX,oracle.com,DIRECT'
    - 'DOMAIN-SUFFIX,adoptium.net,DIRECT'
    - 'DOMAIN-SUFFIX,adoptopenjdk.net,DIRECT'
    - 'DOMAIN-SUFFIX,azul.com,DIRECT'
    - 'DOMAIN-SUFFIX,aliyun.com,DIRECT'
    - 'DOMAIN-SUFFIX,aliyuncs.com,DIRECT'
    - 'DOMAIN-SUFFIX,tsinghua.edu.cn,DIRECT'
    - 'DOMAIN-SUFFIX,ustc.edu.cn,DIRECT'
    # ... 原有规则继续
```