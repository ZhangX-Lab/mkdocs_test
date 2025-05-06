## 解析这些md文件的编写方式

- 构建个人博客.md 

    这个md文件是通过typora本地软件构建的，编写完之后将md文件以及对应的xxx_image文件夹一并放至该位置，这样上传的md文件能够正确显示图片。基本上能够满足日常的需求。

- mkdocs-gou-jian-xiang-mu-wen-dang.md

    是在gitbook上编写的文档，然后在github上下载压缩包并解压，使用了其中的`./gitbook`文件夹和对应的md文档。需要注意的是`.gtibook`文件夹不会被识别，需要手动修改为`gitbook`文件夹；然后在对应的md文件中将`.gitbook`替换为`gitbook`。这样就能正常显示在线文档了。相比较本地编写的优势，gitbook在编写大型项目文档时更具优势，零散个别的md文档编写则可以使用typora本地软件编写。
    
    注：mkdocs在md转换为html后的一些路径变化(比如图像前后存放的相对位置)会自动的被改变，不需要手动去更改。
    如：原本md文件中是`gitbook/xxx_image.jpg`转换为html文件后，由于自动添加了一个文件夹，并在文件夹里面放对应的html文件，所以该mkdocs库会主动的在转换过程中将路径改为`../gitbook/xxx_image.jpg`,而不需要自己手动改，这点需要注意。

