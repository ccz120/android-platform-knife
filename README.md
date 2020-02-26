##Android Platform Knife

This is an almost dead project, just for personal debug use.

I think you should use Ubuntu desktop since Android native arch changed so fast and a lot

-----------------------------------------------------------------------------------------------------------------------------------------------------------

#### How to build?

	cd android-platform-knife/
	make -f Makefile.$(your-platform) CROSS_COMPILE=$(if-you-need)
	find what you build in ./output/bin/

#### How to use?
	cp all ./output/bin/* to your PATH

	or you can use my prebuild

	on Linux:
	source ./setenv.sh

	on Windows:
	.\setenv.bat

#### Qsahara 和 fh_loader 的用法

1）把/output/bin/目录下的 Qsahara fh_loader拷贝到 /usr/bin/目录下，并且修改权限为 777 ，例如chmod 777 /usr/bin/Qsahara 和 chmod 777 /usr/bin/fh_loader

2）在~/.bash_aliases中自定义命令 -- fh53（可定义为任意名称）：

alias fh53='sudo Qsahara -s 13:prog_emmc_firehose_8953_ddr.mbn && sudo fh_loader --sendxml=rawprogram_unsparse.xml --noprompt --showpercentagecomplete --zlpawarehost=0 --memoryname=emmc && sudo fh_loader --sendxml=patch0.xml --noprompt --showpercentagecomplete --zlpawarehost=0 --memoryname=emmc && sudo fh_loader --reset --noprompt --showpercentagecomplete --zlpawarehost=0 --memoryname=emmc'

3）终端进入高通大版本编译完成的镜像目录下，即 bin_for_dl 目录下：
在终端下运行 fh53
