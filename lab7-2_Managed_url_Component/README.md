# Lab 7-2: Managed Component from GitHub URL Demo

## คำอธิบาย
การทดลองนี้แสดงการใช้งาน managed component จาก GitHub Repository
ใช้ `Sensors` component จาก https://github.com/APPLICATIONS-OF-MICROCONTROLLERS/Lab7_Components

## ผลลัพธ์ที่คาดหวัง
- แสดงข้อความการเริ่มต้น sensor จาก GitHub component
- แสดงข้อมูล temperature และ humidity ทุก 4 วินาที
- แสดงสถานะการทำงานของ sensor
- แสดงแหล่งที่มาของ component (GitHub Repository)

## ความแตกต่างจาก Lab 7-1
- Lab 7-1: ใช้ local component (ในเครื่อง)
- Lab 7-2: ใช้ managed component จาก GitHub URL

## การใช้งาน
1. เข้าไปในโฟลเดอร์ lab7-2_Managed_url_Component
2. รันคำสั่ง `idf.py build` (จะดาวน์โหลด component จาก GitHub อัตโนมัติ)
3. ทดสอบด้วย QEMU

I (3653) boot: Loaded app from partition at offset 0x10000
I (3654) boot: Disabling RNG early entropy source...
I (3726) cpu_start: Multicore app
I (7010) cpu_start: Pro cpu start user code
I (7011) cpu_start: cpu freq: 160000000 Hz
I (7012) app_init: Application information:
I (7012) app_init: Project name:     lab7-2
I (7012) app_init: App version:      1
I (7012) app_init: Compile time:     Aug 13 2025 03:25:27
I (7012) app_init: ELF file SHA256:  aac72780c...
I (7013) app_init: ESP-IDF:          v6.0-dev-1002-gbfe5caf58f
I (7013) efuse_init: Min chip rev:     v0.0
I (7013) efuse_init: Max chip rev:     v3.99 
I (7013) efuse_init: Chip rev:         v3.0
I (7014) heap_init: Initializing. RAM available for dynamic allocation:
I (7015) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (7016) heap_init: At 3FFB2EA8 len 0002D158 (180 KiB): DRAM
I (7016) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (7016) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (7016) heap_init: At 4008D000 len 00013000 (76 KiB): IRAM
I (7086) spi_flash: detected chip: winbond
I (7098) spi_flash: flash io: dio
I (7118) main_task: Started on CPU0
I (7128) main_task: Calling app_main()
I (7128) LAB7-2: 🚀 Lab 7-2: Managed Component from GitHub URL Demo Started
I (7128) LAB7-2: 📥 Using Sensors component from: https://github.com/APPLICATIONS-OF-MICROCONTROLLERS/Lab7_Components
I (7128) SENSOR: 🔧 Sensor initialized from file: ./managed_components/lab7_components/Sensors/sensor.c, line: 12
I (7128) SENSOR: 📡 Sensor module ready for operation
I (7128) LAB7-2: 📋 Reading #1 from GitHub Component
I (7128) SENSOR: 📊 Reading sensor data from file: ./managed_components/lab7_components/Sensors/sensor.c, line: 18
I (7138) SENSOR: 🌡️  Tempera ture: 34.2°C
I (7148) SENSOR: 💧 Humidity: 82.3%
I (7148) SENSOR: ✅ Sensor status check from file: ./managed_components/lab7_components/Sensors/sensor.c, line: 30
I (7148) SENSOR: 📈 All sensors operating normally
I (7148) LAB7-2: � Component Source: GitHub Repository
I (7148) LAB7-2: ==========================================
I (11148) LAB7-2: 📋 Reading #2 from GitHub Component
I (11148) SENSOR: 📊 Reading sensor data from file: ./managed_components/lab7_components/Sensors/sensor.c, line: 18
I (11148) SENSOR: 🌡️  Temper ature: 29.9°C
I (11148) SENSOR: 💧 Humidity: 72.5%
I (11148) SENSOR: ✅ Sensor status check from file: ./managed_components/lab7_components/Sensors/sensor.c, line: 30
I (11148) SENSOR: 📈 All sensors operating normally
I (11148) LAB7-2: � Component Source: GitHub Repository
I (11148) LAB7-2: ==========================================
I (15148) LAB7-2: 📋 Reading #3 from GitHub Component
I (15148) SENSOR: 📊 Reading sensor data from file: ./managed_components/lab7_components/Sensors/sensor.c, line: 18
I (15148) SENSOR: 🌡️  Temperature:  29.7°C
I (15148) SENSOR: 💧 Humidity: 80.7%
I (15148) SENSOR: ✅ Sensor status check from file: ./managed_components/lab7_components/Sensors/sensor.c, line: 30
I (15148) SENSOR: 📈 All sensors operating normally
I (15148) LAB7-2: � Component Source: GitHub Repository
I (15148) LAB7-2: ==========================================