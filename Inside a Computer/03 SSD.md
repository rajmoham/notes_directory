# SATA
- Use same SATA ports as hard drives (giving portability)
- But speeds are very slow compared to other SSD types (550 MB/s)
- Cheap and reliable, but not modern
# AHCI
AHCI = Advanced Host Controller Interface
- Manages 1 command queue with 32 tasks at any given time
- SATA drives under the hood runs on AHCI
- AHCI simply is an interface for computers to interact with the SSD
# M.2
- The "physical form factor" -> ie the shape and connector of the drive
- M.2 sticks can be directly inserted into the motherboard of the computer
- Whilst M.2 tells you the connectivity, the technology can vary, so should be checked (either SATA or NVMe)
# PCIe
PCIe = Peripheral Component Interconnect Express
- Has multiple connectivity ports to allow simultaneous data transfer, speeding up access
- PCIe 3.0 with 4 lanes transfers around 3.5 GB/s
- PCIe 4.0 does 7.5 GB/s
- PCIe 5.0 does 14 GB/s
- Due to the higher speeds, this technology is very expensive and has a lot of power usage
- Can also run into bandwidth sharing issues, especially if many devices are being used at once
# NVMe
NVMe = Non-Volatile Memory express
- A modern protocol created specific for SSDs
- Supports 64,000 queues with 64,000 commands each
- Latency of tasks also decreases due to the increased compatibility of the interface
# Summary
Physical Connectivity Types:
- M.2

Technology Types:
- SATA
- NVMe
- PCIe

Connectivity Interface:
- AHCI