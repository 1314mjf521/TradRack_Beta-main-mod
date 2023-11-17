<!--
 * @Author: Mjf
 * @Date: 2023-07-19 20:39:04
 * @LastEditTime: 2023-11-17 18:42:59
 * @LastEditors: Win_VScode
 * @Description: 
 * @FilePath: \undefinedf:\download\TradRack_Beta-main\STLs\TradRack_Beta-main-mod\TradRack_Beta-main-mod\切刀-快乐兔配置参考\readme.md
 * 版权声明暂无
-->

1、修改V1快乐兔py文件2523行，添加或是删除切刀代码 （锁定关键代码：def _form_tip_standalone）<br/>
>''self.gcode.run_script_from_command("FILAMENT_CUTTING")''<br/>

2、修改兔子配置文件parking_distance值大小（新版本已更改无需手动改）<br/>
    **parking_distance: 43.0**  # 控制灯丝停放到栅极垫圈的距离（与编码器的距离，范围=12-30）<br/>
3、快乐兔升级注意<br/>
&emsp;新版快乐兔增加了电机同步py，使用升级时需要将新文件拷贝指<br/>
&emsp;&emsp;&emsp;/home/用户名/klipper/klippy/extras<br/>
&emsp;软衔接制作<br/>
&emsp;&emsp;**ln -s /home/用户名/ERCF-Software-V3/extras/manual_extruder_stepper.py /home/用户名/klipper/klippy/extras/manual_extruder_stepper.py**<br/>
4、快乐兔V3版本的挤出电机改名了！需要注意  
5、新增xiao配置中文注释翻译，由于自用切刀文件不可抄配置，参考中文注释即可 
6、~~针对新版快乐兔V2代码，print.cfg中挤出机中TMC配置全部删除剪切至快乐兔文件夹~~
7、快乐兔V2全新方式完成安装后，针对切刀代码放置于  
>**/config/mmu/base/mmu_software.cfg** 

位置位于 
>**[gcode_macro _MMU_CUT_TIP]** 

同时修改 
>**/config/mmu/base/mmu_parameters.cfg** 

 >**form_tip_macro: _MMU_CUT_TIP**   # 切刀代码  
