# PiPowerControler
使在没有屏幕或者ssh连接等情况下完成关机命令有更好的交互，给Pi添加了关机/重启按钮，并在开机和关机后有提示音（windowsXP的关机和开机提示音）返回。
当然也可以自定义提示音文件。

# Build
linux
$git clone https://github.com/ShaoChenHeng/PiPowerControler
$cd PiPowerControl
$gcc -o poweron poweron.c -lwiringPi
$gcc -o poweroff poweroff.c -lwiringPi
$sudo vim /etc/rc.local
设置开机启动
在 exit 0前一行添加 pyhton3 /home/pi/PiPowerControl/code.py &

# 环境需求
python3.x
wiringPi
gcc

# 说明
可根据乐谱和十二平均律自行设计“.c”文件的乐谱。
电路连接：![https://github.com/ShaoChenHeng/PiPowerControler/blob/master/circuit.png]

# 参考博客
https://blog.csdn.net/xukai871105/article/details/17737005
http://shumeipai.nxez.com/2014/09/01/add-raspberry-pi-sent-to-reboot-off-button.html
https://bbs.pediy.com/thread-212916.htm
