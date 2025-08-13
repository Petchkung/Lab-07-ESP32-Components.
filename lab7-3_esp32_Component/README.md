# Lab 7-3: Custom ESP32 Components (Sensor + Display)

## คำอธิบาย
การทดลองนี้แสดงการสร้าง component ใหม่ด้วยคำสั่ง `idf.py create-component`
สร้าง 2 components:
1. **Sensor Component** - อ่านค่า temperature, humidity และคำนวณ heat index
2. **Display Component** - แสดงผลข้อมูลในรูปแบบตาราง

## โครงสร้างโฟลเดอร์หลังใช้ create-component
lab7-3_esp32_Component/
├── CMakeLists.txt
├── components/
│   ├── sensor/
│   │   ├── CMakeLists.txt
│   │   ├── include/
│   │   │   └── sensor.h
│   │   └── sensor.c
│   └── display/
│       ├── CMakeLists.txt
│       ├── include/
│       │   └── display.h
│       └── display.c
├── main/
│   ├── CMakeLists.txt
│   └── lab7-3.c
├── build/
└── README.md

I (3916) boot: Loaded app from partition at offset 0x10000
I (3916) boot: Disabling RNG early entropy source...
I (3985) cpu_start: Multicore app
I (7517) cpu_start: Pro cpu start user code
I (7518) cpu_start: cpu freq: 160000000 Hz
I (7518) app_init: Application information:
I (7518) app_init: Project name:     lab7-3
I (7518) app_init: App version:      1
I (7519) app_init: Compile time:     Aug 13 2025 03:41:41
I (7519) app_init: ELF file SHA256:  ccbe20eaa...
I (7519) app_init: ESP-IDF:          v6.0-dev-1002-gbfe5caf58f
I (7519) efuse_init: Min chip rev:     v0.0
I (7519) efuse_init: Max chip rev:     v3.99 
I (7520) efuse_init: Chip rev:         v3.0
I (7521) heap_init: Initializing. RAM available for dynamic allocation:
I (7522) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (7522) heap_init: At 3FFB2EC8 len 0002D138 (180 KiB): DRAM
I (7522) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (7522) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (7523) heap_init: At 4008D000 len 00013000 (76 KiB): IRAM
I (7588) spi_flash: detected chip: winbond
I (7604) spi_flash: flash io: dio
I (7628) main_task: Started on CPU0
I (7638) main_task: Calling app_main()
I (7638) LAB7-3: � Lab 7-3: Custom Components Demo (sensor + display) Started
I (7638) LAB7-3: 📦 Using components created with idf.py create-component
I (7638) ENHANCED_SENSOR: 🔧 Enhanced Sensor Component initialized
I (7648) ENHANCED_SENSOR: 📍 File: ./components/sensor/sensor.c, Line: 14
I (7648) ENHANCED_SENSOR: ✅ GPIO LED configured on pin 2
I (7648) DISPLAY: 🖥️  Displa y Component initialized
I (7648) DISPLAY: 📍 File: ./components/display/display.c, Line: 11
I (7648) DISPLAY: ✅ Virtual display ready for operation
I (7648) LAB7-3: 📋 Reading #1
I (7648) DISPLAY: 🧹 Display cleared
I (7648) DISPLAY: 
I (7648) ENHANCED_SENSOR: 🌡️  Temperature: 34.30°C
I (7658) ENHANCED_SENSOR: 💧 Humidity: 60.50%
I (7658) LAB7-3: 🔥 Heat Index: 64.55
I (7658) DISPLAY: ┌─────────────────────────────────┐
I (7658) DISPLAY: │        SENSOR DATA DISPLAY      │
I (7658) DISPLAY: ├─────────────────────────────────┤
I (7668) DISPLAY: │ 🌡️  Tempera ture:  34.30°C      │
I (7668) DISPLAY: │ 💧 Humidity:     60.50%       │
I (7668) DISPLAY: │ 🔥 Heat Index:   64.55        │
I (7668) DISPLAY: └─────────────────────────────────┘
I (7668) DISPLAY: ┌─────────────────────────────────┐
I (7668) DISPLAY: │         SYSTEM STATUS           │
I (7668) DISPLAY: ├─────────────────────────────────┤
I (7668) DISPLAY: │ Status: ✅ Comfortable         │
I (7668) DISPLAY: └─────────────────────────────────┘
I (7668) LAB7-3: ==========================================