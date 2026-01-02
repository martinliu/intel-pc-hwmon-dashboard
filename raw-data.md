# Sensors Data

## Linux OS

```sh
root@pve:/etc/alloy# sensors
iwlwifi_1-virtual-0
Adapter: Virtual device
temp1:            N/A  

nct6776-isa-0a00
Adapter: ISA adapter
Vcore:                   1.15 V  (min =  +0.00 V, max =  +1.74 V)
in1:                     1.23 V  (min =  +0.00 V, max =  +0.00 V)  ALARM
AVCC:                    3.31 V  (min =  +2.98 V, max =  +3.63 V)
+3.3V:                   3.30 V  (min =  +2.98 V, max =  +3.63 V)
in4:                   936.00 mV (min =  +0.00 V, max =  +0.00 V)  ALARM
in5:                     0.00 V  (min =  +0.00 V, max =  +0.00 V)
in6:                   792.00 mV (min =  +0.00 V, max =  +0.00 V)  ALARM
3VSB:                    3.28 V  (min =  +2.98 V, max =  +3.63 V)
Vbat:                    3.15 V  (min =  +2.70 V, max =  +3.63 V)
fan1:                     0 RPM  (min =    0 RPM)
fan2:                     0 RPM  (min =    0 RPM)
SYSTIN:                 +69.0°C  (high = +80.0°C, hyst = +75.0°C)  sensor = thermistor
CPUTIN:                 +27.5°C  (high = +80.0°C, hyst = +75.0°C)  sensor = thermistor
AUXTIN:                 +37.5°C  (high = +80.0°C, hyst = +75.0°C)  sensor = thermistor
PCH_CHIP_TEMP:           +0.0°C  (high =  +0.0°C, hyst =  +0.0°C)  ALARM
PCH_CHIP_CPU_MAX_TEMP:  +22.0°C  (high = +80.0°C, hyst = +75.0°C)
PECI Agent 0:           +43.0°C  (high = +80.0°C, hyst = +75.0°C)
                                 (crit = +100.0°C)
PCH_CPU_TEMP:            +0.0°C  
PCH_MCH_TEMP:            +0.0°C  
pwm1:                       64%  (mode = dc)  MANUAL CONTROL
pwm2:                       35%  (mode = pwm)
intrusion0:            OK
intrusion1:            OK
beep_enable:           disabled

acpitz-acpi-0
Adapter: ACPI interface
temp1:        +27.8°C  
temp2:        +29.8°C  

pch_skylake-virtual-0
Adapter: Virtual device
temp1:        +22.0°C  

coretemp-isa-0000
Adapter: ISA adapter
Package id 0:  +54.0°C  (high = +100.0°C, crit = +100.0°C)
Core 0:        +40.0°C  (high = +100.0°C, crit = +100.0°C)
Core 1:        +39.0°C  (high = +100.0°C, crit = +100.0°C)
Core 2:        +54.0°C  (high = +100.0°C, crit = +100.0°C)
Core 3:        +43.0°C  (high = +100.0°C, crit = +100.0°C)
```

## Node-Exporter Metrics

