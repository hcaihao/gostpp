# gostpp
gost c++ warp；一个c++调用的gost代理库；gost移植为msvc dll；

# 导出函数
extern __declspec(dllexport) void SetCallBack(cb fun, int val);
extern __declspec(dllexport) void StartProxy(char* cmdLine);
extern __declspec(dllexport) void StopProxy();
