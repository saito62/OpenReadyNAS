#OpenReadyNAS
An open-source reverse engineering and modernization project for the Netgear ReadyNAS Ultra 2. The goal is to document the original hardware, reverse engineer its electronics, develop open-source replacement PCBs designed in KiCad, and ultimately replace the original motherboard with a custom-designed interface board for a modern SBC, ideally the FriendlyElec CM3588 based on the Rockchip RK3588.
Current Goals
The project currently focuses on reverse engineering the original hardware to gain a complete understanding of the ReadyNAS Ultra 2 architecture before designing compatible replacement hardware.
SATA Backplane
The SATA backplane is the first reverse engineering target and serves as an introduction to the overall system. The goals are to:
	• Reverse engineer the complete schematic
	• Document the edge connector pinout
	OpenReadyNAS
	An open-source reverse engineering and modernization project for the Netgear ReadyNAS Ultra 2. The goal is to document the original hardware, reverse engineer its electronics, develop open-source replacement PCBs designed in KiCad, and ultimately replace the original motherboard with a custom-designed interface board for a modern SBC, ideally the FriendlyElec CM3588 based on the Rockchip RK3588.
	

	Current Goals
	The project currently focuses on reverse engineering the original hardware to gain a complete understanding of the ReadyNAS Ultra 2 architecture before designing compatible replacement hardware.
	SATA Backplane
	The SATA backplane is the first reverse engineering target and serves as an introduction to the overall system. The goals are to:
		• Reverse engineer the complete schematic
		• Document the edge connector pinout
		• Verify SATA signal routing and power distribution
		• Design a fully compatible interface PCB in KiCad as an intermediate step before integrating its functionality into the new motherboard
	Rear I/O Daughterboard
	The second—and significantly more challenging—target is the rear I/O daughterboard, which contains most of the external interfaces. The goals are to:
		• Reverse engineer the complete schematic
		• Document the PCIe edge connector pinout
		• Reverse engineer the dual Gigabit Ethernet implementation
		• Document both USB 2.0 ports
		• Document the serial header
		• Reverse engineer the power and button circuitry
		• Reverse engineer the 3-pin fan control circuitry
		• Design a fully compatible interface PCB in KiCad as an intermediate step before integrating its functionality into the new motherboard
	

	PCB Design
	All replacement hardware developed as part of this project will be designed in KiCad. The complete design files—including schematics, PCB layouts, libraries, fabrication files, and supporting documentation—will be published in this repository, allowing anyone to study, reproduce, improve, or manufacture the hardware. The documentation and designs may also serve as a foundation for developing similar replacement hardware for other ReadyNAS models.
	

	Target SBC Platform
	The primary target platform for this project is the FriendlyElec CM3588 based on the Rockchip RK3588, as it offers an excellent balance of processing power, PCIe connectivity, and I/O capabilities for a modern NAS while maintaining a compact form factor.
	However, the project will remain as platform-independent as practical. If integrating the CM3588 proves significantly more complex than anticipated due to limited documentation, hardware limitations, or development effort, the design may instead target a more widely adopted Compute Module platform, such as the Raspberry Pi Compute Module 5 (CM5) or the Radxa CM5. These platforms benefit from extensive documentation, larger developer communities, and many existing open-source hardware examples, which could considerably simplify development while still fulfilling the project's primary objectives.
	

	Long-Term Goal
	The ultimate objective is to replace the original ReadyNAS Ultra 2 motherboard with a custom-designed interface board while preserving the original enclosure, drive backplane, rear I/O daughterboard, front-panel functionality, and overall appearance.
	The replacement motherboard is intended to interface with a modern SBC while reusing as much of the original hardware as practical. Planned improvements include:
		• Reusing the original rear I/O daughterboard
		• Upgrading the original dual Gigabit Ethernet ports to dual 2.5 GbE
		• Adding an M.2 expansion slot for future storage or PCIe peripherals
		• Maintaining compatibility with the original drive bays, cooling solution, LEDs, buttons, and overall form factor
The long-term vision is to create a modern, open-source hardware platform that preserves the iconic ReadyNAS Ultra 2 while significantly extending its performance, functionality, and lifespan.