```

# HELP node_hwmon_beep_enabled Hardware beep enabled
# TYPE node_hwmon_beep_enabled gauge
node_hwmon_beep_enabled{chip="platform_nct6775_2560",sensor="beep_enable0"} 0
# HELP node_hwmon_chip_names Annotation metric for human-readable chip names
# TYPE node_hwmon_chip_names gauge
node_hwmon_chip_names{chip="platform_coretemp_0",chip_name="coretemp"} 1
node_hwmon_chip_names{chip="platform_nct6775_2560",chip_name="nct6776"} 1
node_hwmon_chip_names{chip="thermal_thermal_zone0",chip_name="acpitz"} 1
node_hwmon_chip_names{chip="thermal_thermal_zone2",chip_name="pch_skylake"} 1
node_hwmon_chip_names{chip="thermal_thermal_zone4",chip_name="iwlwifi_1"} 1
# HELP node_hwmon_fan_alarm Hardware sensor alarm status (fan)
# TYPE node_hwmon_fan_alarm gauge
node_hwmon_fan_alarm{chip="platform_nct6775_2560",sensor="fan1"} 0
node_hwmon_fan_alarm{chip="platform_nct6775_2560",sensor="fan2"} 0
# HELP node_hwmon_fan_beep_enabled Hardware monitor sensor has beeping enabled
# TYPE node_hwmon_fan_beep_enabled gauge
node_hwmon_fan_beep_enabled{chip="platform_nct6775_2560",sensor="fan1"} 0
node_hwmon_fan_beep_enabled{chip="platform_nct6775_2560",sensor="fan2"} 0
# HELP node_hwmon_fan_min_rpm Hardware monitor for fan revolutions per minute (min)
# TYPE node_hwmon_fan_min_rpm gauge
node_hwmon_fan_min_rpm{chip="platform_nct6775_2560",sensor="fan1"} 0
node_hwmon_fan_min_rpm{chip="platform_nct6775_2560",sensor="fan2"} 0
# HELP node_hwmon_fan_pulses Hardware monitor fan element pulses
# TYPE node_hwmon_fan_pulses gauge
node_hwmon_fan_pulses{chip="platform_nct6775_2560",sensor="fan1"} 2
node_hwmon_fan_pulses{chip="platform_nct6775_2560",sensor="fan2"} 2
# HELP node_hwmon_fan_rpm Hardware monitor for fan revolutions per minute (input)
# TYPE node_hwmon_fan_rpm gauge
node_hwmon_fan_rpm{chip="platform_nct6775_2560",sensor="fan1"} 0
node_hwmon_fan_rpm{chip="platform_nct6775_2560",sensor="fan2"} 0
# HELP node_hwmon_fan_target_rpm Hardware monitor for fan revolutions per minute (target)
# TYPE node_hwmon_fan_target_rpm gauge
node_hwmon_fan_target_rpm{chip="platform_nct6775_2560",sensor="fan1"} 0
node_hwmon_fan_target_rpm{chip="platform_nct6775_2560",sensor="fan2"} 27000
# HELP node_hwmon_fan_tolerance Hardware monitor fan element tolerance
# TYPE node_hwmon_fan_tolerance gauge
node_hwmon_fan_tolerance{chip="platform_nct6775_2560",sensor="fan1"} 0
node_hwmon_fan_tolerance{chip="platform_nct6775_2560",sensor="fan2"} 2727
# HELP node_hwmon_in_alarm Hardware sensor alarm status (in)
# TYPE node_hwmon_in_alarm gauge
node_hwmon_in_alarm{chip="platform_nct6775_2560",sensor="in0"} 0
node_hwmon_in_alarm{chip="platform_nct6775_2560",sensor="in1"} 1
node_hwmon_in_alarm{chip="platform_nct6775_2560",sensor="in2"} 0
node_hwmon_in_alarm{chip="platform_nct6775_2560",sensor="in3"} 0
node_hwmon_in_alarm{chip="platform_nct6775_2560",sensor="in4"} 1
node_hwmon_in_alarm{chip="platform_nct6775_2560",sensor="in5"} 0
node_hwmon_in_alarm{chip="platform_nct6775_2560",sensor="in6"} 1
node_hwmon_in_alarm{chip="platform_nct6775_2560",sensor="in7"} 0
node_hwmon_in_alarm{chip="platform_nct6775_2560",sensor="in8"} 0
# HELP node_hwmon_in_beep_enabled Hardware monitor sensor has beeping enabled
# TYPE node_hwmon_in_beep_enabled gauge
node_hwmon_in_beep_enabled{chip="platform_nct6775_2560",sensor="in0"} 0
node_hwmon_in_beep_enabled{chip="platform_nct6775_2560",sensor="in1"} 0
node_hwmon_in_beep_enabled{chip="platform_nct6775_2560",sensor="in2"} 0
node_hwmon_in_beep_enabled{chip="platform_nct6775_2560",sensor="in3"} 0
node_hwmon_in_beep_enabled{chip="platform_nct6775_2560",sensor="in4"} 0
node_hwmon_in_beep_enabled{chip="platform_nct6775_2560",sensor="in5"} 0
node_hwmon_in_beep_enabled{chip="platform_nct6775_2560",sensor="in6"} 0
node_hwmon_in_beep_enabled{chip="platform_nct6775_2560",sensor="in7"} 0
node_hwmon_in_beep_enabled{chip="platform_nct6775_2560",sensor="in8"} 0
# HELP node_hwmon_in_max_volts Hardware monitor for voltage (max)
# TYPE node_hwmon_in_max_volts gauge
node_hwmon_in_max_volts{chip="platform_nct6775_2560",sensor="in0"} 1.744
node_hwmon_in_max_volts{chip="platform_nct6775_2560",sensor="in1"} 0
node_hwmon_in_max_volts{chip="platform_nct6775_2560",sensor="in2"} 3.632
node_hwmon_in_max_volts{chip="platform_nct6775_2560",sensor="in3"} 3.632
node_hwmon_in_max_volts{chip="platform_nct6775_2560",sensor="in4"} 0
node_hwmon_in_max_volts{chip="platform_nct6775_2560",sensor="in5"} 0
node_hwmon_in_max_volts{chip="platform_nct6775_2560",sensor="in6"} 0
node_hwmon_in_max_volts{chip="platform_nct6775_2560",sensor="in7"} 3.632
node_hwmon_in_max_volts{chip="platform_nct6775_2560",sensor="in8"} 3.632
# HELP node_hwmon_in_min_volts Hardware monitor for voltage (min)
# TYPE node_hwmon_in_min_volts gauge
node_hwmon_in_min_volts{chip="platform_nct6775_2560",sensor="in0"} 0
node_hwmon_in_min_volts{chip="platform_nct6775_2560",sensor="in1"} 0
node_hwmon_in_min_volts{chip="platform_nct6775_2560",sensor="in2"} 2.976
node_hwmon_in_min_volts{chip="platform_nct6775_2560",sensor="in3"} 2.976
node_hwmon_in_min_volts{chip="platform_nct6775_2560",sensor="in4"} 0
node_hwmon_in_min_volts{chip="platform_nct6775_2560",sensor="in5"} 0
node_hwmon_in_min_volts{chip="platform_nct6775_2560",sensor="in6"} 0
node_hwmon_in_min_volts{chip="platform_nct6775_2560",sensor="in7"} 2.976
node_hwmon_in_min_volts{chip="platform_nct6775_2560",sensor="in8"} 2.704
# HELP node_hwmon_in_volts Hardware monitor for voltage (input)
# TYPE node_hwmon_in_volts gauge
node_hwmon_in_volts{chip="platform_nct6775_2560",sensor="in0"} 0.976
node_hwmon_in_volts{chip="platform_nct6775_2560",sensor="in1"} 1.224
node_hwmon_in_volts{chip="platform_nct6775_2560",sensor="in2"} 3.3120000000000003
node_hwmon_in_volts{chip="platform_nct6775_2560",sensor="in3"} 3.2960000000000003
node_hwmon_in_volts{chip="platform_nct6775_2560",sensor="in4"} 0.936
node_hwmon_in_volts{chip="platform_nct6775_2560",sensor="in5"} 0
node_hwmon_in_volts{chip="platform_nct6775_2560",sensor="in6"} 0.792
node_hwmon_in_volts{chip="platform_nct6775_2560",sensor="in7"} 3.2800000000000002
node_hwmon_in_volts{chip="platform_nct6775_2560",sensor="in8"} 3.152
# HELP node_hwmon_intrusion_alarm Hardware sensor alarm status (intrusion)
# TYPE node_hwmon_intrusion_alarm gauge
node_hwmon_intrusion_alarm{chip="platform_nct6775_2560",sensor="intrusion0"} 0
node_hwmon_intrusion_alarm{chip="platform_nct6775_2560",sensor="intrusion1"} 0
# HELP node_hwmon_intrusion_beep_enabled Hardware monitor sensor has beeping enabled
# TYPE node_hwmon_intrusion_beep_enabled gauge
node_hwmon_intrusion_beep_enabled{chip="platform_nct6775_2560",sensor="intrusion0"} 0
node_hwmon_intrusion_beep_enabled{chip="platform_nct6775_2560",sensor="intrusion1"} 0
# HELP node_hwmon_pwm Hardware monitor pwm element 
# TYPE node_hwmon_pwm gauge
node_hwmon_pwm{chip="platform_nct6775_2560",sensor="pwm1"} 127
node_hwmon_pwm{chip="platform_nct6775_2560",sensor="pwm2"} 70
# HELP node_hwmon_pwm_auto_point1_pwm Hardware monitor pwm element auto_point1_pwm
# TYPE node_hwmon_pwm_auto_point1_pwm gauge
node_hwmon_pwm_auto_point1_pwm{chip="platform_nct6775_2560",sensor="pwm1"} 140
node_hwmon_pwm_auto_point1_pwm{chip="platform_nct6775_2560",sensor="pwm2"} 70
# HELP node_hwmon_pwm_auto_point1_temp Hardware monitor pwm element auto_point1_temp
# TYPE node_hwmon_pwm_auto_point1_temp gauge
node_hwmon_pwm_auto_point1_temp{chip="platform_nct6775_2560",sensor="pwm1"} 25000
node_hwmon_pwm_auto_point1_temp{chip="platform_nct6775_2560",sensor="pwm2"} 50000
# HELP node_hwmon_pwm_auto_point2_pwm Hardware monitor pwm element auto_point2_pwm
# TYPE node_hwmon_pwm_auto_point2_pwm gauge
node_hwmon_pwm_auto_point2_pwm{chip="platform_nct6775_2560",sensor="pwm1"} 170
node_hwmon_pwm_auto_point2_pwm{chip="platform_nct6775_2560",sensor="pwm2"} 70
# HELP node_hwmon_pwm_auto_point2_temp Hardware monitor pwm element auto_point2_temp
# TYPE node_hwmon_pwm_auto_point2_temp gauge
node_hwmon_pwm_auto_point2_temp{chip="platform_nct6775_2560",sensor="pwm1"} 35000
node_hwmon_pwm_auto_point2_temp{chip="platform_nct6775_2560",sensor="pwm2"} 65000
# HELP node_hwmon_pwm_auto_point3_pwm Hardware monitor pwm element auto_point3_pwm
# TYPE node_hwmon_pwm_auto_point3_pwm gauge
node_hwmon_pwm_auto_point3_pwm{chip="platform_nct6775_2560",sensor="pwm1"} 200
node_hwmon_pwm_auto_point3_pwm{chip="platform_nct6775_2560",sensor="pwm2"} 133
# HELP node_hwmon_pwm_auto_point3_temp Hardware monitor pwm element auto_point3_temp
# TYPE node_hwmon_pwm_auto_point3_temp gauge
node_hwmon_pwm_auto_point3_temp{chip="platform_nct6775_2560",sensor="pwm1"} 45000
node_hwmon_pwm_auto_point3_temp{chip="platform_nct6775_2560",sensor="pwm2"} 92000
# HELP node_hwmon_pwm_auto_point4_pwm Hardware monitor pwm element auto_point4_pwm
# TYPE node_hwmon_pwm_auto_point4_pwm gauge
node_hwmon_pwm_auto_point4_pwm{chip="platform_nct6775_2560",sensor="pwm1"} 230
node_hwmon_pwm_auto_point4_pwm{chip="platform_nct6775_2560",sensor="pwm2"} 150
# HELP node_hwmon_pwm_auto_point4_temp Hardware monitor pwm element auto_point4_temp
# TYPE node_hwmon_pwm_auto_point4_temp gauge
node_hwmon_pwm_auto_point4_temp{chip="platform_nct6775_2560",sensor="pwm1"} 55000
node_hwmon_pwm_auto_point4_temp{chip="platform_nct6775_2560",sensor="pwm2"} 98000
# HELP node_hwmon_pwm_auto_point5_pwm Hardware monitor pwm element auto_point5_pwm
# TYPE node_hwmon_pwm_auto_point5_pwm gauge
node_hwmon_pwm_auto_point5_pwm{chip="platform_nct6775_2560",sensor="pwm1"} 255
node_hwmon_pwm_auto_point5_pwm{chip="platform_nct6775_2560",sensor="pwm2"} 255
# HELP node_hwmon_pwm_auto_point5_temp Hardware monitor pwm element auto_point5_temp
# TYPE node_hwmon_pwm_auto_point5_temp gauge
node_hwmon_pwm_auto_point5_temp{chip="platform_nct6775_2560",sensor="pwm1"} 60000
node_hwmon_pwm_auto_point5_temp{chip="platform_nct6775_2560",sensor="pwm2"} 127000
# HELP node_hwmon_pwm_crit_temp_tolerance Hardware monitor pwm element crit_temp_tolerance
# TYPE node_hwmon_pwm_crit_temp_tolerance gauge
node_hwmon_pwm_crit_temp_tolerance{chip="platform_nct6775_2560",sensor="pwm1"} 0
node_hwmon_pwm_crit_temp_tolerance{chip="platform_nct6775_2560",sensor="pwm2"} 2000
# HELP node_hwmon_pwm_enable Hardware monitor pwm element enable
# TYPE node_hwmon_pwm_enable gauge
node_hwmon_pwm_enable{chip="platform_nct6775_2560",sensor="pwm1"} 1
node_hwmon_pwm_enable{chip="platform_nct6775_2560",sensor="pwm2"} 5
# HELP node_hwmon_pwm_floor Hardware monitor pwm element floor
# TYPE node_hwmon_pwm_floor gauge
node_hwmon_pwm_floor{chip="platform_nct6775_2560",sensor="pwm1"} 1
node_hwmon_pwm_floor{chip="platform_nct6775_2560",sensor="pwm2"} 1
# HELP node_hwmon_pwm_mode Hardware monitor pwm element mode
# TYPE node_hwmon_pwm_mode gauge
node_hwmon_pwm_mode{chip="platform_nct6775_2560",sensor="pwm1"} 0
node_hwmon_pwm_mode{chip="platform_nct6775_2560",sensor="pwm2"} 1
# HELP node_hwmon_pwm_start Hardware monitor pwm element start
# TYPE node_hwmon_pwm_start gauge
node_hwmon_pwm_start{chip="platform_nct6775_2560",sensor="pwm1"} 1
node_hwmon_pwm_start{chip="platform_nct6775_2560",sensor="pwm2"} 1
# HELP node_hwmon_pwm_step_down_time Hardware monitor pwm element step_down_time
# TYPE node_hwmon_pwm_step_down_time gauge
node_hwmon_pwm_step_down_time{chip="platform_nct6775_2560",sensor="pwm1"} 1000
node_hwmon_pwm_step_down_time{chip="platform_nct6775_2560",sensor="pwm2"} 2400
# HELP node_hwmon_pwm_step_up_time Hardware monitor pwm element step_up_time
# TYPE node_hwmon_pwm_step_up_time gauge
node_hwmon_pwm_step_up_time{chip="platform_nct6775_2560",sensor="pwm1"} 1000
node_hwmon_pwm_step_up_time{chip="platform_nct6775_2560",sensor="pwm2"} 1200
# HELP node_hwmon_pwm_stop_time Hardware monitor pwm element stop_time
# TYPE node_hwmon_pwm_stop_time gauge
node_hwmon_pwm_stop_time{chip="platform_nct6775_2560",sensor="pwm1"} 6000
node_hwmon_pwm_stop_time{chip="platform_nct6775_2560",sensor="pwm2"} 24000
# HELP node_hwmon_pwm_target_temp Hardware monitor pwm element target_temp
# TYPE node_hwmon_pwm_target_temp gauge
node_hwmon_pwm_target_temp{chip="platform_nct6775_2560",sensor="pwm1"} 0
node_hwmon_pwm_target_temp{chip="platform_nct6775_2560",sensor="pwm2"} 50000
# HELP node_hwmon_pwm_temp_sel Hardware monitor pwm element temp_sel
# TYPE node_hwmon_pwm_temp_sel gauge
node_hwmon_pwm_temp_sel{chip="platform_nct6775_2560",sensor="pwm1"} 1
node_hwmon_pwm_temp_sel{chip="platform_nct6775_2560",sensor="pwm2"} 9
# HELP node_hwmon_pwm_temp_tolerance Hardware monitor pwm element temp_tolerance
# TYPE node_hwmon_pwm_temp_tolerance gauge
node_hwmon_pwm_temp_tolerance{chip="platform_nct6775_2560",sensor="pwm1"} 0
node_hwmon_pwm_temp_tolerance{chip="platform_nct6775_2560",sensor="pwm2"} 5000
# HELP node_hwmon_pwm_weight_duty_base Hardware monitor pwm element weight_duty_base
# TYPE node_hwmon_pwm_weight_duty_base gauge
node_hwmon_pwm_weight_duty_base{chip="platform_nct6775_2560",sensor="pwm1"} 0
node_hwmon_pwm_weight_duty_base{chip="platform_nct6775_2560",sensor="pwm2"} 0
# HELP node_hwmon_pwm_weight_duty_step Hardware monitor pwm element weight_duty_step
# TYPE node_hwmon_pwm_weight_duty_step gauge
node_hwmon_pwm_weight_duty_step{chip="platform_nct6775_2560",sensor="pwm1"} 0
node_hwmon_pwm_weight_duty_step{chip="platform_nct6775_2560",sensor="pwm2"} 5
# HELP node_hwmon_pwm_weight_temp_sel Hardware monitor pwm element weight_temp_sel
# TYPE node_hwmon_pwm_weight_temp_sel gauge
node_hwmon_pwm_weight_temp_sel{chip="platform_nct6775_2560",sensor="pwm1"} 0
node_hwmon_pwm_weight_temp_sel{chip="platform_nct6775_2560",sensor="pwm2"} 0
# HELP node_hwmon_pwm_weight_temp_step Hardware monitor pwm element weight_temp_step
# TYPE node_hwmon_pwm_weight_temp_step gauge
node_hwmon_pwm_weight_temp_step{chip="platform_nct6775_2560",sensor="pwm1"} 0
node_hwmon_pwm_weight_temp_step{chip="platform_nct6775_2560",sensor="pwm2"} 1000
# HELP node_hwmon_pwm_weight_temp_step_base Hardware monitor pwm element weight_temp_step_base
# TYPE node_hwmon_pwm_weight_temp_step_base gauge
node_hwmon_pwm_weight_temp_step_base{chip="platform_nct6775_2560",sensor="pwm1"} 0
node_hwmon_pwm_weight_temp_step_base{chip="platform_nct6775_2560",sensor="pwm2"} 90000
# HELP node_hwmon_pwm_weight_temp_step_tol Hardware monitor pwm element weight_temp_step_tol
# TYPE node_hwmon_pwm_weight_temp_step_tol gauge
node_hwmon_pwm_weight_temp_step_tol{chip="platform_nct6775_2560",sensor="pwm1"} 0
node_hwmon_pwm_weight_temp_step_tol{chip="platform_nct6775_2560",sensor="pwm2"} 2000
# HELP node_hwmon_sensor_label Label for given chip and sensor
# TYPE node_hwmon_sensor_label gauge
node_hwmon_sensor_label{chip="platform_coretemp_0",label="Core 0",sensor="temp2"} 1
node_hwmon_sensor_label{chip="platform_coretemp_0",label="Core 1",sensor="temp3"} 1
node_hwmon_sensor_label{chip="platform_coretemp_0",label="Core 2",sensor="temp4"} 1
node_hwmon_sensor_label{chip="platform_coretemp_0",label="Core 3",sensor="temp5"} 1
node_hwmon_sensor_label{chip="platform_coretemp_0",label="Package id 0",sensor="temp1"} 1
node_hwmon_sensor_label{chip="platform_nct6775_2560",label="AUXTIN",sensor="temp3"} 1
node_hwmon_sensor_label{chip="platform_nct6775_2560",label="CPUTIN",sensor="temp2"} 1
node_hwmon_sensor_label{chip="platform_nct6775_2560",label="PCH_CHIP_CPU_MAX_TEMP",sensor="temp8"} 1
node_hwmon_sensor_label{chip="platform_nct6775_2560",label="PCH_CHIP_TEMP",sensor="temp7"} 1
node_hwmon_sensor_label{chip="platform_nct6775_2560",label="PCH_CPU_TEMP",sensor="temp10"} 1
node_hwmon_sensor_label{chip="platform_nct6775_2560",label="PCH_MCH_TEMP",sensor="temp11"} 1
node_hwmon_sensor_label{chip="platform_nct6775_2560",label="PECI Agent 0",sensor="temp9"} 1
node_hwmon_sensor_label{chip="platform_nct6775_2560",label="SYSTIN",sensor="temp1"} 1
# HELP node_hwmon_temp_alarm Hardware sensor alarm status (temp)
# TYPE node_hwmon_temp_alarm gauge
node_hwmon_temp_alarm{chip="platform_nct6775_2560",sensor="temp2"} 0
node_hwmon_temp_alarm{chip="platform_nct6775_2560",sensor="temp3"} 0
node_hwmon_temp_alarm{chip="platform_nct6775_2560",sensor="temp7"} 1
# HELP node_hwmon_temp_beep_enabled Hardware monitor sensor has beeping enabled
# TYPE node_hwmon_temp_beep_enabled gauge
node_hwmon_temp_beep_enabled{chip="platform_nct6775_2560",sensor="temp1"} 0
node_hwmon_temp_beep_enabled{chip="platform_nct6775_2560",sensor="temp2"} 0
node_hwmon_temp_beep_enabled{chip="platform_nct6775_2560",sensor="temp3"} 0
node_hwmon_temp_beep_enabled{chip="platform_nct6775_2560",sensor="temp7"} 0
node_hwmon_temp_beep_enabled{chip="platform_nct6775_2560",sensor="temp8"} 0
node_hwmon_temp_beep_enabled{chip="platform_nct6775_2560",sensor="temp9"} 0
# HELP node_hwmon_temp_celsius Hardware monitor for temperature (input)
# TYPE node_hwmon_temp_celsius gauge
node_hwmon_temp_celsius{chip="platform_coretemp_0",sensor="temp1"} 44
node_hwmon_temp_celsius{chip="platform_coretemp_0",sensor="temp2"} 37
node_hwmon_temp_celsius{chip="platform_coretemp_0",sensor="temp3"} 36
node_hwmon_temp_celsius{chip="platform_coretemp_0",sensor="temp4"} 47
node_hwmon_temp_celsius{chip="platform_coretemp_0",sensor="temp5"} 37
node_hwmon_temp_celsius{chip="platform_nct6775_2560",sensor="temp1"} 69
node_hwmon_temp_celsius{chip="platform_nct6775_2560",sensor="temp10"} 0
node_hwmon_temp_celsius{chip="platform_nct6775_2560",sensor="temp11"} 0
node_hwmon_temp_celsius{chip="platform_nct6775_2560",sensor="temp2"} 27.5
node_hwmon_temp_celsius{chip="platform_nct6775_2560",sensor="temp3"} 37.5
node_hwmon_temp_celsius{chip="platform_nct6775_2560",sensor="temp7"} 0
node_hwmon_temp_celsius{chip="platform_nct6775_2560",sensor="temp8"} 21
node_hwmon_temp_celsius{chip="platform_nct6775_2560",sensor="temp9"} 38
node_hwmon_temp_celsius{chip="thermal_thermal_zone0",sensor="temp0"} 27.8
node_hwmon_temp_celsius{chip="thermal_thermal_zone0",sensor="temp1"} 27.8
node_hwmon_temp_celsius{chip="thermal_thermal_zone0",sensor="temp2"} 29.8
node_hwmon_temp_celsius{chip="thermal_thermal_zone2",sensor="temp0"} 22
node_hwmon_temp_celsius{chip="thermal_thermal_zone2",sensor="temp1"} 22
# HELP node_hwmon_temp_crit_alarm_celsius Hardware monitor for temperature (crit_alarm)
# TYPE node_hwmon_temp_crit_alarm_celsius gauge
node_hwmon_temp_crit_alarm_celsius{chip="platform_coretemp_0",sensor="temp1"} 0
node_hwmon_temp_crit_alarm_celsius{chip="platform_coretemp_0",sensor="temp2"} 0
node_hwmon_temp_crit_alarm_celsius{chip="platform_coretemp_0",sensor="temp3"} 0
node_hwmon_temp_crit_alarm_celsius{chip="platform_coretemp_0",sensor="temp4"} 0
node_hwmon_temp_crit_alarm_celsius{chip="platform_coretemp_0",sensor="temp5"} 0
# HELP node_hwmon_temp_crit_celsius Hardware monitor for temperature (crit)
# TYPE node_hwmon_temp_crit_celsius gauge
node_hwmon_temp_crit_celsius{chip="platform_coretemp_0",sensor="temp1"} 100
node_hwmon_temp_crit_celsius{chip="platform_coretemp_0",sensor="temp2"} 100
node_hwmon_temp_crit_celsius{chip="platform_coretemp_0",sensor="temp3"} 100
node_hwmon_temp_crit_celsius{chip="platform_coretemp_0",sensor="temp4"} 100
node_hwmon_temp_crit_celsius{chip="platform_coretemp_0",sensor="temp5"} 100
node_hwmon_temp_crit_celsius{chip="platform_nct6775_2560",sensor="temp9"} 100
# HELP node_hwmon_temp_max_celsius Hardware monitor for temperature (max)
# TYPE node_hwmon_temp_max_celsius gauge
node_hwmon_temp_max_celsius{chip="platform_coretemp_0",sensor="temp1"} 100
node_hwmon_temp_max_celsius{chip="platform_coretemp_0",sensor="temp2"} 100
node_hwmon_temp_max_celsius{chip="platform_coretemp_0",sensor="temp3"} 100
node_hwmon_temp_max_celsius{chip="platform_coretemp_0",sensor="temp4"} 100
node_hwmon_temp_max_celsius{chip="platform_coretemp_0",sensor="temp5"} 100
node_hwmon_temp_max_celsius{chip="platform_nct6775_2560",sensor="temp1"} 80
node_hwmon_temp_max_celsius{chip="platform_nct6775_2560",sensor="temp2"} 80
node_hwmon_temp_max_celsius{chip="platform_nct6775_2560",sensor="temp3"} 80
node_hwmon_temp_max_celsius{chip="platform_nct6775_2560",sensor="temp7"} 0
node_hwmon_temp_max_celsius{chip="platform_nct6775_2560",sensor="temp8"} 80
node_hwmon_temp_max_celsius{chip="platform_nct6775_2560",sensor="temp9"} 80
# HELP node_hwmon_temp_max_hyst_celsius Hardware monitor for temperature (max_hyst)
# TYPE node_hwmon_temp_max_hyst_celsius gauge
node_hwmon_temp_max_hyst_celsius{chip="platform_nct6775_2560",sensor="temp1"} 75
node_hwmon_temp_max_hyst_celsius{chip="platform_nct6775_2560",sensor="temp2"} 75
node_hwmon_temp_max_hyst_celsius{chip="platform_nct6775_2560",sensor="temp3"} 75
node_hwmon_temp_max_hyst_celsius{chip="platform_nct6775_2560",sensor="temp7"} 0
node_hwmon_temp_max_hyst_celsius{chip="platform_nct6775_2560",sensor="temp8"} 75
node_hwmon_temp_max_hyst_celsius{chip="platform_nct6775_2560",sensor="temp9"} 75
# HELP node_hwmon_temp_offset_celsius Hardware monitor for temperature (offset)
# TYPE node_hwmon_temp_offset_celsius gauge
node_hwmon_temp_offset_celsius{chip="platform_nct6775_2560",sensor="temp1"} 0
node_hwmon_temp_offset_celsius{chip="platform_nct6775_2560",sensor="temp2"} 0
node_hwmon_temp_offset_celsius{chip="platform_nct6775_2560",sensor="temp3"} 0
# HELP node_hwmon_temp_type Hardware monitor temp element type
# TYPE node_hwmon_temp_type gauge
node_hwmon_temp_type{chip="platform_nct6775_2560",sensor="temp1"} 4
node_hwmon_temp_type{chip="platform_nct6775_2560",sensor="temp2"} 4
node_hwmon_temp_type{chip="platform_nct6775_2560",sensor="temp3"} 4
```