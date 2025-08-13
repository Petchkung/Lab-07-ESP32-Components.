# Lab 7-1: Local Component Demo

## คำอธิบาย
การทดลองนี้แสดงการใช้งาน component ที่มีอยู่ในโฟลเดอร์ `components/Sensors/` ของ project


## สรุปคำสั่งที่ใช้ และผลลัพธ์ที่ได้

1. สร้างและเข้าใช้งาน Docker container
docker-compose up -d
docker exec -it esp32-lab7 bash

2. ไปยังไดเรกทอรีของโปรเจค Lab 7-1
cd lab7-1_Managed_Local_Component

3. Export environment สำหรับ ESP-IDF
. $IDF_PATH/export.sh

4. ตั้งค่า Target เป็น esp32
idf.py set-target esp32

5. Build โปรเจค
idf.py build

I (4099) cpu_start: Multicore app
I (7727) cpu_start: Pro cpu start user code
I (7728) cpu_start: cpu freq: 160000000 Hz
I (7729) app_init: Application information:
I (7729) app_init: Project name:     lab7-1
I (7729) app_init: App version:      1
I (7729) app_init: Compile time:     Aug 13 2025 02:50:23
I (7729) app_init: ELF file SHA256:  d8165e088...
I (7730) app_init: ESP-IDF:          v6.0-dev-1002-gbfe5caf58f
I (7730) efuse_init: Min chip rev:     v0.0
I (7730) efuse_init: Max chip rev:     v3.99 
I (7730) efuse_init: Chip rev:         v3.0
I (7731) heap_init: Initializing. RAM available for dynamic allocation:
I (7732) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (7733) heap_init: At 3FFB2EA8 len 0002D158 (180 KiB): DRAM
I (7733) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (7733) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (7733) heap_init: At 4008D000 len 00013000 (76 KiB): IRAM
I (7810) spi_flash: detected chip: winbond
I (7822) spi_flash: flash io: dio
I (7842) main_task: Started on CPU0
I (7852) main_task: Calling app_main()
I (7852) LAB7-1: 🚀 Lab 7-1: Local Component Demo Started
I (7852) SENSOR: 🔧 Sensor initialized from file: /project/components/Sensors/sensor.c, line: 12
I (7852) SENSOR: 📡 Sensor module ready for operation
I (7852) SENSOR: 📊 Reading sensor data from file: /project/components/Sensors/sensor.c, line: 18
I (7852) SENSOR: 🌡️  Temperature : 34.5°C
I (7862) SENSOR: 💧 Humidity: 99.4%
I (7872) SENSOR: ✅ Sensor status check from file: /project/components/Sensors/sensor.c, line: 30
I (7872) SENSOR: 📈 All sensors operating normally
I (7872) LAB7-1: ----------------------------
I (10872) SENSOR: 📊 Reading sensor data from file: /project/components/Sensors/sensor.c, line: 18
I (10872) SENSOR: 🌡️  Temperature: 31.3°C
I (10872) SENSOR: 💧 Humidity: 88.4%
I (10872) SENSOR: ✅ Sensor status check from file: /project/components/Sensors/sensor.c, line: 30
I (10872) SENSOR: 📈 All sensors operating normally
I (10872) LAB7-1: ----------------------------
I (13872) SENSOR: 📊 Reading sensor data from file: /project/components/Sensors/sensor.c, line: 18
I (13872) SENSOR: 🌡️  Temperature: 31.6°C
I (13872) SENSOR: 💧 Humidity: 92.0%
I (13872) SENSOR: ✅ Sensor status check from file: /project/components/Sensors/sensor.c, line: 30
I (13872) SENSOR: 📈 All sensors operating normally
I (13872) LAB7-1: ----------------------------
I (16872) SENSOR: 📊 Reading sensor data from file: /project/components/Sensors/sensor.c, line: 18
I (16872) SENSOR: 🌡️  Tempe rature: 32.1°C
I (16872) SENSOR: 💧 Humidity: 85.4%
I (16872) SENSOR: ✅ Sensor status check from file: /project/components/Sensors/sensor.c, line: 30
I (16872) SENSOR: 📈 All sensors operating normally
I (16872) LAB7-1: ----------------------------
I (19872) SENSOR: 📊 Reading sensor data from file: /project/components/Sensors/sensor.c, line: 18
I (19872) SENSOR: 🌡️  Temperature: 35.0°C
I (19872) SENSOR: 💧 Humidity: 72.6%
I (19872) SENSOR: ✅ Sensor status check from file: /project/components/Sensors/sensor.c, line: 30
I (19872) SENSOR: 📈 All sensors operating normally
I (19872) LAB7-1: ----------------------------
I (22872) SENSOR: 📊 Reading sensor data from file: /project/components/Sensors/sensor.c, line: 18
I (22872) SENSOR: 🌡️  Temperature: 27.4°C
I (22872) SENSOR: 💧 Humidity: 92.7%
I (22872) SENSOR: ✅ Sensor status check from file: /project/components/Sensors/sensor.c, line: 30
I (22872) SENSOR: 📈 All sensors operating normally
I (22872) LAB7-1: ----------------------------