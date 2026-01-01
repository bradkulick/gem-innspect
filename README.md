# Innspect Gem 🕵️‍♂️

**A Gemonade Gem for Counter-Surveillance & Network Privacy.**

This Gem provides specialized tools to detect hidden cameras, identify suspicious devices on a local network, and assess the privacy risks of temporary accommodations (AirBnBs, Hotels).

## 📦 Installation

This Gem is designed for the [Gemonade Framework](https://github.com/bradkulick/gemonade).

```bash
gemonade install bradkulick/gem-innspect
```

## 🧠 Capabilities

*   **Network Sweep:** Scans local subnets for MAC addresses associated with surveillance vendors (Hikvision, Dahua, Espressif).
*   **Virtualization Detection:** Automatically detects if you are running in a restricted container (Crostini/WSL) and switches to passive multicast listening.
*   **Physical Guidance:** Provides checklists for physical searches based on room type.

## 🛠️ The Tool: `innspect_sweep`

This is the unified entry point for all digital discovery. It automatically adapts to your environment.

1.  **Pre-flight Check:** Detects if you are in a virtualized container (Crostini, WSL2, Docker).
2.  **Passive Discovery (Multicast):** Listens for mDNS (Bonjour) and SSDP (UPnP) broadcasts. This works even in many restricted environments.
3.  **Active Discovery (ARP/Ping):** Performs a high-speed sweep of the local subnet (effective only in Native environments).
4.  **Vendor Analysis:** Cross-references all discovered MAC addresses against a database of known surveillance hardware.

## 🚀 Usage

Once installed, launch the Gem:

```bash
gemonade innspect
```

### Standard Operating Procedure

1.  **Run the Sweep:**
    Inside the session, run the unified diagnostic tool:
    ```bash
    innspect_sweep
    ```

2.  **Interpret Results:**
    *   **Native Mode:** Trust the full device list.
    *   **Restricted Mode:** If the scan finds only your gateway, rely heavily on the **Multicast** results (which will be listed separately) and **Physical Inspection**.

3.  **Physical Inspection:**
    If digital tools are blinded, physical search is mandatory.
    *   Smoke Detectors
    *   Alarm Clocks
    *   Vents
    *   Power Adapters

4.  **External Verification:**
    If running in a container, use a host device (Smartphone) to run a network scan (Fing/WiFiman) and feed the results to the AI for analysis.

## 🏗️ Architecture

This Gem follows the **Gemonade Package Standard (GPS)**:
*   `gem.json`: Metadata and dependency triggers.
*   `requirements.txt`: Python dependencies (automatically installed into an isolated `.venv`).
*   `tools/`: Custom Python scripts added to the session `$PATH`.