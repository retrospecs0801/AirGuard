# 🌍AirGuard  
*Real-Time Air Quality Monitoring & Alert System*
Even in the same city, people experience different pollution exposure. Someone who spends more time outdoors breathes far more polluted air than someone mostly indoors. <br>
*AirGuard tracks every outdoor session using geofencing and combines duration × live AQI to calculate each user’s personal exposure score.*<br>
This app helps users understand how much polluted air they personally breathe every day using live AQI data and geofencing.  
At the end of the day, the app also generates a personalized recovery plan (breathing + diet suggestions) using the Gemini API.

---

## 📚Table of Contents  
- [Features](#features)
- [Tech Stack & Dependencies](#tech-stack--dependencies)  
- [Installation & Setup](#installation--setup)  
- [How the App Works](#how-the-app-works)  
- [Directory Structure](#directory-structure)

---


## 🧩Features

### *1. Real-Time AQI Tracking*
- Fetches live AQI from OpenAQ API  
- Shows current AQI and PM2.5 around the user  



### *2. Outdoor Exposure Timer*
- User sets home location  
- Geofence detects when user leaves/enters home  


Exposure = Time Outside × AQI




### *3. Daily Exposure Summary*
Displays:  
1. Today’s time outdoors  
2. Average AQI  
3. Total exposure score  



### *4. Auto generated recovery plan*
 1. Score 0–100 → Low (Simple breathing exercises (2–3 guided breathing rounds))<br>
 2. Score 101–250 → Moderate (Recovery: Hydration + light movement (1 hydration action + 2 light movements / stretches))<br>
 3. Score 251–400 → High (Mask + avoid exposure + diet + breathing (mask reminder, 2 dietary tips, 1 breathing + light indoor activity))<br>
 4. Score 400 → Critical (Doctor recommendation + immediate actions (call-to-action, emergency tips, reduce exposure now))<br>

---

## 💻Tech Stack & Dependencies 

### Tech Stack
1. Flutter for framework<br>
2. Dart for Language

### Dependencies
geolocator – For live GPS tracking and geofencing<br>
WAQI API – For live AQI and PM2.5 data

---

## 📥Installation & Setup  
Download Flutter SDK<br>
Configure System Environment Variables<br>
Install Android studio<br>
Set up Android Studio for Flutter<br>
Accept Android Licenses / Configure SDK<br>
Verify Installation — Run flutter doctor<br>
Create a New Flutter Project<br>
and
### *1. Clone the repository*
bash
git clone https://github.com/retrospecs0801/AirGuard.git
cd AirGuard


---

### *2. Install dependencies*
bash
flutter pub get


---
Set up your wireless device.<br>
and 
### *4. Run the application*
bash
flutter run


## 📱How the app works? 
(refer the video for detailed explaination)
1. Click on the set home buttton.
2. Walk about 15 m away from the location in order to get outside the preset home location
3. Session starts as you get out of the preset home location
4. Once you get back to the home location it will show the total exposure (which is equal to the time outside * AQI of the location.
5. Scroll down to see the recovery option click on it.
6. It shows the solutions to follow according to the level of exposure.
7. Click on the task to start your recovery sesssion.
8. Complete them.
9. YEAH!! you have countered your AQI exposure.

---


## 🗂Directory Structure  

AirGuard/
├── lib
│   ├── models
│   │   ├── exposure_level.dart
│   │   └── recovery_task.dart
│   │
│   ├── recovery
│   │   ├── completion_screen.dart
│   │   ├── guided_breathing.dart
│   │   ├── task_card.dart
│   │   ├── recovery_module.dart
│   │   └── recovery_screen.dart
│   │
│   ├── services
│   │   ├── gemini_service.dart
│   │   ├── exposure_service.dart
│   │   ├── location_service.dart
│   │   ├── pollution_service.dart
│   │   └── storage_service.dart
│   │
│   └── widgets
│       └──
│
└── main.dart
