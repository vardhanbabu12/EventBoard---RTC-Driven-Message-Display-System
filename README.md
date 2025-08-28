# 📟 EventBoard - RTC-Driven Message Display System  

## 📖 Overview  
The **EventBoard** is a real-time, microcontroller-based message display system designed using the **LPC2148 ARM7 microcontroller**. Its primary purpose is to automatically display predefined messages at specific times on a **16x2 LCD screen** with a scrolling effect. The system leverages the **built-in Real-Time Clock (RTC)** of the LPC2148 for accurate timekeeping.  

In addition, the project provides a **secure Admin Mode**, allowing authorized users to edit the system time and manage scheduled messages. This is implemented using an **external interrupt switch**, **keypad**, and **password-protected access**.  

---

## 🌟 Key Features  
- RTC-based scheduling of messages  
- 16x2 LCD display with scrolling  
- 10 predefined messages stored in memory  
- Secure Admin Mode via switch, keypad & password  
- Admin can update RTC time and enable/disable messages  
- LED status indication:  
  - 🟢 Green LED → Active message display  
  - 🔴 Red LED → Idle mode  
- LM35 sensor for real-time temperature monitoring    

---

## ⚙️ Requirements  

### 🔧 Hardware  
- LPC2148 Microcontroller (ARM7)  
- 16x2 LCD Display  
- 4x4 Keypad  
- Green & Red LEDs  
- LM35 Temperature Sensor   
- Power Supply Circuitry  

### 💻 Software  
- Embedded C  
- Keil uVision IDE  
- Flash Magic Programmer  

---

## 🔄 Working Principle  
1. RTC keeps track of time continuously.  
2. When the current time matches a scheduled message:  
   - Message scrolls on LCD.  
   - Green LED turns ON.  
3. If no scheduled message is active:  
   - LCD shows current time & temperature.  
   - Red LED turns ON.  
4. Admin Mode:  
   - Entered via external switch (interrupt).  
   - Access protected by keypad password.  
   - Allows time editing & message selection.  
---
## 📂 Project File Structure & Descriptions
Project Files
│
├── main.c        # Contains initialization, main loop, RTC handling, LCD display, keypad input
├── delay.c       # Delay-related functions (time delays, debounce handling)
├── delay.h       # Header file for delay function declarations
├── defines.h     # Macro definitions (constants, LCD commands, etc.)
├── types.h       # Custom type definitions and structures
├── interrupt.h   # Interrupt service routines and related definitions



---
## 🎯 Applications  

The EventBoard – RTC-Driven Message Display System can be applied in various real-world scenarios, including:  

- **Educational Institutions**  
  - Displaying class schedules, exam notifications, and reminders in classrooms and labs.  
- **Corporate Offices**  
  - Showing meeting reminders, daily announcements, and motivational messages in workspaces.  
- **Hospitals & Clinics**  
  - Displaying patient appointment times, health tips, and emergency alerts.  
- **Railway/Bus Stations**  
  - Announcing arrival and departure times, delay notices, and passenger information.  
- **Libraries**  
  - Reminders for events, return deadlines, and silence notifications.  
- **Factories & Industries**  
  - Worker shift schedules, safety instructions, and production updates.  
- **Community Centers**  
  - Event announcements, activity reminders, and public service messages.  
- **Home Automation**  
  - Personalized reminders, family schedules, and daily inspirational notes.  

This makes the system versatile for **time-driven communication**, **alerts**, and **information broadcasting** in multiple domains.  
