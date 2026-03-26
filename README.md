# 【JHeart 权限维持BOF】：一键扫描上线主机“白加黑”维权点
## 【实现逻辑】

* 扫描目标机器启动项程序所在目录的所有程序是否可以“白加黑利用”
* 该启动项的状态是“已启用”
* 启动项程序所在目录有可写权限，方便后续写入“黑dll”
* 白程序需要有签名

## 【效果】

![](https://cdn.nlark.com/yuque/0/2026/png/1346970/1774522803369-dc639f7f-00fe-44d9-b198-7e4a2a9c4766.png)

```shell
03/26 18:48:37 beacon> jheart
03/26 18:48:37 [*] Tasked beacon to run JHeart: Scanning for white-app DLL hijacking opportunities ...
03/26 18:48:57 [+] host called home, sent: 6241 bytes
03/26 18:49:00 [+] received output:
[*] JHeart Scanning (Active Items Only) Started...
03/26 18:49:00 [+] received output:
[+] HIJACK: C:\Users\test\AppData\Roaming\baidu\BaiduNetdisk\ShellFolder64.exe (x64) -> Missing: ShellFolderDepend64.dll
    Path: C:\Users\test\AppData\Roaming\baidu\BaiduNetdisk

03/26 18:49:00 [+] received output:
[+] HIJACK: C:\Users\test\AppData\Roaming\baidu\BaiduNetdisk\ShellFolder64.exe (x64) -> Missing: ShellFolderDepend64.dll
    Path: C:\Users\test\AppData\Roaming\baidu\BaiduNetdisk

03/26 18:49:00 [+] received output:
[+] HIJACK: C:\QuarkCloudDrive\quark_cloud_drive.exe (x64) -> Missing: quark_cloud_drive_elf.dll
    Path: C:\QuarkCloudDrive

03/26 18:49:00 [+] received output:
[*] Scan Completed.
```

## 【使用方法】

保持该目录结构，将cna文件添加进CS，beacon交互窗口输入`jheart`即可开启扫描。

![](https://cdn.nlark.com/yuque/0/2026/png/1346970/1774525231272-7fd7f7a1-5144-4e02-8506-f26391b982eb.png)

## 【下载地址】

https://github.com/m1crofan/JHeart