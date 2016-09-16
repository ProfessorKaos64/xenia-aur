# Current issues

Errors due to improperly generated makefiles (auto-added by premake):

```
==== Building vulkan-loader (debug_linux) ====
Creating obj/Linux/Debug/Linux/Debug/vulkan-loader
cJSON.c
error: invalid argument '-std=c++14' not allowed with 'C/ObjC'
vulkan-loader.make:185: recipe for target 'obj/Linux/Debug/Linux/Debug/vulkan-loader/cJSON.o' failed
make[1]: *** [obj/Linux/Debug/Linux/Debug/vulkan-loader/cJSON.o] Error 1
Makefile:216: recipe for target 'vulkan-loader' failed
make: *** [vulkan-loader] Error 2
```

see: src/xenia/build/vulkan.loader.make

# Links:

https://github.com/benvanik/xenia/issues/599
