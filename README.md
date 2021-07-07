# wmt_hc32_study
My HC32F460 study  

## HC32F460 dev sdk  
* search baidupan, hc32f46x_ddl_Rev1.2.0.zip  

## 使用体会    
把玄宇芯的华大HC32F460JETA开发板跑通了，烧录方法如下：  
（1）首先，这个板有一定难度，无论是文档方面、焊接排针方面还是闪烁灯方面，需要较多的时间准备。  
（2）支持ISP串口烧录和串口读取固件，对于HC32F460JETA而言，PA13收PB14发PB11模式接地  
（不同型号接法不同，需参考文档）。烧录前需要reset，烧录后拔掉PB11的接地线之后也要reset才能真正运行。  
（3）MDK5工程需要先安装pack包。我用的是gpio_output工程做闪烁灯试验，但原来的代码的  
四个灯与板载的两个LED灯是不同的，所以需要另外接一个灯，我是把LED接在PA7和VSS之间。  
原本的代码里使用了一些脚，是HC32F460JETA没有的脚，但不会影响运行。  
（4）HC32F460有两个型号的开发板，建议买针脚少便宜的那个版本HC32F460JETA，  
因为焊接会比双排针容易一些（也容易得到排针）  
（5）中间的J4跳帽排针（标有VCC字样），看原理图是用于USB供电给VCC的（用于测量电流），   
需要用跳帽长期连接，当然如果烧录的时候接了VCC，即使这个跳帽没接上也能正常供电  
（6）ISP软件界面上左面那个按钮是读取，右面的执行按钮才是烧录写入  

## HC32F460JETA-LQFP48  
https://www.hdsc.com.cn/Category83-1484  

## 四季物联  
search baidupan, HC32F460JETA核心板_四季物联  

## HC32F460PETB-LQFP100  
https://www.hdsc.com.cn/Category83-1487  

## hc32f460 mdk5 plugin    
search baidupan, HDSC.HC32F46x.1.0.6.pack  
other hc32 mcu, see github_com_hdscmcu_pack-master.zip, or https://github.com/hdscmcu/pack  
https://gitee.com/mcuxmx/hc32f460  
https://github.com/wellrun/hc32f460  

