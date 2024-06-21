# gostpp
一个c++可以调用的gost代理库，基于gost 2.11.5 (go1.19.2 windows/amd64)，由msvc2019+win32构建，仅封装导出，未变更原始代码，支持gost所有命令；

# 导出函数
extern __declspec(dllexport) void StartProxy(char* cmdLine);

extern __declspec(dllexport) void StopProxy();

# 调用示例

作为标准HTTP/SOCKS5代理
```shell
gost -L=:8080
```

设置代理认证信息
```shell
gost -L=admin:123456@localhost:8080
```

多端口监听
```shell
gost -L=http2://:443 -L=socks5://:1080 -L=ss://aes-128-cfb:123456@:8338
```

设置转发代理
```shell
gost -L=:8080 -F=192.168.1.1:8081
```

转发代理认证
```shell
gost -L=:8080 -F=http://admin:123456@192.168.1.1:8081
```


更多命令参考gost官方文档


