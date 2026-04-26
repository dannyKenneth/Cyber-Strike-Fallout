# 🌌 CYBER STRIKE: Fallout

**Cyber Strike** is a high-stakes survival simulation where you pilot a data-collection craft through a collapsing digital architecture. As the Overseer, you have the power to "rig" the system integrity, choosing exactly how fast reality de-stabilizes around the pilot.

---

## 🕹️ Controls

### Keyboard & Mouse
* **W / A / S / D**: Fluid 8-way movement.
* **SPACE**: Fire data-disruption bolts.
    * *Note: Manual clicking/tapping is required when stability is critical or rigging is high.*
* **` (Backtick)**: Toggle Admin Command Line Interface (CLI).
* **Shift + \ **: Emergency System Reboot (Hard Reset).

### Analog Joystick / Controller
* **Left Stick**: Full 360-degree analog movement.
* **Button 0 (A/Cross)**: Primary Fire.
* **Start / Select**: Toggle Admin CLI.

---

## 🛠️ Admin CLI (Overseer Commands)

Access the console by pressing **`**. Use these commands to manipulate the simulation in real-time:

| Command | Description | Example |
| :--- | :--- | :--- |
| `help` | Displays the command manifest. | `help` |
| **`rig [%]`** | Sets system rigging from **0 to 100**. | `rig 75` |
| `kill` | Instant purge of all active enemies. | `kill` |
| `spwn [T] [MS]` | Set spawn rate (ms) for Tier 0-3. | `spwn 0 500` |
| `speed [V]` | Overrides base enemy velocity. | `speed 2.5` |
| `time [S]` | Shift the session clock to a specific second. | `time 25` |
| `clear` | Wipes the console log history. | `clear` |

---

## ⚠️ Core Mechanics

### 1. The Rigging Scale (0% - 100%)
The system’s difficulty is non-linear and scales based on the `rig` percentage:
* **0% Rigging**: The "System Overload" wall hits at **30 seconds**. Stability is ignored.
* **100% Rigging**: The "System Overload" wall hits at **10 seconds**. Stability drains rapidly.
* **Hybrid**: Values in between scale the spawn intensity, reload delays, and how early the "wall" appears.

### 2. Link Stability
Visible in the UI as **LINK %**. 
* **Firing**: Rapid fire generates heat. At high rig percentages, this causes your Link to drop.
* **Degradation**: 
    * **< 40%**: Global enemy speed increases by **1.5x**.
    * **< 20%**: Speed increases by **2.5x** and weapons are forced into **Semi-Auto** mode.
    * **0%**: The "Hell Multiplier" activates, spiking speeds and spawn rates to maximum.

### 3. Enemy Tiers
* **Tier 0 (Core)**: Standard tracking units.
* **Tier 1 (ZigZag)**: Erratic horizontal movement.
* **Tier 2 (Pointer)**: High-speed interceptors.
* **Tier 3 (Phantom)**: Spawns a Teleporter. It is **invulnerable** for 3 seconds (Phantom Lock). You have a 1-second window to destroy it once the lock clears before it self-destructs.

---

## 🚀 Installation & Launch

1.  **Environment**: Ensure Python 3.x and `pygame` are installed.
    ```bash
    pip install pygame
    ```
2.  **Assets**: Ensure the `assets/` folder contains:
    * `player.png`, `core.png`, `zigzag.png`, `pointer.png`, `teleporter.png`, `title_bg.png`.
3.  **Execution**: Run the script:
    ```bash
    python main.py
    ```
4.  **Authorization**: Press **SPACE** on the splash screen to initialize the connection.
