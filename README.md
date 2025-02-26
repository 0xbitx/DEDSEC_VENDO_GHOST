
<p align="center">
<img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExczk4MjBtZ2g1djdvemZ2dnpob3I3NXQxMmk2ZGxreDMxbm91M2FveiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/9b7RA8UZj2Quad47m0/giphy.webp" width="30%" height="30%">
</p>

<h1 align="center"> DEDSEC_VENDO_GHOST </h1>

## DESCRIPTION
Vendo Ghost is a powerful Wi-Fi Vendo disruption tool designed to help Wi-Fi vendors improve the number of clients connected to their networks by silently interfering with nearby competitor networks. The tool targets competing Wi-Fi vendors by sending deauthentication frames to their clients, effectively disconnecting them for brief periods while keeping the attack stealthy and undetectable.

### Scenario

Imagine you run a Wi-Fi Vendo Machine, providing internet access to nearby clients. However, your competitor's Wi-Fi Vendo Machine is located near yours and attracts more clients due to better connectivity or other factors. Vendo Ghost solves this issue by subtly interfering with your competitor's Vendo Machine, causing clients to experience intermittent disconnections. Over time, this "connection instability" will encourage clients to switch to your more stable network.


### Features
  * Stealth Deauthentication Attacks: Vendo Ghost sends deauth frames to your competitor's Vendo clients. These frames disconnect the clients for short moments, causing them to believe there are connectivity issues with their router or that they are outside the router's range.
  
  * Small, Timed Interruptions: The deauth frames are sent at timed intervals—short enough to not raise suspicion but long enough to cause disconnections. The reconnections between deauth attacks create the illusion of network instability or range issues.
  
  * Stealth Operation: The tool is designed to operate without detection, using minimal disruption to avoid triggering alarms or suspicion from the competitor’s side.
  
  * Long-term Effect: Over time, the consistent disruption leads to many clients switching to your Wi-Fi Vendo, as they experience better reliability and performance. As more clients choose your Vendo, you gain an advantage over your competitor's network.
  
  * Compact and Stealthy ESP32 Implementation: Vendo Ghost operates on a small ESP32 device, which can be discreetly installed inside your Wi-Fi Vendo hardware. The ESP32 allows the tool to run autonomously and stealthily, without requiring an additional computer or device, and ensures that the operation remains covert, with minimal power consumption and a small form factor.
  
  * BSSID-Driven Attack Persistence: The tool requires the SSID and BSSID of the target Vendo. Even if the competitor changes the AP's SSID, the BSSID remains constant and allows the tool to continue the attack. As long as the target BSSID is active, Vendo Ghost will persistently send deauth frames, keeping the attack going until the competitor changes their AP entirely.
  
  * Randomized Delay for Stealth Attack Pattern:
To prevent detection and make the deauthentication attacks appear as natural connectivity issues, Vendo Ghost implements a randomized delay between deauth frame bursts. This delay feature causes interruptions at varied intervals, reducing the likelihood of establishing a predictable pattern that could trigger alarms or prompt investigation.
  
  * Client Discovery: This feature scans the target network to detect if have client connected before launching any attacks. The tool initiates attacks only if client found, preventing unnecessary actions on underutilized networks and optimizing resource usage. This approach ensures that attacks remain stealthy and effective.

  * SSID Unique Name Filtering: This feature ensures that Vendo Ghost continues attacking the competitor's Wi-Fi even if they change their SSID.
    Instead of relying only on exact SSID matches, the system detects a predefined unique identifier in the SSID, combined with keywords like "vendo", "wifi", "machine", or "piso".
    How It Works:
    You define a unique name for your competitor, such as "Razor".
    If the competitor changes their SSID but keeps the unique name, the attack will still detect and target their network.
    The attack is triggered only if the SSID contains both the unique name AND a keyword from the predefined list.

        Example of Detected SSIDs:
    
        If competitor's unique name is "Razor", the following SSIDs will be detected as targets:
    
        vendo Razor → Detected (Contains "Razor" + "vendo")
        Razor wifi → Detected (Contains "Razor" + "wifi")
        Razor vendo → Detected (Contains "Razor" + "vendo")
        Razor vendo Machine → Detected (Contains "Razor" + "vendo", "machine")
        Razor Piso wifi → Detected (Contains "Razor" + "piso", "wifi")
        Razor Piso wifi machine → Detected (Contains "Razor" + "piso", "wifi", "machine")
        Fast Razor vendo machine → Detected (Contains "Razor" + "vendo", "machine")

   * Advanced Kill Switch Feature: A customizable list of "Kill Switch" SSIDs is used to prevent attacks when specific networks are detected nearby.
   If a Kill Switch SSID is found, all attacks are immediately paused, and the device will delay the next scan based on a configurable kill switch delay setting.
   This prevents unwanted disruptions and ensures stealthy operation by avoiding detection in specific situations.
    
## Support hardware (XIAO ESP32 S3) (XIAO ESP32 C3) (ESP32-C3 Super Mini) working
<p align="center">
<img src="https://cdn-reichelt.de/bilder/web/xxl_ws/A300/XIAO_ESP32S3_01.png" width="23%" height="23%">
<img src="https://cdn-reichelt.de/bilder/web/xxl_ws/A300/XIAO_ESP32S3_SEN_04.png" width="23%" height="23%">
</p>
<p align="center">
 <img src="https://github.com/user-attachments/assets/dfd9a538-f70a-4e06-9d53-f47546a33ce0" width="50%" height="50%">
</p>

## Support hardware (ESP32 Dev Kit V1) working
<p align="center">
<img src="https://freesvg.org/img/1666364456Esp32_devkitc_v4.png" width="30%" height="30%">
</p>

## Support hardware (RTL8720DN BW16) coming soon
<p align="center">
<img src="https://github.com/user-attachments/assets/f10fee55-3f3f-46b6-a0ca-87005f0bb052" width="30%" height="30%">
</p>

## Usage
    Installation: 

    1. First, prepare your ESP32 module (an antenna is optional, depending on the target range).
    2. Contact me on Discord (make sure your ESP32 is ready) before reaching out.
    3. will build your custom firmware and send you the custom flasher.

    if your done flashing your firmware get ready to setup your vendo_ghost device to your Wifi vendo machine via usb cable
    and the tool to begin sending magic and causing minimal disruption to your competitor’s clients.
    Monitor the Results: Over time, you will notice more clients choosing your Vendo network due to the perceived instability of your competitor's.

## feature list:
- [x] stealth mode
- [x] 2.4Ghz support
- [x] Change ssid detection
- [x] esp32 s3/c3 support
- [ ] 5 Ghz support
      
## Support

If you find my work helpful and want to support me, consider making a donation. Your contribution will help me continue working on open-source projects.

**Bitcoin Address: `36ALguYpTgFF3RztL4h2uFb3cRMzQALAcm`**


<h1 align="center"> DISCLAIMER </h1>

<h4 align="center">I'm not responsible for anything you do with this program, so please only use it for good and educational purposes. </h4>

With Vendo Ghost, you can enhance your Wi-Fi Vendo business by gaining more clients through a clever and subtle disruption of your competitor's network. Let the ghost work its magic silently and watch your clients grow!
