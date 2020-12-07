# TinyJPEGDecoder

>  本仓库拷贝自https://github.com/fzyzwrj/TinyJPEGDecoder，做了稍许改动。

### 运行环境

Windows10；VS2017；Cmake

在目录下运行`Cmake .`，将生成`.sln`文件，打开项目并生成即可运行。

### 运行示例

```bash
TinyJPEGDecoder ./test_image/testrgb1x1.jpg yuv420p ./test_image/test
```

### 项目说明

* 在原仓库的基础上，增加了部分注释，修正了输出错误。

* 删除了原本的makefile文件：本人在Linux下make失败，原因是`jidctflt.c`嵌入了汇编代码（可能在Win下可以编译）
* 改动：当运行参数[format]设置为`YUV420p`时，将输出`.yuv`文件，而不仅仅是.Y .U .V文件
* 经过测试，JPG文件经过解码后能获得正确的输出文件，可以使用`YUVPlayer`自行尝试

### 相应博客

https://blog.csdn.net/leelitian3/article/details/110818955