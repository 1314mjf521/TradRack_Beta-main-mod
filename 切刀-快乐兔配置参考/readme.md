<!--
 * @Author: Mjf
 * @Date: 2023-07-19 20:39:04
 * @LastEditTime: 2023-08-30 23:08:03
 * @LastEditors: Win_VScode
 * @Description: 
 * @FilePath: \undefinedf:\download\TradRack_Beta-main\STLs\TradRack_Beta-main-mod\TradRack_Beta-main-mod\切刀-快乐兔配置参考\readme.md
 * 版权声明暂无
-->

1、修改V1快乐兔py文件2523行，添加或是删除切刀代码 （锁定关键代码：def _form_tip_standalone）  
    self.gcode.run_script_from_command("FILAMENT_CUTTING")  
    **V2快乐兔测试方案不一定成功待验证其中V1方案确认可行，V2待验证**  
    v2快乐兔修改方式1，由于代码结构问题，V2将退料代码移至宏文件中所以本次修改位置厨上面的拔尖处外（归位使用）增加宏代码位置  
    mmu_software.cfg 文件的[gcode_macro _MMU_UNLOAD_SEQUENCE]宏代码下面添加切刀配置  
    例如：FILAMENT_CUTTING（切刀命令）  
    V2方法2依然查询_form_tip_standalone 这个代码，然后在"current_action = self._set_action(self.ACTION_FORMING_TIP)"这个代码上面添加切刀代码  
    self.gcode.run_script_from_command("FILAMENT_CUTTING")  
    修改：mmu_parameters.cfg中打开始终形成对立尖端force_form_tip_standalone: 1  
    同时建议修改toolhead_extruder_to_nozzle与 toolhead_sensor_to_nozzle 来完成对拔尖代码后的切刀文件的适配具体配比自行分析建议  
    

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
