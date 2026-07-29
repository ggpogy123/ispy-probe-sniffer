# Journal

## July 28 - Day 1 (2 hrs)

### What I did
Decided on the project, set up the GitHub repo and Wokwi ESP32 project, read some documentation and about wifi probe requests 
and wrote the project description.

### Why I picked this project
I was planning on choosing between a network traffic analyzer, a GPS tracker and a 
WiFi probe sniffer. The probe sniffer felt the most spy like
because it requires no network connection at all, it's completely passive 
and the target has no idea it's happening.

### What I learned
Didn't realize phones constantly broadcast the SSIDs of every network they've ever connected to, 
I thought this only happened when you turned on WiFi or refreshed it from the settings app or maybe using geolocation.
Turns out it happens every few seconds automatically.

Read through these to understand how it works:
- [ESP32 WiFi API](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-guides/wifi.html)
- [ESP32 Promiscuous Mode](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-reference/network/esp_wifi.html)
  
- [WiFi Probe Requests — Wikipedia](https://en.wikipedia.org/wiki/Probe_request)

### Screenshots
<img width="2559" height="1473" alt="image" src="https://github.com/user-attachments/assets/2e62fd50-68b4-47f6-8d01-58eacb8c7051" />
<img width="2559" height="1445" alt="image" src="https://github.com/user-attachments/assets/793581fd-4695-4784-a19c-8e0b44f90c0a" />





### Problems
Nothing till now as i'm also using AI to make me understand wherever i get stuck.


---

## July 29 - Day 2 (1.5 hrs)

### What I did
I set up the environment on Wokwi and initialized the WiFi adapter in promiscuous mode using `esp_wifi` APIs. I also verified serial output to make sure the board boots and enters promiscuous mode nicely.


### What I learned
Standard WiFi connection modes require joining an Access Point, but promiscuous mode allows the ESP32 radio antenna to passively capture raw 802.11 packets floating around on the set channel without authenticating to any network.

### Documentation followed:
- [ESP-IDF WiFi Promiscuous Mode](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-reference/network/esp_wifi.html#promiscuous-mode)

### Screenshots
<img width="2559" height="1477" alt="image" src="https://github.com/user-attachments/assets/8959bab3-68d7-49f9-bb8b-1f33b94c532a" />


### Problems
Wokwi can't simulate this Wi-Fi thing (no actual  devices broadcasting packets in the simulation), so real packets won't trigger automatically in the simulator. Will need to simulate incoming packet data for the same later.
