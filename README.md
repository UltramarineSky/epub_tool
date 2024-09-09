## Ⅰ epub_tool仓库介绍<br>
一些可用的epub工具<br>
1. `重构epub为规范格式_v2.8.3.py`->`utils\reformat_epub.py`<br>
作用：见原文件名。<br>
原始的百度贴吧帖子链接：[遥遥心航的帖子](https://jump2.bdimg.com/p/8090221625)。<br>
遥遥心航提供的原始文件：[蓝奏云网盘链接](https://wwb.lanzoub.com/b01k016hg) 密码：`i89p`。<br>
2. `重构epub并反文件名混淆.py`->`utils\decrypt_epub.py`<br>
作用：见原文件名。<br>
3. `重构epub并加入文件名混淆.py`->`utils\encrypt_epub.py`<br>
作用：见原文件名。<br>
4. `epub_tool.py`<br>
作用：对上述工具的整合。<br>

## Ⅱ 怎么使用？（仅针对最新版本）<br>
- python执行<br>
1. 下载python3.8；<br> 
2. 使用`git clone https://github.com/cnwxi/epub_tool.git`克隆本仓库；或直接在网页下载源码压缩包，解压后得到py文件；<br>
3. 执行py文件。
    - 单个工具执行：
    1. 使用命令行执行 `python 解压目标文件夹/epub_tool/utils/**.py` 或修改py为pyz双击运行。<br>
    - 整合工具执行：
    1. 使用命令行执行 `python 解压目标文件夹/epub_tool/epub_tool.py -i 需要处理的epub文件或者所在文件夹 -e/d/r` 其中e、d、r为不同的处理模式，分别是混淆`-e`、反混淆`-d`、重新格式化`-r`。
    2. 也可使用命令行执行 `python 解压目标文件夹/epub_tool/epub_tool.py -i 需要处理的epub文件或者所在文件夹 -m 处理模式`，处理模式为e、d、r。
- 可执行文件<br>
1. 从[releases](https://github.com/cnwxi/epub_tool/releases)下载对应的可执行文件；<br>
2. 现在也可以直接双击可执行文件了。<br>
![image](https://github.com/user-attachments/assets/53ed7c69-3f59-44fd-9c59-b754ada6c5a8)
3. 使用命令行工具执行。<br>
参数列表参考如下：<br>
\-i  后面接需要处理的epub文件或所在文件夹；<br>
\-e  无需后接任何参数，指定程序对epub进行混淆处理；<br>
\-d  无需后接任何参数，指定程序对epub进行反混淆处理；<br>
\-r  无需后接任何参数，指定程序对epub进行格式化处理。<br>
\-m  后接指定的处理模式，e、d、r。（可选，效果同上-e、-d、-r）
- 举例：<br>
在可执行文件所在文件夹打开命令行工具（或打开命令行工具后切换到可执行文件所在文件夹）。<br>
可使用的命令行工具如cmd/powershell/terminal等。<br>
输入`Windows_epub_tool.exe -i epub文件路径或所在文件夹路径 -d`或`Windows_epub_tool.exe -i epub文件路径或所在文件夹路径 -m d`
并回车（注意不同平台可执行文件名不一致）。<br>
此命令行指定程序读取指定目录下所有epub文件，并对这些文件进行反混淆。<br>
<details>
  <summary>Windows系统CMD命令行操作演示(点击以展开)</summary>
  <p>1. 可执行文件已下载至C:\Users\Administrator\Downloads\Programs位置，打开文件管理器，进入对应目录。如图：</p>
  <p align="center"><img src="https://github.com/user-attachments/assets/0cd71e92-714b-4f44-8060-ad5d353ebb7a" width="600"></p>
  <p>2. 在最上方地址输入框输入cmd并回车，则可以直接在此目录下打开cmd。如图：</p>
  <p align="center"><img src="https://github.com/user-attachments/assets/2f23826d-480a-4526-9dbe-f3fb06f5fa35" width="600"></p>
  <p align="center"><img src="https://github.com/user-attachments/assets/8def1166-f7f6-4738-bed8-0b3057e1d81b" width="600"></p>
  <p>3. 输入 Windows_epub_tool.exe -i epub文件路径或所在文件夹路径 -d （注：此为演示命令行，具体的输入文件/文件夹和执行模式需要你自行指定）
  <p>或 Windows_epub_tool.exe -i epub文件路径或所在文件夹路径 -m d 。如图：</p>
  <p align="center"><img src="https://github.com/user-attachments/assets/0e1c703f-1c78-4242-9dce-480219805005" width="600"></p>
</details>


## Ⅲ 执行遇到错误？
- epub无法正常规范/混淆/反混淆<br>
优先解压文件，查看其中content.opf文件，检查是否存在问题。若无法解决，在Issues区提交issue并附带原文件。

## Ⅳ 更新日志<br>
<details>
  <summary>点击以展开</summary>
  <p>

### 2024.09.09<br>
因额外依赖库未打包到可执行文件，重新打包可执行文件。<br>
### 2024.09.08<br>
为避免有人不会使用命令行工具，更新Windows系统下相关操作的基础流程。<br>
程序允许直接双击执行，后续再输入参数。<br>
对应操作忽略固定后缀跳过文件处理。_encrypt、_decrypt、_reformat<br>
### 2024.08.29<br>
修复混淆ID导致的反混淆不完全。<br>
修复存在异常opf时程序闪退问题。<br>
更新日志记录。<br>
### 2024.08.28<br>
整合代码，使用命令行批量处理epub文件。<br>
支持输入单个epub文件或epub文件所在文件夹，支持子目录遍历。<br>
修改输出路径，现为原epub文件同级路径，通过添加不同后缀`encrypt\decrypt\reformat`区分原文件和处理后文件。<br>
更新README。<br>
### 2024.08.11<br>
更新README。<br>
### 2024.06.19<br>
代码更新，使用相似度计算覆盖opf文件中未混淆的其他文件名情况。<br>
### 2024.06.13<br>
更新yml文件，由[lgernier](https://github.com/lgernierO)提交。<br>
### 2024.06.12<br>
针对cover页面未混淆的情况做更改。<br>
修改自动发布逻辑，修改py文件不触发CI，仅修改yml后触发。修改yml，无需手动执行才执行发布。<br>
### 2024.06.08<br>
CI配置文件更新，由[lgernier](https://github.com/lgernierO)提交。<br>
### 2024.06.07<br>
修改主函数逻辑，防止epub文件不存在导致的程序崩溃，由[lgernier](https://github.com/lgernierO)提交。<br>
加入CI自动构建，由[lgernier](https://github.com/lgernierO)提交。<br>
加入CI自动发布，由[No Response](https://github.com/cnwxi)提交。<br>
### 2024.05.28<br>
修正`重构epub为规范格式_v2.8.3.py`中生成的content.opf文件内容格式，由[lgernier](https://github.com/lgernierO)提交。<br>
### 2024.05.16<br>
更改文件输出路径，由[lgernier](https://github.com/lgernierO)提交。<br>
### 2024.05.09<br>
针对多看~slim文件进行修改，处理html中使用`../`、`./`、`/`开头的链接。<br>
### 2024.04.23<br>
初始化仓库。<br>

  </p>
</details>

## Ⅴ 鸣谢<br>
感谢以下用户对此项目的贡献：
- [遥遥心航](https://tieba.baidu.com/home/main?id=tb.1.7f262ae1.5_dXQ2Jp0F0MH9YJtgM2Ew)
- [lgernier](https://github.com/lgernierO)<br>
