
## skywalking 安装

### 1、复制ca根证书到cert目录,生成skywalking证书
```
cp /app/xjk/fini-install/roles/fini/files/cert/ca.{key,crt}  cert/
./tls_gerner.sh
```

### 2、替换efs_url
```
sed -i 's/efs/\${EFS}/g' tpl/skywalking-pv.yaml
```
### 3、推送skywalking镜像到ecr仓库



### 4、安装skywalking
```
./install.sh
```
## skywalking 更新
### 111
### 222
### 333


*测试*

**测试试**
