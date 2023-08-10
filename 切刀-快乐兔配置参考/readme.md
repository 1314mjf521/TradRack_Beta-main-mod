<!--
 * @Author: Mjf
 * @Date: 2023-07-19 20:39:04
 * @LastEditTime: 2023-08-11 00:10:12
 * @LastEditors: Win_VScode
 * @Description: 
 * @FilePath: \undefinedf:\download\TradRack_Beta-main\STLs\TradRack_Beta-main-mod\TradRack_Beta-main-mod\切刀-快乐兔配置参考\readme.md
 * 版权声明暂无
-->

1、修改V1快乐兔py文件2523行，V2快乐兔3310行，添加或是删除切刀代码 （锁定关键代码：def _form_tip_standalone）  
    self.gcode.run_script_from_command("FILAMENT_CUTTING")  
2、修改兔子配置文件parking_distance值大小（新版本已更改无需手动改）  
    parking_distance: 43.0		# 控制灯丝停放到栅极垫圈的距离（与编码器的距离，范围=12-30）  
3、快乐兔升级注意    
    新版快乐兔增加了电机同步py，使用升级时需要将新文件拷贝指  
        /home/用户名/klipper/klippy/extras  
    软衔接制作  
      "ln -s /home/用户名/ERCF-Software-V3/extras/manual_extruder_stepper.py /home/用户名/klipper/klippy/extras/manual_extruder_stepper.py"  
4、快乐兔V3版本的挤出电机改名了！需要注意 
5、新增xiao配置中文注释翻译，由于自用切刀文件不可抄配置，参考中文注释即可！  
6、针对新版快乐兔V2代码，print.cfg中挤出机中TMC配置全部删除剪切至快乐兔文件夹  
