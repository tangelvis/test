
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
### 3、推送skywalking镜像到ecr仓库，并修改镜像仓库地址

```
sed -i 's/your_ecr_url/${ecr_url}/g' tpl/*.yaml
```

### 4、安装skywalking

```
./install.sh
```

## skywalking 操作
```
./skywalking <command>

最常用的skywalking命令有:
  status 查看skywalking ns状态  
  stop   停止所有skywalking pod
  start  启动所有skywalking pod
  delete
  create
  clear       

```


*测试*

**测试试**
