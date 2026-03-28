# Output Doubler – Audio Duplication / Routing Tool

**Developer:** Burak Bozteke  
**Platform:** Windows 10 (2004+)

---

## What Does the Program Do?

This program allows you to route the audio of applications on your computer  
to a secondary audio output device simultaneously, alongside your default audio device.

Additionally, you can route an input device (such as a microphone) directly  
to the selected secondary output device.

### Example Usage Scenarios

- Hearing an application's audio from both headphones and speakers at the same time  
- Routing a music player to a separate sound card  
- Cloning game audio to a different output device  
- Routing your microphone to a different sound card or virtual output  

**Important:**  
This program **copies** the audio, it does not move it.  
The application continues to play audio from the default device; the program only forwards  
the same audio to the secondary device you selected.

---

## System Requirements

- Windows 10 version 2004 (May 2020 Update) or higher  
- At least **2 audio output devices** (headphones + speakers, USB DAC, etc.)

---

## How to Use

### 1. Run the Program

Double-click the `OutputDoubler.exe` file.

- The program runs as a **single instance**  
- Opening it again brings the existing window to the front  

---

### 2. Select Secondary Output Device

From the **"Secondary Output Device"** dropdown:

- Select the device you want to route audio to  

**Note:**  
The device marked with `[DEFAULT]` is the Windows default device.  
You cannot select it because audio is already playing there.

---

### 3. Select Applications

The list shows applications currently playing audio.

- ✓ Checked → Routing starts (audio duplicated)  
- ☐ Unchecked → Routing stops  

---

### 4. Monitor Routing

Enable **"Monitor Routing"**

- Lets you hear routed audio from your default device as well  
- Activates only when at least one routing is active  

---

### 5. Input Routing (Microphone)

- Select a device from **"Input Device"**  
- Enable **"Route Input to Output"**  

To refresh input devices:

- Use the **Refresh** button next to the input list  

---

### 6. Refreshing the List

Lists update automatically in the background.

Manual refresh options:

- Press **Refresh (F5)**  
- Press **F5**

**Important:**  
Manual refresh stops all active routings.

---

### 7. Background Tracking & Auto-Route

- If a routed app closes → routing stops automatically  
- If an input device disconnects → safely removed  
- Prevents crashes and stale entries  

Enable **"Auto-Route New Apps"**:

- Newly opened audio apps are automatically routed  

---

### 8. Changing Devices

When selecting a different output device:

- All routings stop  
- All selections reset  

You must re-select applications.

---

### 9. System Tray

- Program can minimize to system tray  
- Right-click tray icon:

  - **Restore**  
  - **Exit**

---

## Status Bar

Located at the bottom:

- `Ready. No active routing.` → Idle state  
- `Active routing: X` → X apps currently routed  

---

## Keyboard Shortcuts

| Key   | Function                    |
|-------|---------------------------|
| F5    | Refresh lists             |
| Tab   | Navigate UI               |
| Space | Toggle selected checkbox  |

---

## Frequently Asked Questions

### Program does not open

Make sure you're using **Windows 10 2004 or newer**.  
The app depends on the **Process Loopback API**.

---

### Application not listed

- The app must be actively playing audio  
- Start playback and press **F5**

---

### Audio delay

- Expected latency: **~20 ms**  
- Rare hardware-based delays may occur  

---

### Cannot select default device

- This is intentional  
- Audio already plays there  
- Select a different device  

---

## License

© 2026 Burak Bozteke  
All rights reserved.