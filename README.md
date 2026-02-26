# Output Doubler – Audio Duplication / Routing Tool

**Developer:** Burak Bozteke
**Platform:** Windows 10 (2004+)

---

## Overview

**Output Doubler** allows you to duplicate the audio of specific applications to a secondary audio output device while keeping playback on the default device.

This means audio is **copied**, not moved.

The original application continues playing through the default device, and Output Doubler forwards the same audio to another device you choose.

---

## Example Use Cases

* Listen to audio from both **headphones and speakers simultaneously**
* Route a **music player to a separate sound card**
* Duplicate **game audio to another output device**
* Send audio to **streaming, monitoring, or external hardware**

---

## System Requirements

* Windows 10 version 2004 (May 2020 Update) or newer
* Minimum **2 audio output devices**

  * Examples:

    * Headphones
    * Speakers
    * USB DAC
    * HDMI Audio Device

---

## Recommendation: Virtual Audio Device

It is recommended to have a **virtual audio device** installed on your system.

Because Output Doubler requires at least **one additional output device** besides your default device.

If you only have one physical output device, you can install a virtual sound card application to create an extra output.

Example purposes:

* Use as secondary routing device
* Create virtual monitoring paths
* Improve routing flexibility

Examples of virtual audio device software:

* VB-Audio Virtual Cable
* Virtual Audio Cable
* VoiceMeeter Virtual Input

After installation, the virtual device will appear in the **Secondary Output Device** list and can be selected normally.

---

## How to Use

### 1. Run the Program

Launch:

```
OutputDoubler.exe
```

* The program runs as **single instance only**
* Opening again will bring the existing window to front

---

### 2. Select Secondary Output Device

From the dropdown:

**Secondary Output Device**

Select the device you want audio duplicated to.

**Note:**

Device marked with:

```
[DEFAULT]
```

cannot be selected, because audio already plays there.

---

### 3. Select Applications

The application list shows programs **currently playing audio**

Checkbox behavior:

| Action      | Result         |
| ----------- | -------------- |
| ✓ Checked   | Routing starts |
| ☐ Unchecked | Routing stops  |

---

### 4. Monitor Routing

Enable:

```
Monitor Routing
```

This allows you to also hear routed audio locally.

This option activates only when routing is active.

---

### 5. Refresh Application List

If applications open or close:

* Press **Refresh button**
* Or press **F5**

**Important:**

Refresh will stop all active routings.

---

### 6. Change Output Device

When selecting a different device:

* All routings stop automatically
* All checkboxes reset

You must select applications again.

---

## Status Bar

Located at the bottom.

Displays:

**Ready state**

```
Ready. No active routing.
```

**Active state**

```
Active routing: X
```

---

## Keyboard Shortcuts

| Key   | Function                 |
| ----- | ------------------------ |
| F5    | Refresh list             |
| Tab   | Navigate controls        |
| Space | Toggle selected checkbox |

---

## FAQ

### Program does not open

Ensure your Windows version is **2004 or newer**

This software uses the **Windows Process Loopback API**, which is unavailable in older versions.

---

### Application does not appear

Application must be actively playing audio.

Start playback and press **F5**

---

### Audio delay

Expected latency:

```
~20ms
```

Rare hardware-dependent delays may occur.

---

### Cannot select default device

This is intentional.

Routing to the same device is unnecessary.

Select another device.

---

## Technical Notes

* Uses Windows Process Loopback Capture
* Low latency audio duplication
* No virtual drivers required
* No audio quality loss

---

## License

© 2026 Burak Bozteke
All rights reserved.
