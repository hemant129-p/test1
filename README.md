# test1

This is my first repository on GitHub.

## About Me

I am an **Embedded Firmware Developer** with a focus on low-level software development for microcontrollers and embedded systems.

## Current Project: Differential FOTA on TI C2000 Series MCU

I am currently working on **Differential Firmware Over-The-Air (FOTA)** updates targeting the **Texas Instruments C2000 series** of microcontrollers.

### What is Differential FOTA?

Differential FOTA (Firmware Over-The-Air) is a technique for updating device firmware by transmitting only the **binary difference (delta/patch)** between the old firmware and the new firmware, rather than sending the full firmware image. This approach offers significant advantages for embedded systems:

- **Reduced transmission size** – Only the changed bytes are sent, saving bandwidth and time.
- **Lower flash wear** – Fewer write operations extend the lifetime of flash memory.
- **Faster updates** – Smaller payloads mean quicker OTA transfer and flashing cycles.
- **Suitable for constrained devices** – Ideal for MCUs with limited RAM, flash, and communication bandwidth.

### TI C2000 Series MCU

The [TI C2000 series](https://www.ti.com/microcontrollers-mcus/c2000-real-time-control-mcus/overview.html) are 32-bit real-time microcontrollers optimized for control applications such as:

- Motor drives and power conversion
- Solar inverters and industrial automation
- Digital power supplies

Key features relevant to FOTA on C2000:

- Internal flash memory with sector-based erase/write
- On-chip bootloader (Boot ROM) supporting various communication interfaces (SCI, SPI, CAN, etc.)
- Dual-core variants (e.g., TMS320F2837xD) enabling safe in-field updates

### Project Goals

- [ ] Implement a binary diff/patch algorithm suitable for C2000 flash constraints
- [ ] Develop a bootloader capable of applying differential patches in-place
- [ ] Validate update integrity using CRC/checksum verification
- [ ] Support rollback in case of a failed update
- [ ] Optimize for minimal RAM usage during patch application
