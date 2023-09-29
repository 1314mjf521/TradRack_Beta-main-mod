<!--
 * @Author: Mjf
 * @Date: 2023-09-16 18:54:57
 * @LastEditTime: 2023-09-24 23:14:50
 * @LastEditors: Win_VScode
 * @Description: 
 * @FilePath: \undefinedf:\download\TradRack_Beta-main\STLs\TradRack_Beta-main-mod\TradRack_Beta-main-mod\兔子板可打板\readme.md
 * 版权声明暂无
-->
### 梦梦专属兔子板V1.2
**原版xiao已做验证可正常使用，RP2040主板未验证不建议打**  

算了我补下零件清单吧
> 1、XH2.54  3-4P 插座（2040需要买点2P的）  
2、2P，7P-8P引脚（2.54单排母-2040需要9P跟5P的）  
3、独石电容0.33UF，0.1UF   
4、KF127-5.08 2P直插（电源输入-觉得不方便的自己换）  
5、10K色环电阻 其实每张板子就用4个（2040需要其它电阻的，另外就是0R贴片自己换导线）  
6、L7805CV电源转换（可换成5V1A或是5V3A模块不值钱自己换）  
7、直插电解电容25V100UF（白菜价）  
8、UART跟保护电阻啥的买个锤子直接烙铁焊接完事  
9、120欧 色环电阻（can板保护电路-2040专用）  
10、0欧贴片保护电阻（买个锤子-2040专用）  
11、100NF贴片电容（保护作用不要没啥事-2040专用）  
12、30PF贴片电容（保护作用不要没啥事-2040专用）  
13、CJ3400 SOT-23 场效应管  （4个扩展电路使用-2040专用）  
14、主控Seeduino Xiao  35一个随便买、RP2040-zero 超过15不要买  
15、单排排针买40个绝对用不完  

*xiao-兔子板引脚配置如下自行验证:*
>   G-EN PA2  
    G-STEP PA4  
    G-DIR PA10  
    S-EN PA11  
    S-STEP PA9  
    S-DIR PB8  
    UART PA8  
    SERVER1 PA6  
    SERVER2 PA5  
    ENCODER PB9  
    ENDSTOP PA7  

**RP204主板引脚待验证-验证中**
> 我也没验证没办法穷没打板卷了   
##  2023-09-24 RP2040-zero更新新增7.2V及热敏电阻位置不要问为啥因为我还没验证  
##  2023-09-29 RP2040-zero-V1.3原版存在UART无法使用，风扇电路短路问题，修改文件更改UART模式  