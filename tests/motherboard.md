# Motherboard Knowledge Test

**Conceptual** 
* Explain the traditional roles of the northbridge and southbridge chipsets. How has this architecture changed in modern motherboards?
* **Describe the function of the following motherboard components:** 
    * BIOS/UEFI
    * VRM (Voltage Regulator Module)
    * PCIe slots
* What is the purpose of the CMOS battery on a motherboard?

**Component Identification**
* **Provide an image of a motherboard layout. Ask the candidate to identify:**
    * CPU socket
    * RAM slots (and type supported - DDR4, DDR5, etc.)
    * M.2 slots
    * SATA ports 
    * Expansion slots (PCIe x16, x4, etc.)

**Practical/Troubleshooting**
* List factors to consider when choosing a motherboard for a specific CPU.
* Describe the typical steps involved in the POST (Power-On Self-Test) process during a computer boot-up.
* A user's computer fails to turn on. What motherboard-related issues could be the cause, and how would you begin diagnosing them?
* You're building a computer for gaming. What features should you prioritize in a motherboard, and why?

**Specific Features**
* Explain the purpose of onboard audio vs. a dedicated sound card.
* What is the advantage of motherboards with multiple M.2 slots?
* Describe the different PCIe versions (e.g., PCIe 3.0, 4.0, 5.0) and their significance in terms of bandwidth.
* What is the role of motherboard headers (USB headers, fan headers, RGB headers)?

**Overclocking**
* Beyond voltage and multiplier, what other factors (e.g., BCLK, memory timings) often need fine-tuning for a successful overclock?
* Describe the different types of stress testing tools used to evaluate overclock stability.  What specific system conditions do they monitor?
* Discuss the trade-offs between using liquid cooling vs. advanced air cooling for an overclocked system.
* Explain the risks of excessive CPU overclocking on long-term component lifespan.

**Turbo Speed**
* How does CPU Turbo Boost (Intel) or Precision Boost (AMD) technology work to intelligently increase clock speeds under specific workloads?
* What factors, other than raw clock speed, can influence the performance benefits seen from turbo modes?

**BIOS Options**
* Explain the significance of memory XMP (Intel) or DOCP (AMD) profiles within the BIOS settings.
* What BIOS setting(s) would you adjust to enable or disable hardware virtualization support?
* Describe how to change the boot order of devices in the BIOS and why this might be necessary. 

**Motherboard Architecture**
* Explain the concept of PCIe lanes and how they are allocated among different expansion slots and devices.
* How does the DMI (Direct Media Interface) connect the chipset to the CPU, and what potential bottlenecks can it create?

**DMA, IRQ**
* Describe a scenario where using DMA (Direct Memory Access) offers a significant performance advantage over traditional programmed I/O.
* How are IRQ (Interrupt Request) lines used by devices to signal attention from the CPU?  Briefly explain potential issues that can arise from IRQ conflicts.

**Chipset Features**
* Outline the key differences between modern AMD and Intel chipsets in terms of supported features and target audiences (e.g., X570 vs. Z690).
* What chipset features are crucial to maximizing the capabilities of a high-speed NVMe SSD?

**Form Factors**
* Besides physical size, discuss functional differences between ATX, Micro-ATX, and Mini-ITX motherboards.
* For a compact, space-efficient workstation build, what limitations and advantages should be considered when using a Mini-ITX motherboard?

Absolutely! Here are some questions to test knowledge about motherboard voltage levels and their applications:

**Identification and Purpose**
* List the most common voltage rails found on a modern motherboard (e.g., +12V, +5V, +3.3V, Vcore). Indicate the typical usage of each.
* Which voltage rail is essential for powering the CPU? How does the VRM (Voltage Regulator Module) play a role in delivering this power?
* What components are typically powered by the +5V rail?
* Which voltage rail is most often used by RAM (DDR4 or DDR5)?

**Troubleshooting and Diagnostics**
* A system unexpectedly shuts down under heavy load.  Suspecting a power issue, how could you use a multimeter to check if the motherboard is supplying correct voltages?
* You encounter errors related to a SATA hard drive. What voltage rail(s) would be relevant to check during troubleshooting?

**Advanced / Overclocking**
* Explain the term 'Vdroop'. How does it relate to motherboard power delivery, and why is it relevant for overclockers?
* Describe the purpose of advanced voltage control options within a motherboard's BIOS (e.g., LLC - Load-Line Calibration).

**Specific Components**
* Certain PCIe expansion cards require additional power directly from the PSU. Which voltage rail(s) are typically used for these PCIe power connectors?
* How do motherboard fan headers provide different voltage levels (or PWM control) to achieve variable fan speeds?

**Expansion Slots**
* Describe the different PCIe slot versions (x1, x4, x16) and their typical uses.
* What graphics card features should you prioritize for a system built for 4K video editing?
* You want to install multiple high-performance NVMe SSDs. What motherboard features should you look for to maximize their connectivity?

**Onboard Features**
* Outline the advantages and disadvantages of onboard Wi-Fi vs. a dedicated PCIe Wi-Fi card.
* Discuss scenarios where using a dedicated sound card offers tangible benefits over a motherboard's onboard audio.
* What type of motherboard headers are used for connecting additional USB ports on a case?

**Troubleshooting**
* A computer fails to boot, and no beeps are heard.  What motherboard-related areas would you initially investigate?
* The system recognizes a newly installed RAM module but fails to utilize its full capacity. What could be the reasons?
* Describe the steps you would take to troubleshoot a non-functional Ethernet port on the motherboard.

