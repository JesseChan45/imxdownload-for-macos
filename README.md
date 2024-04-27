# imxdownload-for-macos

正点原子 imxdownload 的 macOS 版本  

## Build

```shell
clang -O2 imxdownload.c -o imxdownload
```

## Download

```shell
./imxdownload xxx.bin /dev/sdx
```

## Difference

在 macOS 下 dd 命令的参数与 Linux 不同，以及在使用 dd 命令前，需要 unmount 相应的设备，否则会报 ```Resource Busy``` 错误

关于修改部分参数的文档

```
oflag=value[,value ...]
	Where value is one of the symbols from the following list.
	
	fsync	Set the O_FSYNC flag on the output file to make writes synchronous.
	sync	Set the O_SYNC flag on the output file to make writes synchronous. This is synonymous with the fsync value.
	direct	Set F_NOCACHE on the output file to make writes bypass any local caching.
```

