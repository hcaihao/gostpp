# gostpp
一个c++可以调用的gost代理库

# 导出函数
extern __declspec(dllexport) void SetCallBack(cb fun, int val);

extern __declspec(dllexport) void StartProxy(char* cmdLine);

extern __declspec(dllexport) void StopProxy();

# 调用示例
StartProxy("-L=:8888 -F=socks5://usre:pass@127.0.0.1:8080");
