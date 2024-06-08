## This article tells how to program/debug a STM32 MCU in an external application board with ST-LINK/V2-1 on Nucleo-64 development board<br>(e.g.NUCLEO-F411RE programming Blue Pill-STM32F103C8T6 by 4pin-Jumper Wire)    <br>    本文介绍如何使用Nucleo-64开发板上的ST-LINK/V2-1对外部应用板中的STM32 MCU进行编程/调试(e.g.NUCLEO-F411RE烧录Blue Pill-STM32F103C8T6(使用4根杜邦线))
<p></p>
 <p>The following schematic diagram is the 4th page of official document <a href="https://www.st.com/content/ccc/resource/technical/layouts_and_diagrams/schematic_pack/group2/74/18/73/70/3c/70/4a/52/MB1136-DEFAULT-C04_Schematic/files/MB1136-DEFAULT-C04_Schematic.pdf/jcr:content/translations/en.MB1136-DEFAULT-C04_Schematic.pdf">
MB1136-DEFAULT-C04 Board schematic</a> from ST official website open source ST-LINK/V2-1 schematic diagram.<br>
以下是ST官网官方文档<a href="https://www.st.com/content/ccc/resource/technical/layouts_and_diagrams/schematic_pack/group2/74/18/73/70/3c/70/4a/52/MB1136-DEFAULT-C04_Schematic/files/MB1136-DEFAULT-C04_Schematic.pdf/jcr:content/translations/en.MB1136-DEFAULT-C04_Schematic.pdf">
MB1136-DEFAULT-C04 Board schematic</a> 第4页官方开源的的ST-LINK/V2-1原理图</p>

![在这里插入图片描述](https://img-blog.csdnimg.cn/a489aa14e93e4baaa5f47c462fd0d1e8.jpeg)
<p>The following schematic diagram is the 19th page of official document <a href="https://www.st.com/resource/en/user_manual/um1724-stm32-nucleo64-boards-mb1136-stmicroelectronics.pdf">
UM1724
STM32 Nucleo-64 boards (MB1136)</a> which tells how to program/debug a STM32 MCU in an external application board with ST-LINK/V2-1 on Nucleo-64 development board<br>
以下是ST官网官方文档<a href="https://www.st.com/resource/en/user_manual/um1724-stm32-nucleo64-boards-mb1136-stmicroelectronics.pdf">
UM1724
STM32 Nucleo-64 boards (MB1136)</a> 第19页官方介绍如何使用Nucleo-64开发板上的ST-LINK/V2-1对外部应用板中的STM32 MCU进行编程/调试</p>

![在这里插入图片描述](https://img-blog.csdnimg.cn/699feee7e5054107ae414b7cac2be727.jpeg)
## It can be seen from the above figure that we should remove the two jumpers from CN2.<br>由上图可知我们需要从卸下CN2的两个跳线帽<br>Let's take a closer look at the schematic diagram of ST-LINK/V2-1.<br>让我们仔细看看ST-LINK/V2-1的原理图
![在这里插入图片描述](https://img-blog.csdnimg.cn/be9153869e6a442eadb9a72714538b16.png)
## We can find that after removing the two jumper caps of CN2, SWCLK and SWDIO of STLink are disconnected from SWD of STM on Nucelo-64 development board. <br>我们可以发现在卸下CN2的两个跳线帽之后，STLink的SWCLK和SWDIO与Nucelo-64开发板上的STM32F411RET6的SWD断开了
![在这里插入图片描述](https://img-blog.csdnimg.cn/5bafa423ef234ff1b6cc9242c8e1a712.png)![在这里插入图片描述](https://img-blog.csdnimg.cn/fbde1e5b89424adab9f55b5033cf8574.png)    
## thus using four Jumper Wire to program program/debug a STM32 MCU in an external application board with ST-LINK/V2-1 on Nucleo-64 development board<br>这样可以使用四根跳线在Nucleo-64开发板上使用ST-LINK/V2-1对外部应用板中的STM32 MCU进行编程/调试
![在这里插入图片描述](https://img-blog.csdnimg.cn/e8305002e685438192c7971bb4f5640e.png)

## 3V3&emsp;&emsp;&thinsp;wire to the Pin on the left of JP1(+3V3_ST_LINK)<br> SWCLK wire to the 2nd pin of CN4<br>GND &emsp;&thinsp;&thinsp;wire to the 3rd pin of CN4<br> SWDIO &thinsp;wire to the 4th pin of CN4<br><br>3V3&emsp;&emsp;&thinsp;接 JP1左边的管脚(+3V3_ST_LINK)<br> SWCLK 接 CN4的第2个管脚<br>GND &emsp;&thinsp;&thinsp;接 CN4的第3个管脚<br> SWDIO &thinsp;接 CN4的第4个管脚



![在这里插入图片描述](https://img-blog.csdnimg.cn/e40acdda74204e3cae0f83eb5d803301.jpeg)

 This article tells how to program/debug a STM32 MCU in an external application board using a cable connected to SWD connector CN4 on ST Nucleo-64 development board.(e.g.NUCLEO-F411RE)<br>本文介绍如何用ST Nucleo-64开发板SWD连接器CN4对外部应用板中的STM32 MCU进行编程/调试。

### References
<blockquote>
<p>[1]:<a href="https://www.st.com/resource/en/user_manual/um1724-stm32-nucleo64-boards-mb1136-stmicroelectronics.pdf">
UM1724
STM32 Nucleo-64 boards (MB1136)</a><br>
https://www.st.com/resource/en/user_manual/um1724-stm32-nucleo64-boards-mb1136-stmicroelectronics.pdf</p>
<p>[2]:<a href="https://www.st.com/content/ccc/resource/technical/layouts_and_diagrams/schematic_pack/group2/74/18/73/70/3c/70/4a/52/MB1136-DEFAULT-C04_Schematic/files/MB1136-DEFAULT-C04_Schematic.pdf/jcr:content/translations/en.MB1136-DEFAULT-C04_Schematic.pdf">
MB1136-DEFAULT-C04 Board schematic</a><br>
https://www.st.com/content/ccc/resource/technical/layouts_and_diagrams/schematic_pack/group2/74/18/73/70/3c/70/4a/52/MB1136-DEFAULT-C04_Schematic/files/MB1136-DEFAULT-C04_Schematic.pdf/jcr:content/translations/en.MB1136-DEFAULT-C04_Schematic.pdf</p>

</blockquote>
<hr> 
<blockquote>
<p>版权声明：本文为CSDN博主「<a href="https://apollo.blog.csdn.net">
Apollo-007</a>」的原创文章，</p><p>遵循<a href="https://creativecommons.org/licenses/by-nc-sa/4.0/">CC BY-NC-SA 4.0</a>版权协议，转载请附上原文出处链接及本声明。</p>
<p>原文链接:<a href="https://apollo.blog.csdn.net/article/details/128449083
">
https://apollo.blog.csdn.net/article/details/128449083</a></p> 
</blockquote> 
