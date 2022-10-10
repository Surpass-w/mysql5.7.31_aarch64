# mysql5.7.31_aarch64

编译环境

| Os   | Kylin v10 sp1 |
| ---- | ------------- |
| Cpu  | Kunpeng 920   |



编译依赖安装

gcc > 7

```go
yum install gcc gcc-c++ cmake make zlib-devel openssl-devel cyrus-sasl-devel libaio-devel ncurses-devel numactl-devel openldap-devel perl-JSON  rpm-build -y
```

然后开始编译

```go
rpmbuild -ba /root/rpmbuild/SPECS/mysql.spec
```

如果编译过程中有 Could not find rpcgen的报错需要源码编译 rpcsvc

```go
tar -xvf rpcsvc-proto-1.4.1.tar

cd rpcsvc-proto-1.4.1

./configure

make

make install
```



