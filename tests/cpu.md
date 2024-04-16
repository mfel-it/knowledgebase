# CPU Knowledge test

* What is the purpose of the CPU in a computer system?
* Explain the difference between a CPU and a GPU.
* What are the main components of a CPU?
* Describe the function of the Arithmetic Logic Unit (ALU) in a CPU.
* What is the role of the Control Unit in a CPU?
* Explain the concept of clock speed and its impact on CPU performance.
* What is the difference between a single-core and a multi-core CPU?
* How does the CPU interact with other components of a computer system?
* Discuss the concept of cache memory and its importance in CPU performance.
* Explain the difference between a 32-bit and a 64-bit CPU architecture.
* Explain the difference between a CPU's L1, L2, and L3 cache.
* Describe the fetch-decode-execute cycle.
* What factors influence a CPU's benchmark score?
* How does CPU thermal throttling work, and why is it important?
* Explain compatibility considerations when choosing a CPU for a specific motherboard socket.
* Describe how multiple CPU cores and threads work together to improve performance.
* What are the factors that influence a CPU's cache size (L1, L2, L3), and how does cache affect performance?
* Discuss the advantages of a CPU with an unlocked multiplier for overclocking.

**Multiple Choice**
* **Which of the following CPU features is primarily designed to enhance single-thread performance?**
   * Increased core count
   * Hyper-threading
   * Larger L2/L3 cache
   * Higher clock speed

* **What is the primary role of a CPU's Control Unit?**
    * Executing arithmetic and logic operations
    * Fetching instructions from memory
    * Decoding instructions from memory
    * Managing data flow between the CPU and RAM

* **A CPU with a 64-bit architecture can directly address a maximum of approximately how much RAM?**
    * 4 GB
    * 16 GB
    * 128 GB
    * 18 Exabytes (18 billion GB)

* **Which of the following is NOT a common CPU socket type?**
    * LGA
    * PGA 
    * AM4
    * XQD

**Scenario-Based**
* You're building a computer for video editing. What CPU characteristics should you prioritize, and why?
* A user's computer is experiencing slow performance, even during basic tasks. List troubleshooting steps you would take to isolate whether the CPU is the bottleneck.

**x86 vs. ARM**
* Explain the key differences between CISC and RISC instruction sets, and how they relate to x86 and ARM respectively.
* Discuss the trade-offs between x86 and ARM architectures in terms of performance and power consumption.
* Provide real-world applications where an ARM-based processor might be a better fit than an x86 processor, and justify your reasoning.

**Multi-core Concepts**
* What is the purpose of hyper-threading? Describe a scenario where it offers significant benefits and one where it offers minimal benefits.
* Outline challenges faced by software developers in fully optimizing applications for multi-core CPUs.
* Explain the concepts of Amdahl's Law and Gustafson's Law in the context of multi-core scaling.

**Power Management**
* Describe different power-saving states (C-states) supported by modern CPUs.
* How do CPU frequency scaling and voltage scaling work to reduce power consumption?
* Beyond architectural features, what are some software-level techniques for optimizing power efficiency in CPU-bound tasks?

**Overclocking**
* What are the primary risks associated with overclocking a CPU?
* List the essential components (beyond the CPU itself) that need to be robust for a successful and stable overclock.
* Explain how increasing core voltage and adjusting the clock multiplier influence overclock outcomes.

**Virtualization**
* What are the hardware-assisted virtualization features commonly found in modern CPUs?
* Describe the difference between Type-1 and Type-2 hypervisors.
* Outline a security consideration when using virtualization in a production environment.

**Security Features**
* Explain how the Meltdown and Spectre vulnerabilities exploited design aspects of modern CPUs.
* Describe a hardware-based security mitigation implemented in CPUs to address certain classes of vulnerabilities.
* Outside of the CPU itself, how does a secure boot process contribute to the overall security of a system?

**Security: Conceptual**
* What is the principle of a side-channel attack? Provide a real-world example.
* Explain how speculative execution can be exploited by attackers and describe mitigations against such attacks.
* What is a microarchitectural data sampling (MDS) attack, and how does it differ from Meltdown/Spectre?
* Describe the role of a Trusted Platform Module (TPM) in enhancing system security.
* How does Secure Encrypted Virtualization (SEV) protect the contents of virtual machine memory, even from the hypervisor?


**Security: Application-Based**
* You're choosing a CPU for a server handling highly sensitive data. What security features would be at the top of your requirements list, and why?
* A software patch is released that mitigates a CPU-level vulnerability but has a potential performance impact.  Discuss factors you'd consider when deciding whether to apply the patch in a production environment.
* How does memory tagging, a potential future CPU security feature, aim to prevent classes of memory corruption vulnerabilities?


**Security: Beyond Traditional CPUs**
* Some CPUs include dedicated AI accelerators. What unique security concerns might these accelerators introduce?
* How might the security considerations for CPUs in embedded systems differ from those in traditional desktop/server CPUs?

