# config.txt

树莓派并没有传统PC上的[BIOS](https://en.wikipedia.org/wiki/BIOS)。因为它也仅仅只是一个嵌入式平台。 类似传统PC里面BIOS中有关系统配置的一些字段都保存在一个叫做`config.txt`的可选纯文本文件里。在树莓派的CPU和操作系统初始化之前它将会被树莓派的GPU所读取，因此它和`bootcode.bin``start.elf`必须被放在你SD卡中的第一个分区里（boot）。在linux中可以很方便地通过管理员身份来编辑和修改`/boot/config.txt`，但在Win和OS X下你只会看到一个可用分区，而`config.txt`就在这个分区里，如果你的boot分区里没有这个文件，而你却希望更改下文中列出的一些配置选项，可以简单的创建一个以`config.txt`命名的txt文件。




一部分修改后的配置仅仅在你的树莓派重启后生效。在Linux启动完毕后，你可以通过如下命令来查看当前生效的一些设置：