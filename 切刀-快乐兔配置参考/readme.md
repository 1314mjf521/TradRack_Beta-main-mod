
1、修改py文件2523行添加或是删除切刀代码 （锁定关键代码：def _form_tip_standalone）  
    self.gcode.run_script_from_command("FILAMENT_CUTTING")  
2、修改兔子配置文件parking_distance值大小  
    parking_distance: 43.0		# 控制灯丝停放到栅极垫圈的距离（与编码器的距离，范围=12-30）  
3、快乐兔升级注意    
    新版快乐兔增加了电机同步py，使用升级时需要将新文件拷贝指  
        /home/用户名/klipper/klippy/extras  
    软衔接制作  
      "ln -s /home/用户名/ERCF-Software-V3/extras/manual_extruder_stepper.py /home/用户名/klipper/klippy/extras/manual_extruder_stepper.py"  
4、快乐兔V3版本的挤出电机改名了！需要注意
