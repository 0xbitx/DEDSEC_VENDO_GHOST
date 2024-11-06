
<p align="center">
<img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExaXlwY2ttZ2duZW5nc2kxZDI1bjRpYTExZWN2aXkzOGt0M2VpYmhpZCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/xwgABNX9ikRq5lbgMU/giphy.webp" width="30%" height="30%">
</p>

<h1 align="center"> DEDSEC_VENDO_GHOST </h1>

## DESCRIPTION
Vendo Ghost is a powerful Wi-Fi Vendo disruption tool designed to help Wi-Fi vendors improve the number of clients connected to their networks by silently interfering with nearby competitor networks. The tool targets competing Wi-Fi vendors by sending deauthentication frames to their clients, effectively disconnecting them for brief periods while keeping the attack stealthy and undetectable.

### Scenario

Imagine you run a Wi-Fi Vendo Machine, providing internet access to nearby clients. However, your competitor's Wi-Fi Vendo Machine is located near yours and attracts more clients due to better connectivity or other factors. Vendo Ghost solves this issue by subtly interfering with your competitor's Vendo Machine, causing clients to experience intermittent disconnections. Over time, this "connection instability" will encourage clients to switch to your more stable network.


### How It Works
  * Stealth Deauthentication Attacks: Vendo Ghost sends deauth frames to your competitor's Vendo clients. These frames disconnect the clients for short moments, causing them to believe there are connectivity issues with their router or that they are outside the router's range.
  
  * Small, Timed Interruptions: The deauth frames are sent at timed intervals—short enough to not raise suspicion but long enough to cause disconnections. The reconnections between deauth attacks create the illusion of network instability or range issues.
  
  * Stealth Operation: The tool is designed to operate without detection, using minimal disruption to avoid triggering alarms or suspicion from the competitor’s side.
  
  * Long-term Effect: Over time, the consistent disruption leads to many clients switching to your Wi-Fi Vendo, as they experience better reliability and performance. As more clients choose your Vendo, you gain an advantage over your competitor's network.
  
  * Compact and Stealthy ESP32 Implementation: Vendo Ghost operates on a small ESP32 device, which can be discreetly installed inside your Wi-Fi Vendo hardware. The ESP32 allows the tool to run autonomously and stealthily, without requiring an additional computer or device, and ensures that the operation remains covert, with minimal power consumption and a small form factor.
  
  * BSSID-Driven Attack Persistence: The tool requires the SSID and BSSID of the target Vendo. Even if the competitor changes the AP's SSID, the BSSID remains constant and allows the tool to continue the attack. As long as the target BSSID is active, Vendo Ghost will persistently send deauth frames, keeping the attack going until the competitor changes their AP entirely.

### Variables need to setup 
    target_ssid = "test_wifi_vendo" // Competitor's Vendo SSID
    target_bssid = "00:00:00:00:00:00" // Competitor's Vendo BSSID
    frame_send = 5 // Number of frames to send to disconnect the client and allow immediate reconnection
    attack_delay = 120 // Delay before starting the attack. You can increase this to avoid suspicion 

## Usage
    Install: Follow the installation instructions to set up the tool.
    first ready your esp32 (antenna) 
    contact me for your firmware prefer your target ssid and bssid 
    Open the webflasher: https://dedsec_vendo_ghost
    if your done flashing your firmware get ready to setup your vendo_ghost device to your Wifi vendo machine via usb cable
    Launch the Tool: Start the tool to begin sending magic and causing minimal disruption to your competitor’s clients.
    Monitor the Results: Over time, you will notice more clients choosing your Vendo network due to the perceived instability of your competitor's.

## Support

If you find my work helpful and want to support me, consider making a donation. Your contribution will help me continue working on open-source projects.

**Bitcoin Address: `36ALguYpTgFF3RztL4h2uFb3cRMzQALAcm`**


<h1 align="center"> DISCLAIMER </h1>

<h4 align="center">I'm not responsible for anything you do with this program, so please only use it for good and educational purposes. </h4>

With Vendo Ghost, you can enhance your Wi-Fi Vendo business by gaining more clients through a clever and subtle disruption of your competitor's network. Let the ghost work its magic silently and watch your clients grow!
