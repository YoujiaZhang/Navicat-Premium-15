# Navicat-Premium-15

<p align="center">
<img src="/images/navicat.jpg" >
</p>

操作系统 ：**Ubuntu 18.04.6 LTS**

## 一、相关工具
- [navicat15-premium-cs.AppImage](https://github.com/YoujiaZhang/Navicat-Premium-15/releases/download/1.0/navicat15-premium-cs.AppImage) ：Navicat 15 premium 官方简体中文试用版
- navicat-patcher ：补丁
- navicat-keygen ：注册机
- appimagetool-x86_64.AppImage ：Linux 独立运行软件打包工具 

## 二、系统环境配置
安装 capstone
```
sudo apt-get install libcapstone-dev
```
安装 keystone
```
sudo apt-get install cmake

git clone https://github.com/keystone-engine/keystone.git
cd keystone
mkdir build
cd build
../make-share.sh
sudo make install
sudo ldconfig
```

安装 rapidjson
```
sudo apt-get install rapidjson-dev
```
## 三、操作步骤
1、赋予执行权限
```
chmod +x appimagetool-x86_64.AppImage
chmod +x navicat-patcher
chmod +x navicat-keygen
```
2、解包官方软件
```
mkdir navicat15
mount -o loop navicat15-premium-cs.AppImage navicat15
cp -r navicat15 navicat15-patched
```

3、运行补丁
```
./navicat-patcher navicat15-patched
```
生成RegPrivateKey.pem文件
```

**********************************************************
*       Navicat Patcher (Linux) by @DoubleLabyrinth      *
*                  Version: 1.0                          *
**********************************************************
[*] New RSA-2048 private key has been saved to
    ./RegPrivateKey.pem
*******************************************************
*           PATCH HAS BEEN DONE SUCCESSFULLY!         *
*                  HAVE FUN AND ENJOY~                *
*******************************************************
```
4、打包成独立运行软件
```
./appimagetool-x86_64.Appimage navicat15-patched navicat15-premium-cs-pathed.AppImage
```
5、运行补丁后软件包
```
chmod +x navicat15-premium-cs-pathed.AppImage
./navicat15-premium-cs-pathed.AppImage
```

6、运行注册机
```
./navicat-keygen --text ./RegPrivateKey.pem 
```
选择产品类型： 1 Premium
```
**********************************************************
*       Navicat Keygen (Linux) by @DoubleLabyrinth       *
*                   Version: 1.0                         *
**********************************************************

[*] Select Navicat product:
 1. DataModeler
 2. Premium
 3. MySQL
 4. PostgreSQL
 5. Oracle
 6. SQLServer
 7. SQLite
 8. MariaDB
 9. MongoDB
 10. ReportViewer

(Input index)> 1
```
选择语言： 1 Simplified Chinese
```
[*] Select product language:
 1. English
 2. Simplified Chinese
 3. Traditional Chinese
 4. Japanese
 5. Polish
 6. Spanish
 7. French
 8. German
 9. Korean
 10. Russian
 11. Portuguese

(Input index)> 1
```
选择版本： 15
```
[*] Input major version number:
(range: 0 ~ 15, default: 12)> 15
```

- **激活时必须断网！**
- **激活时必须断网！**
- **激活时必须断网！**

**生成序列号**： 填写至软件注册页面，并在断网后选择手工激活

```
[*] Serial number:
NAVC-PJWW-BKN4-C4YW (示例)
```

填写个人信息：

```
[*] Your name: YoujiaZhang
[*] Your organization: HUST
```

**输入注册码**： 复制软件激活页面注册码并粘贴此处

```
[*] Input request code in Base64: (Double press ENTER to end)
nqKkI0BtJR5Nq***==  (示例)
```

**生成激活码**： 复制Activation Code内容粘贴至软件激活页面

```
[*] Request Info:
{"K":"NAVCPJWWBKN4C4YW", "DI":"B0A1C7E8FA226577356B", "P":"linux"}

[*] Response Info:
{"K":"NAVCPJWWBKN4C4YW","DI":"B0A1C7E8FA226577356B","N":"zenghaiming","O":"hh","T":1582448573}

[*] Activation Code:
***CKrwYGzMf0OZgZCE***== (示例)
```
