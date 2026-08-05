# OpenReadyNAS

> An open-source reverse engineering and modernization project for the **Netgear ReadyNAS Ultra 2**.

The goal of this project is to document the original hardware, reverse engineer its electronics, develop open-source replacement PCBs designed in **KiCad**, and ultimately replace the original motherboard with a custom-designed replacement motherboard for a modern SBC, ideally the **FriendlyElec CM3588** based on the **Rockchip RK3588**.

<p align="center">
  <img src="https://github.com/user-attachments/assets/3a4bba27-9bb3-4cd5-924b-e44129a4b44f" width="700" alt="Netgear ReadyNAS Ultra 2">
</p>

---

## Current Goals

The project currently focuses on reverse engineering the original hardware to gain a complete understanding of the ReadyNAS Ultra 2 architecture before designing compatible replacement hardware.

### SATA Backplane

The SATA backplane is the first reverse engineering target and serves as an introduction to the overall system.

**Objectives**

* [ ] Reverse engineer the complete schematic
* [ ] Document the edge connector pinout
* [ ] Verify SATA signal routing and power distribution
* [ ] Design a fully compatible interface PCB in **KiCad**
* [ ] Integrate the design into the replacement motherboard

---

### Rear I/O Daughterboard

The second—and significantly more challenging—target is the rear I/O daughterboard, which contains most of the external interfaces.

**Objectives**

* [ ] Reverse engineer the complete schematic
* [ ] Document the PCIe edge connector pinout
* [ ] Reverse engineer the dual Gigabit Ethernet implementation
* [ ] Document both USB 2.0 ports
* [ ] Document the serial header
* [ ] Reverse engineer the power and button circuitry
* [ ] Reverse engineer the 3-pin fan control circuitry
* [ ] Design a fully compatible interface PCB in **KiCad**
* [ ] Integrate the design into the replacement motherboard

---

## PCB Design

All replacement hardware developed as part of this project will be designed in **KiCad**.

The complete design files—including

* Schematics
* PCB layouts
* Libraries
* Manufacturing files (Gerbers)
* BOMs
* Supporting documentation

will be published in this repository, allowing anyone to study, reproduce, improve, or manufacture the hardware.

The documentation and PCB designs are also intended to serve as a foundation for similar replacement projects for other ReadyNAS models.

---

## Target SBC Platform

The primary target platform is the **FriendlyElec CM3588** based on the **Rockchip RK3588**, offering an excellent balance of CPU performance, PCIe connectivity, and I/O capabilities for a modern NAS.

However, the project will remain as platform-independent as practical.

If integrating the CM3588 proves significantly more complex than anticipated due to limited documentation, hardware limitations, or development effort, the design may instead target a more widely adopted Compute Module platform such as the:

* Raspberry Pi Compute Module 5 (CM5)
* Radxa CM5

These platforms benefit from extensive documentation, larger developer communities, and many existing open-source hardware examples while still fulfilling the project's primary objectives.

---

## Long-Term Goal

The ultimate objective is to replace the original ReadyNAS Ultra 2 motherboard with a custom-designed replacement motherboard while preserving the original enclosure, drive backplane, rear I/O daughterboard, front-panel functionality, and overall appearance.

The new motherboard is planned to provide:

* ✅ Support for a modern Compute Module
* ✅ Reuse of the original rear I/O daughterboard
* ✅ Dual **2.5 GbE** networking
* ✅ M.2 expansion slot
* ✅ Compatibility with the original drive backplane
* ✅ Compatibility with the original cooling solution
* ✅ Compatibility with the original LEDs and buttons
* ✅ Original mechanical form factor

The long-term vision is to create a modern, open-source hardware platform that preserves the iconic ReadyNAS Ultra 2 while significantly extending its performance, functionality, and lifespan.
