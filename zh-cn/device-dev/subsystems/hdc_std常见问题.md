# hdc\_std常见问题<a name="ZH-CN_TOPIC_0000001119447290"></a>

-   [hdc\_std连接不到设备](#section1221016541119)
-   [hdc\_std运行不了](#section219185710311)

## hdc\_std连接不到设备<a name="section1221016541119"></a>

-   **现象描述**

    执行 "hdc\_std list targets"命令后结果为：\[Empty\]

-   **可能原因和解决方法**
    1.  设备没有被识别：

        在设备管理器中查看是否有hdc设备，在通用串行总线设备中会有“HDC Device”信息。如果没有，hdc无法连接。此时需要插拔设备，或者烧写最新的镜像。

    2.  hdc\_std工作异常：

        可以执行"hdc kill"或者"hdc start -r"杀掉hdc服务或者重启hdc服务，然后再执行hdc list targets查看是否已经可以获取设备信息。

        如果一直获取不到设备信息，请在任务管理器中查询是否有adb进程，该进程可能会对hdc产生干扰，可以将其杀掉后重复执行上面的步骤。

    3.  hdc\_std与设备不匹配：

        如果设备烧写的是最新镜像，hdc\_std也需要使用最新版本。由于hdc\_std会持续更新，请从开源仓developtools\_hdc\_standard中获取，具体位置在该开源仓的prebuilt目录。



## hdc\_std运行不了<a name="section219185710311"></a>

-   **现象描述**

    点击hdc\_std.exe文件无法运行。

-   **可能原因和解决方法**

    hdc\_std.exe不需要安装，直接放到磁盘上就能使用，也可以添加到环境变量中。通过打开cmd执行hdc\_std命令直接使用。


