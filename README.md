# gostpp
一个c++可以调用的gost代理库，基于gost 2.11.5 (go1.19.2 windows/amd64)构造，仅封装导出，未变更原始代码，支持gost所有命令；

# 导出函数
extern __declspec(dllexport) void StartProxy(char* cmdLine);

extern __declspec(dllexport) void StopProxy();

# 调用示例
StartProxy("-L=:8888 -F=socks5://usre:pass@127.0.0.1:8080");
