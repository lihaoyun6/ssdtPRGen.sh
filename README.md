ssdtPRGen.sh
============

增加了对于Sandy Bridge及更高架构的奔腾和赛扬系列处理器的支持，您可以在终端中使用下列命令获取此脚本:

``` sh
curl -o ~/ssdtPRGen.sh https://raw.githubusercontent.com/lihaoyun6/ssdtPRGen.sh/Pentium/ssdtPRGen.sh
```

使用下列命令为脚本添加可执行权限，否则您将无法运行此脚本.
 
``` sh
chmod +x ~/ssdtPRGen.sh
```


帮助信息
----------------

``` sh
$ ~/ssdtPRGen.sh -h

Usage: ./ssdtPRGen.sh [-abcdfhlmptwx]
       -a 处理器设备名 (例如: CPU0, C000)
       -bclk 时钟频率 (基准时钟频率)
       -b 设备ID (例如如: Mac-F60DEB81FF30ACF6)
       -cpus 处理器物理核心数 [1-4]
       -d 调试信息处理:
          0 = 不输出任何调试信息
          1 = 将调试信息输出到: ssdt.dsl
          2 = 仅显示调试信息，不写入文件
          3 = 等同于同时应用1和2选项
       -developer 开发者模式 [0-1]
          0 = 关闭 – 从 /Users/mac/Library/ssdtPRGen 处读取所需文件
          1 = 开启 – 从 /Users/mac 处读取所需文件
       -extract 提取ACPI表至 [路径]
       -f 处理器主频 (时钟频率)
       -h 显示帮助信息 (即显示此文档)
       -lfm 最低空载频率
       -l 处理器逻辑核心数 [2-128]
       -mode 脚本工作模式 [normal/custom]:
           normal – 从计算机中自动提取所需的ACPI信息
           custom – 从此处读取所需的acpi信息: /Users/[username]/Desktop
       -m SMBIOS机型信息 (例如: MacPro6,1)
       -o 打开预先生成好的SSDT文件
       -p 处理器型号 (例如: 'E3-1285L v3')
       -show 显示支持的处理器标识:
           Sandy Bridge
           Ivy Bridge
           Haswell
           Broadwell
           Skylake
       -target 处理器类型:
          0 = Sandy Bridge
          1 = Ivy Bridge
          2 = Haswell
          3 = Broadwell
          4 = Skylake
       -turbo 最高睿频频率:
          对于 Sandy Bridge 和 Ivy Bridge 处理器，这个值通常是6300
          对于 Haswell 和 Broadwell 处理器，这个值通常是8000
       -t 额定功耗 [11.5 - 150]
       -w 设定 Ivy Bridge 处理器的工作模式:
          0 = no workarounds
          1 = inject extra (turbo) P-State at the top with maximum (turbo) frequency + 1 MHz
          2 = inject extra P-States at the bottom
          3 = both
       -x 内核电源管理设置:
          0 = 禁用 XCPM 内核电源管理
          1 = 启用 XCPM 内核电源管理

Note: lihaoyun6 汉化于 2016.7.5

```


