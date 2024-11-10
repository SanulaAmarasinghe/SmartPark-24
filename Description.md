# Smart Parking System with PowerApps

This repository contains the implementation of a **Smart Parking System** developed using **PowerApps**. The system utilizes **IoT sensors** and an **ESP32** to provide real-time updates on parking spot availability. The availability data is displayed in a mobile application built on PowerApps. Additionally, **RFID scanning** is integrated to identify users, displaying their details in the app.

## Features

- **Real-Time Parking Availability:** The system uses IoT sensors to detect the availability of parking spaces and sends real-time updates to the mobile app.
- **User Identification via RFID:** An RFID scanner is used to identify users. When a user scans their RFID tag, their personal information is retrieved from the cloud and displayed in the app.
- **Motor Control:** The system controls a motor (e.g., a gate or barrier) to allow or deny access to the parking space based on availability.
- **PowerApps Integration:** The mobile app, built using PowerApps, provides an interface for users to view available parking spaces, check their details, and interact with the parking system.

## Technologies Used

- **PowerApps:** For building the mobile application and creating a user-friendly interface.
- **ESP32:** A microcontroller that integrates with IoT sensors and controls a motor for access to the parking space.
- **IoT Sensors:** Used to detect available parking spots, sending real-time data to the cloud and PowerApps.
- **RFID Scanner:** For user identification, retrieving user details from cloud storage upon scanning.
- **Cloud Services:** Used to store parking and user data. Data such as parking spot availability and user information is stored and accessed via cloud services (e.g., Firebase, Google Cloud, or Azure).

## Setup

### Hardware Setup

1. **ESP32 Microcontroller** with the following integrations:
   - **IoT sensors** to detect parking space availability.
   - **Motor control** to operate a gate/barrier for access.
   - **RFID Scanner** for user identification.
   
2. Set up the **IoT sensors** to detect whether a parking space is available or occupied. The sensor data will be sent to the cloud.

3. Integrate the **motor control** (e.g., using a relay or motor driver) to open or close the parking gate based on sensor data.

4. **RFID Scanner** should be connected to the ESP32 to scan users' RFID tags and retrieve their data from cloud storage (e.g., Firebase or a SQL database).

### Cloud Storage Setup

1. Set up **cloud storage** to store:
   - Parking spot availability data.
   - User data associated with each RFID tag.

2. Configure the cloud service (e.g., Firebase, Azure, or Google Cloud) to allow the ESP32 to send data for storage and retrieve user data based on the RFID tag scanned.

### PowerApps Setup

1. Clone this repository to your local machine.

2. **Create a PowerApps app** to:
   - Display the real-time parking spot availability.
   - Show the user's details when an RFID tag is scanned.
   - Control the parking gate motor based on the availability of spots.
   
3. Connect the PowerApps application to your cloud service where parking and user data are stored. Use connectors for Firebase or another cloud provider.

4. Customize the app to meet your specific needs (e.g., layout, data display, user interface).

5. Test the app on your mobile device and ensure it works with the ESP32, sensors, and RFID scanner.

