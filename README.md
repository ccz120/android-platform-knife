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

#### Qsahara �� fh_loader ���÷�

1����/output/bin/Ŀ¼�µ� Qsahara fh_loader������ /usr/bin/Ŀ¼�£������޸�Ȩ��Ϊ 777 ������chmod 777 /usr/bin/Qsahara �� chmod 777 /usr/bin/fh_loader

2����~/.bash_aliases���Զ������� -- fh53���ɶ���Ϊ�������ƣ���

alias fh53='sudo Qsahara -s 13:prog_emmc_firehose_8953_ddr.mbn && sudo fh_loader --sendxml=rawprogram_unsparse.xml --noprompt --showpercentagecomplete --zlpawarehost=0 --memoryname=emmc && sudo fh_loader --sendxml=patch0.xml --noprompt --showpercentagecomplete --zlpawarehost=0 --memoryname=emmc && sudo fh_loader --reset --noprompt --showpercentagecomplete --zlpawarehost=0 --memoryname=emmc'

3���ն˽����ͨ��汾������ɵľ���Ŀ¼�£��� bin_for_dl Ŀ¼�£�
���ն������� fh53
