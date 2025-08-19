

# **The AI Compute and Capital Deep Dive: An Expert Report on the 2024-2025 Landscape**

## **Chapter 2: The AI Infrastructure and Compute Landscape**

### **The Incumbent Titans: NVIDIA, AMD, and Intel**

The AI compute landscape in 2024 and 2025 is defined by an accelerating arms race for silicon dominance, driven by an insatiable demand for processing power. At the forefront of this competition are the traditional semiconductor giants, each pursuing a distinct strategy to capture market share and establish a defensible position.

NVIDIA's Unwavering Dominance and Strategic Roadmap  
NVIDIA continues to lead the market, not merely by producing the fastest chips but by orchestrating a vertically integrated compute ecosystem. The company has adopted a rapid, sub-two-year cadence for new products, with a roadmap that introduces new chips about every 12 to 18 months.1 The Blackwell Ultra GPU is set for production in the second half of 2025, while the Rubin GPU and its Ultra variant are slated for release in the second half of 2026 and 2027, respectively.1 This aggressive pace of innovation is a powerful competitive advantage. The scale of NVIDIA's market penetration is evident in its sales, with more than 3.6 million Blackwell GPUs sold to the top four U.S. cloud service providers alone in 2025.1  
A core component of NVIDIA's strategy is the creation of a unified, rack-scale computing fabric. The Grace Blackwell (GB200) Superchip is a prime example of this approach, integrating two Blackwell GPUs and an Arm-based Grace CPU via the NVLink-C2C interconnect.2 This tightly coupled design enhances bandwidth between the GPU and CPU by an order of magnitude.2 The fifth-generation NVLink doubles the bidirectional bandwidth to 1.8 terabytes per second (TB/s) over its predecessor, greatly improving intra-server communication.2 This technology extends beyond single servers; the NVLink Switch allows for up to 576 fully connected GPUs in a non-blocking compute fabric, effectively transforming an entire rack of GPUs into a single, massive accelerator.3 This proprietary interconnect technology is a critical pillar of NVIDIA's market position, as it simplifies the deployment of trillion-parameter models for hyperscale customers while creating a high degree of technological lock-in.

AMD's Open Ecosystem and Value Proposition  
In direct contrast to NVIDIA's proprietary model, AMD is positioning itself as a leader of an open, collaborative ecosystem. The company's roadmap is highly competitive, with the Instinct MI350 series launching in 2025, and the MI400 series slated for 2026.4 The MI350 series delivers a reported 4x generational increase in AI compute and a 35x leap in inferencing performance over the previous MI300X, paving the way for advanced solutions across multiple industries.4 The upcoming MI400 is confirmed to use next-generation HBM4 memory, providing a substantial 19.6 TB/s of bandwidth, a direct response to NVIDIA's roadmap and positioning AMD to compete directly with its flagship platforms.5  
AMD's strategic foundation lies in its open-source ROCm software stack and its role as a contributing member of the Ultra Ethernet Consortium (UEC).7 This approach is a direct appeal to hyperscalers and enterprises seeking to avoid reliance on a single vendor. The company's collaborations with major players like Meta, which has deployed MI300X GPUs for Llama inference, and Oracle Cloud Infrastructure (OCI), which plans to offer zettascale clusters with up to 131,072 MI355X GPUs, demonstrate the growing adoption of this open-standards approach.4 AMD is not just selling chips but building a high-performance alternative that de-risks a company's long-term compute strategy.

Intel's Strategic Pivot and Gaudi's Niche  
Intel's AI strategy in 2024 and 2025 is a pragmatic adjustment to the competitive landscape. Rather than a head-on confrontation with NVIDIA in the high-end training market, Intel has shifted its focus to high-growth areas like edge AI, agentic AI, and AI-enabled consumer devices.9 This pivot is supported by the Gaudi 3 accelerator, which has shown a compelling performance-per-dollar advantage over the NVIDIA H100 in specific inference workloads.9 For example, Gaudi 3 reportedly outperformed the H100 in Llama-3.1-405B inferencing on IBM Cloud and offered 70% better price-performance for Llama 3 80B on Dell's AI platform.9  
This targeted approach to the enterprise market is a departure from the hyperscaler-focused battles of its rivals. Intel is actively partnering with companies like IBM Cloud to make Gaudi 3 accelerators available to a wider enterprise audience.10 While Intel's AI revenue is projected to be around $1.2 billion in 2025, which is dwarfed by NVIDIA's projected $15 billion in AI-related revenue, the company is playing a long game by focusing on high-volume, cost-sensitive inference workloads.9 The company's emphasis on open-source tools and partnerships aims to mitigate the challenges posed by NVIDIA's dominant CUDA ecosystem.9

### **The Ascendant Innovators: Specialized Architectures**

The AI hardware market is not solely a battle among the incumbents. A new class of innovators is emerging, each with a specialized architectural approach designed to address a specific bottleneck in the AI compute stack.

Cerebras: The Wafer-Scale Bet  
Cerebras Systems is challenging the fundamental paradigm of AI computing with its wafer-scale engine (WSE) technology. The latest iteration, the Wafer-Scale Engine 3 (WSE-3), is the world's largest single chip, measuring 46,255 mm² and containing 4 trillion transistors.11 This monolithic design delivers a peak performance of 125 petaflops of AI compute and an unprecedented 21 petabytes per second of memory bandwidth.11  
The WSE-3 is designed to support immense models with up to 24 trillion parameters by decoupling memory from the computational cores, using an external, independently scalable memory cluster called MemoryX.11 This approach bypasses the memory fragmentation and communication overheads inherent in traditional multi-GPU clusters. Cerebras is not a general-purpose competitor; its solution is tailored for the largest, most demanding scientific and foundation model training jobs that require single-device simplicity. The WSE-3 has already demonstrated its capability by outperforming competitors in specific high-end inference tasks.13

Groq: The Low-Latency Inference Engine  
Groq is carving out a niche in the high-speed inference market with its purpose-built Language Processing Unit (LPU). Unlike dynamically scheduled GPU architectures, the Groq LPU uses static scheduling to eliminate non-deterministic latency and on-chip SRAM for primary weight storage.14 This unique design allows the LPU to achieve a deterministic latency below 1 millisecond and a Time to First Token (TTFT) of 0.22 seconds.16 This result is reportedly 3 to 18 times faster than other cloud-based inference providers.16  
Groq's core value proposition is predictability. In a world where consistent, low-latency responses are critical for real-time applications like conversational and agentic AI, Groq's deterministic architecture offers a significant advantage. This strategic focus has attracted major capital. At LEAP 2025, Groq secured a $1.5 billion commitment from the Kingdom of Saudi Arabia to expand its AI inference infrastructure, a move that highlights the geopolitical importance of building high-speed domestic AI capabilities.17

Graphcore: The New SoftBank Play  
The market for specialized AI hardware is also undergoing consolidation. Graphcore, a pioneer in Intelligence Processing Units (IPUs), was acquired by SoftBank in July 2024 for a reported price of approximately $500 million, a value significantly less than its peak unicorn valuation.18 This acquisition is a strategic maneuver by SoftBank to bolster its position in the AI compute market by integrating Graphcore's technology with its chip design subsidiary, Arm.7  
SoftBank's intent is to combine Graphcore's innovative IPU architecture with the ubiquitous Arm ecosystem to create a more comprehensive AI solution, thereby challenging NVIDIA’s dominance through an open-standards approach.20 Since the acquisition, Graphcore has joined the Ultra Ethernet Consortium and embarked on a major hiring drive, a clear signal that SoftBank is revitalizing the company's technology and talent pool to compete in the long term.7

### **Cloud Hyperscalers: The New AI Data Centers**

The three major hyperscale cloud providers—Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP)—are at the heart of the AI compute revolution. Their strategies for providing AI infrastructure are diverging, reflecting their unique market positions and core business models.

AWS: The Comprehensive and Trusted Platform  
AWS is positioning itself as the indispensable, neutral utility provider for AI, offering customers maximum flexibility and choice. Its platform provides a comprehensive suite of AI services, including generative AI and agentic AI.22 AWS offers a wide range of purpose-built instances, from those powered by NVIDIA Hopper GPUs to its own custom-built silicon like EC2 Trn1 for training and Inf1 for inference.22 This breadth of offering allows customers to select the best hardware for their specific workload and budget.  
The company's approach is to abstract away the complexity of the underlying hardware, providing managed services like Amazon Bedrock that offer a choice of leading foundation models.22 This strategy resonates with enterprises that prioritize security, privacy, and avoiding vendor lock-in, cementing AWS's position as a go-to platform for companies seeking to adopt AI without committing to a single technology stack.22

Microsoft Azure: The Integrated and Custom Stack  
Microsoft's strategy is one of deep vertical integration, from custom hardware to end-user applications. Azure's infrastructure offers access to a variety of compute resources, including virtual machines powered by NVIDIA Hopper and AMD Instinct GPUs.23 However, Microsoft has also developed its own custom silicon, including the Azure Maia AI accelerator and the Azure Cobalt CPU series, to enhance performance and efficiency for its large-scale internal AI workloads.23 This dual approach allows Microsoft to optimize its own services, such as the Azure OpenAI Service and the flagship Microsoft Copilot, while still offering customers a wide range of hardware options.23  
By building its own chips and deeply integrating them with its software and services, Microsoft is creating a powerful, closed-loop ecosystem. This reduces its dependency on external hardware suppliers and creates a seamless, highly optimized experience for its vast enterprise customer base, making the company a self-sufficient powerhouse in the AI space.

Google Cloud Platform (GCP): The Innovation-Driven Ecosystem  
GCP is pursuing a dual-pronged strategy of "homegrown superiority" and "open ecosystem support." The company's proprietary Tensor Processing Units (TPUs) are a core component of its AI infrastructure, offering a differentiated solution for large-scale training and inference.25 The latest TPU v6e (Trillium) delivers 918 TFLOPS of BF16 compute per chip and features a new SparseCore designed for efficiency in sparse workloads like Mixture-of-Experts (MoE) models.26  
Google leverages managed services like Vertex AI and Google Kubernetes Engine (GKE) to simplify the orchestration of large-scale workloads on both TPUs and GPUs.25 At the same time, Google's co-founding of the OpenXLA project and its sponsorship of the PyTorch Foundation demonstrate a commitment to open standards, a strategic move that attracts a broader developer community.25 A notable development in 2025 is Google's partnership with Oracle, which will make Google's Gemini models available on Oracle Cloud Infrastructure, signaling a new willingness to decouple its most valuable software assets from its own hardware and expand its reach beyond its traditional platform.28

### **The Edge AI Frontier**

The development of AI is not confined to the data center; a new frontier is emerging at the edge, where AI models are deployed on-device for real-time, low-latency, and privacy-preserving applications.

Qualcomm: The AI PC and Hybrid AI Bet  
Qualcomm is leading the charge in the nascent "AI PC" market with its Snapdragon X Elite platform.29 The chip's integrated Hexagon NPU delivers 45 TOPS of performance, with the overall platform capable of reaching 75 TOPS.29 This power allows the Snapdragon X Elite to run generative AI models with up to 13 billion parameters locally on the device, enabling a new class of hybrid AI applications that combine local and cloud processing.29 Qualcomm is also strategically entering the data center market in partnership with NVIDIA, a move that aims to build a full cloud-to-edge AI stack.31  
Apple Silicon: The Vertical Integration Moat  
Apple's strategy is a masterclass in ecosystem lock-in, where the hardware is a means to an end: a seamless, privacy-focused user experience.32 The Apple M4 chip, built on TSMC’s second-generation 3nm process, features a 16-core Neural Engine that delivers 38 TOPS, a more than 2x performance increase over its predecessor.33 The M4’s unified memory architecture provides high bandwidth for AI workloads by eliminating costly data copies between the CPU, GPU, and NPU, a critical advantage for efficiency and performance at the edge.30 The tight integration of hardware and software allows Apple to deliver "Apple Intelligence" directly on-device, reinforcing its brand and creating a unique competitive advantage that is difficult for rivals to replicate.32  
NVIDIA Jetson: The Robotics and Industrial AI Play  
NVIDIA's edge strategy is highly specialized and industrial-focused. The new Jetson Thor is not a consumer-oriented device but a high-performance compute platform designed for "physical AI" and robotics.35 Powered by the Blackwell GPU, it delivers up to 2070 FP4 TFLOPS of AI compute within a 130W power envelope.35 This makes it a powerful embedded brain for autonomous systems and industrial machinery. Unlike the previous Jetson Orin modules, the Thor is not pin-compatible, a change that reflects its focus on new, high-performance industrial applications where power and processing capability are prioritized over backward compatibility.36

## **Chapter 7: The Economics of Compute and Capital**

### **The Shifting Economics of AI Workloads**

The economic model of AI development is bifurcating into two distinct and asymmetrical phases: the capital-intensive training phase and the rapidly commoditizing inference phase.

Training Economics: The Billion-Dollar Race  
The cost of training frontier AI models is growing at an exponential rate. Research suggests that training compute costs are doubling every nine months.37 In 2024, the cost of a single training run for a frontier model was projected to reach close to a billion dollars.38 The upfront hardware capital expenditure (CapEx) to acquire the compute infrastructure for a model like GPT-4 was estimated at $800 million.38 This astronomical cost creates a significant barrier to entry, effectively concentrating the power to build foundational models in the hands of a few well-capitalized tech giants and sovereign-backed startups. It transforms the AI race into a capital-intensive arms race where the ability to afford the hardware and associated operational costs is a primary competitive advantage.  
Inference Economics: The Cost-per-Token Revolution  
In contrast to the rising costs of training, the economics of AI inference are experiencing a rapid and dramatic decline. The cost per million tokens has decreased by approximately 10x from March 2023 to August 2024.39 For a model performing at the level of GPT-3.5, the inference cost dropped more than 280-fold between November 2022 and October 2024, a reflection of improved hardware and model efficiency.40 This trend is arguably the single most important factor for the commercialization and widespread adoption of AI. As the cost of running a query drops to near-zero, it becomes economically viable to integrate AI into every business process and application, enabling a new wave of services that were previously too expensive to deploy at scale.

### **Investment and Strategic Capital Flows**

The flow of capital into the AI ecosystem is a powerful signal of its strategic importance, and the sources of this capital are becoming increasingly diverse, moving beyond traditional venture funding to include sovereign and defense-linked investors.

Venture Capital in the AI Era: a16z and Sequoia  
Venture capital firms are moving beyond a simple "AI for X" investment thesis and are now looking to fund companies that solve fundamental, deep-seated problems. Sequoia's 2024 investment thesis, for example, likens the current market to a "primordial soup" that requires visionary founders to discover and invent new things rather than just building on existing technologies.41 This contrasts with the frenzy of 2023, which produced many companies with similar objectives.41  
Andreessen Horowitz (a16z) has been an active investor with theses spanning "Bio \+ Health," "Enterprise," "Fintech," and "American Dynamism".42 A new and powerful phenomenon in the venture landscape is the "OpenAI alumni effect," where a number of former OpenAI employees are launching high-value startups.43 Investors are pouring billions into these ventures, signaling a strong conviction that the teams that worked at the frontier of AI have a unique understanding of the unsolved problems and the vision to build the next generation of foundational companies.43

The Rise of Sovereign Funds: PIF, Mubadala, and Temasek  
Sovereign wealth funds are no longer passive investors; they are becoming active geopolitical actors using capital as a tool for economic diversification and national security. In 2024, Abu Dhabi's Mubadala Investment Co. was the world's most active sovereign wealth fund, deploying $29.2 billion.44 At the same time, Saudi Arabia's Public Investment Fund (PIF) has shifted its focus to domestic projects as part of its Vision 2030 initiative.44 This does not preclude foreign investments, but rather re-orients them toward strategic goals. The $1.5 billion commitment from Saudi Arabia to Groq at LEAP 2025 is a clear example of this strategy, as it aims to build a domestic AI infrastructure to reduce reliance on foreign powers.17 This demonstrates a willingness to make massive, long-term bets to secure a national competitive advantage.  
Defense-Linked Capital: In-Q-Tel and NATO DIANA  
The lines between commercial, venture, and defense capital are blurring, with new investment vehicles emerging to bridge the gap between technology and national security. In-Q-Tel (IQT) is a not-for-profit firm that invests in global innovation to secure the U.S., with its 800th investment closing in 2025.46 Its portfolio includes companies in areas like AI, cyber, and microelectronics.47  
Similarly, the NATO Innovation Fund (NIF) is a venture capital fund backed by 24 NATO allies with a total of more than one billion euros to deploy in deep tech companies.48 The NIF's focus is on "dual-use" technologies that have both commercial and defense applications, such as the quantum sensing company it first invested in in 2024\.50 These investment vehicles demonstrate that governments and supranational organizations are using capital as a strategic tool to accelerate innovation and ensure a technological advantage, moving faster than traditional procurement models would allow.

### **Systems Map 1: The Compute Stack**

The following map outlines the dependencies within the AI compute ecosystem, from foundational raw materials to the final service layer.

* **Raw Materials:** Sand, rare earth metals, and chemical precursors.  
* **Foundry & Fabrication:** TSMC (NVIDIA, AMD, Apple), Intel, Samsung. This layer is constrained by capacity for advanced nodes (e.g., 3nm, 5nm) and advanced packaging technologies.  
* **Chip Architecture:**  
  * **GPU/NPU:** NVIDIA (Hopper, Blackwell), AMD (Instinct MI300/400), Intel (Gaudi), ARM.  
  * **Specialized Accelerators:** Groq (LPU), Cerebras (WSE-3), Graphcore (IPU).  
* **Interconnects:** NVIDIA (NVLink/NVLink-C2C, NVLink Switch), AMD (Infinity Fabric), open standards (Ultra Ethernet Consortium/UEC, RDMA over Converged Ethernet/RoCE). This layer dictates the scalability and efficiency of multi-chip systems.  
* **Cloud & Edge Platforms:**  
  * **Hyperscalers:** AWS, Microsoft Azure, Google Cloud Platform (GCP), Oracle Cloud Infrastructure (OCI). These platforms bundle the underlying hardware into accessible services.  
  * **Edge Devices:** Qualcomm (Snapdragon), Apple (Apple Silicon), NVIDIA (Jetson).  
* **Software & Frameworks:** NVIDIA (CUDA), AMD (ROCm), Google (TensorFlow, JAX, OpenXLA), PyTorch. This layer enables developers to utilize the underlying hardware.  
* **End-User Services:**  
  * **Training:** High-end, capital-intensive training runs for frontier models.  
  * **Inference:** Real-time, low-latency applications for chatbots, agents, and robotics.

### **Systems Map 2: The Capital & Strategic Flow**

The following map illustrates the flow of strategic capital from diverse investor groups into the AI ecosystem, highlighting key dependencies and motivations.

* **Venture Capital:** (a16z, Sequoia)  
  * **Motive:** High-growth returns, market creation, and disruption.  
  * **Flows to:** AI startups, horizontal platforms (e.g., ElevenLabs), vertical applications (e.g., HappyRobot), foundational models (e.g., OpenAI, Anthropic), and infrastructure (e.g., Cerebras).  
* **Sovereign Wealth Funds:** (PIF, Mubadala, Temasek)  
  * **Motive:** National economic diversification, technology transfer, and geopolitical influence.  
  * **Flows to:** Domestic AI infrastructure projects (e.g., Groq's Saudi data center) and strategic foreign investments (e.g., SoftBank/Graphcore acquisition).  
* **Defense-Linked Capital:** (In-Q-Tel, NATO DIANA/NIF)  
  * **Motive:** Long-term strategic technological advantage, national security, and resilience.  
  * **Flows to:** "Dual-use" deep tech startups (e.g., quantum sensing, advanced materials, secure computing) that can serve both commercial and military applications.  
* **Corporate Venture Capital & Strategic Alliances:** (Google, Microsoft, SoftBank)  
  * **Motive:** Securing supply, building a competitive ecosystem, and vertical integration.  
  * **Flows to:** Foundational model companies (e.g., SoftBank's investment in OpenAI), chip designers (e.g., SoftBank's acquisition of Graphcore), and cloud partners (e.g., Oracle and Google partnership).

### **Cost and Performance of AI Compute**

The following table provides a comparison of key AI chips and systems, focusing on performance, memory, and availability as of mid-2025.

| Chip/System | Node | Memory | Interconnect | Perf (TFLOPS/TOPS) | Availability | Target Workload | $/token est. | Source |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **NVIDIA B200** | 4nm | 192GB HBM3e | NVLink 1.8TB/s | 900 FP8 TFLOPS | H2 2025+ (backlogged) | Training, HPC | $1.10 \- $2.20 (GPT-4.1) | 1 |
| **AMD MI350X** | 3nm | 288GB HBM3e | AMD Infinity Fabric | 5,229 FP8 TFLOPS | 2H 2025 | Training, HPC, Inference | N/A | 4 |
| **Intel Gaudi 3** | 5nm | 128GB HBM2e | 24x 200Gb Ethernet | 1,835 FP8 TFLOPS | 2024 | Inference, Fine-tuning | N/A | 60 |
| **Cerebras WSE-3** | 5nm | 44GB on-chip SRAM | Swarm Network | 125,000 FP16 TFLOPS | 2024 | Ultra-large model training | N/A | 11 |
| **Groq LPU** | 14nm | On-chip SRAM | Static-Scheduled Net | 750 TOPS | 2024 | Low-latency inference | N/A | 14 |
| **Apple M4 Neural Engine** | 3nm | Unified | Coherent memory fabric | 38 TOPS | 2024 | On-device AI, consumer | N/A | 30 |
| **NVIDIA Jetson Thor** | N/A | 128GB LPDDR5X | NVLink-C2C | 2,070 FP4 TFLOPS | 2025 | Robotics, physical AI | N/A | 35 |

Απόσπασμα κώδικα

Chip/System,Node,Memory,Interconnect,Perf (TFLOPS/TOPS),Availability,Target Workload,$/token est.,Source  
NVIDIA B200,4nm,"192GB HBM3e","NVLink 1.8TB/s","900 FP8 TFLOPS","H2 2025+ (backlogged)","Training, HPC","1.10 \- 2.20 (GPT-4.1)",\[1, 59\]  
AMD MI350X,3nm,"288GB HBM3e",AMD Infinity Fabric,"5,229 FP8 TFLOPS",2H 2025,"Training, HPC, Inference",N/A,\[4, 8\]  
Intel Gaudi 3,5nm,"128GB HBM2e",24x 200Gb Ethernet,"1,835 FP8 TFLOPS",2024,"Inference, Fine-tuning",N/A,\[60, 61\]  
Cerebras WSE-3,5nm,"44GB on-chip SRAM",Swarm Network,"125,000 FP16 TFLOPS",2024,"Ultra-large model training",N/A,\[11, 12\]  
Groq LPU,14nm,On-chip SRAM,Static-Scheduled Net,"750 TOPS",2024,Low-latency inference,N/A,\[14, 16\]  
Apple M4 Neural Engine,3nm,Unified,Coherent memory fabric,"38 TOPS",2024,"On-device AI, consumer",N/A,\[30, 33\]  
NVIDIA Jetson Thor,N/A,"128GB LPDDR5X",NVLink-C2C,"2,070 FP4 TFLOPS",2025,"Robotics, physical AI",N/A,\[35\]

### **Capital Flow Table**

| Investor | Target | Round/Amount | Stage | Strategic Motive | Date | Source |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| SoftBank Group | Graphcore | Acquisition (\~$500M) | Acquisition | Integrate IPU tech with Arm to challenge NVIDIA | Jul 2024 | 18 |
| Kingdom of Saudi Arabia | Groq | Commitment ($1.5B) | Expansion | Build domestic, high-speed inference infrastructure | Feb 2025 | 17 |
| a16z | Periodic Labs | Series A ($200M) | Seed/A | Bet on "OpenAI alumni" talent in AI for scientific discovery | Aug 2025 | 43 |
| SoftBank Group | OpenAI | Investment ($15B-$25B planned) | Strategic | Secure position in foundation models and challenge tech giants | Jan 2025 | 62 |
| NATO Innovation Fund | Aquark Technologies | Seed (€5M) | Seed | Secure quantum sensing for defense & telecom | Sep 2024 | 50 |

### **Risk Memo**

The AI infrastructure supply chain and market structure present significant concentration and geopolitical risks. The primary chokepoint has shifted from semiconductor fabrication to advanced packaging and High-Bandwidth Memory (HBM) supply. TSMC's CoWoS packaging capacity was a major bottleneck in 2024, causing shortages across the industry, though the company plans to nearly triple its capacity by 2026\.51 Similarly, the three dominant HBM producers—SK Hynix, Samsung, and Micron—have reported lead times of six to twelve months due to soaring demand.53 These supply constraints create a single point of failure for the entire industry.

Geopolitical risks are embodied in the evolving landscape of U.S. export controls. In 2024, the U.S. expanded restrictions to include advanced HBM, prohibiting its sale to China to degrade its AI industry.54 An unusual deal was also brokered, allowing NVIDIA and AMD to sell specific chips in China in exchange for a 15% revenue share with the U.S. government.56 These policies are creating a two-tiered global AI market and may inadvertently accelerate China's technological independence as its firms are compelled to innovate in efficiency and find alternative supply chains.57

Finally, the market is facing significant cloud concentration risk. The top four U.S. cloud providers are dominating the allocation of next-generation GPUs, cementing their role not just as providers but as the primary beneficiaries and architects of the AI revolution.1 This concentration of compute power could stifle broader market competition, as a small number of powerful platforms control the infrastructure necessary for developing and deploying frontier AI models. This raises concerns about innovation and accessibility for startups and smaller enterprises.

#### **Πηγές αναφοράς**

1. Nvidia details AI roadmap with new chips, robots and more | Manufacturing Dive, πρόσβαση Αυγούστου 17, 2025, [https://www.manufacturingdive.com/news/nvidia-details-ai-roadmap-Rubin-Blackwell-Ultra-chips-robots/742902/](https://www.manufacturingdive.com/news/nvidia-details-ai-roadmap-Rubin-Blackwell-Ultra-chips-robots/742902/)  
2. Train and deploy AI models at trillion-parameter scale with Amazon ..., πρόσβαση Αυγούστου 17, 2025, [https://aws.amazon.com/blogs/machine-learning/train-and-deploy-ai-models-at-trillion-parameter-scale-with-amazon-sagemaker-hyperpod-support-for-p6e-gb200-ultraservers/](https://aws.amazon.com/blogs/machine-learning/train-and-deploy-ai-models-at-trillion-parameter-scale-with-amazon-sagemaker-hyperpod-support-for-p6e-gb200-ultraservers/)  
3. NVLink & NVSwitch: Fastest HPC Data Center Platform | NVIDIA, πρόσβαση Αυγούστου 17, 2025, [https://www.nvidia.com/en-us/data-center/nvlink/](https://www.nvidia.com/en-us/data-center/nvlink/)  
4. AMD Unveils Vision for an Open AI Ecosystem, Detailing New Silicon, Software and Systems at Advancing AI 2025, πρόσβαση Αυγούστου 17, 2025, [https://ir.amd.com/news-events/press-releases/detail/1255/amd-unveils-vision-for-an-open-ai-ecosystem-detailing-new-silicon-software-and-systems-at-advancing-ai-2025](https://ir.amd.com/news-events/press-releases/detail/1255/amd-unveils-vision-for-an-open-ai-ecosystem-detailing-new-silicon-software-and-systems-at-advancing-ai-2025)  
5. The Biggest AMD Advancing AI News: From MI500 GPU TO ROCm Enterprise AI \- CRN, πρόσβαση Αυγούστου 17, 2025, [https://www.crn.com/news/ai/2025/the-biggest-amd-advancing-ai-news-from-mi500-gpu-to-rocm-enterprise-ai](https://www.crn.com/news/ai/2025/the-biggest-amd-advancing-ai-news-from-mi500-gpu-to-rocm-enterprise-ai)  
6. AMD's next-gen Instinct MI400 GPU confirmed: rocks 432GB of HBM4 at 19.6TB/sec ready for 2026 \- TweakTown, πρόσβαση Αυγούστου 17, 2025, [https://www.tweaktown.com/news/105758/amds-next-gen-instinct-mi400-gpu-confirmed-rocks-432gb-of-hbm4-at-19-6tb-sec-ready-for-2026/index.html](https://www.tweaktown.com/news/105758/amds-next-gen-instinct-mi400-gpu-confirmed-rocks-432gb-of-hbm4-at-19-6tb-sec-ready-for-2026/index.html)  
7. Graphcore joins Ultra Ethernet Consortium, πρόσβαση Αυγούστου 17, 2025, [https://www.graphcore.ai/posts/graphcore-joins-ultra-ethernet-consortium](https://www.graphcore.ai/posts/graphcore-joins-ultra-ethernet-consortium)  
8. Advancing AI 2025: AMD's Latest Products Focused on Openness \- Counterpoint Research, πρόσβαση Αυγούστου 17, 2025, [https://www.counterpointresearch.com/insight/advancing-ai-2025-amds-latest-products-focused-on-openness/](https://www.counterpointresearch.com/insight/advancing-ai-2025-amds-latest-products-focused-on-openness/)  
9. Intel's Strategic Rebirth: Can Restructuring and AI Catch-Up Spark a ..., πρόσβαση Αυγούστου 17, 2025, [https://www.ainvest.com/news/intel-strategic-rebirth-restructuring-ai-catch-spark-buyout-turnaround-opportunity-2508/](https://www.ainvest.com/news/intel-strategic-rebirth-restructuring-ai-catch-spark-buyout-turnaround-opportunity-2508/)  
10. Intel and IBM Announce the Availability of Intel Gaudi 3 AI Accelerators on IBM Cloud, πρόσβαση Αυγούστου 17, 2025, [https://newsroom.ibm.com/blog-intel-and-ibm-announce-the-availability-of-intel-gaudi-3-ai-accelerators-on-ibm-cloud](https://newsroom.ibm.com/blog-intel-and-ibm-announce-the-availability-of-intel-gaudi-3-ai-accelerators-on-ibm-cloud)  
11. A Comparison of the Cerebras Wafer-Scale Integration Technology with Nvidia GPU-based Systems for Artificial Intelligence \- arXiv, πρόσβαση Αυγούστου 17, 2025, [https://arxiv.org/html/2503.11698v1](https://arxiv.org/html/2503.11698v1)  
12. The Future of AI is Wafer Scale \- Cerebras, πρόσβαση Αυγούστου 17, 2025, [https://www.cerebras.ai/chip](https://www.cerebras.ai/chip)  
13. Forget Nvidia: DeepSeek AI Runs Near Instantaneously on These Weird Chips, πρόσβαση Αυγούστου 17, 2025, [https://singularityhub.com/2025/02/06/forget-nvidia-deepseek-ai-runs-near-instantaneously-on-these-weird-chips/](https://singularityhub.com/2025/02/06/forget-nvidia-deepseek-ai-runs-near-instantaneously-on-these-weird-chips/)  
14. Inside the LPU: Deconstructing Groq's Speed | Groq is fast inference ..., πρόσβαση Αυγούστου 17, 2025, [https://groq.com/blog/inside-the-lpu-deconstructing-groq-speed](https://groq.com/blog/inside-the-lpu-deconstructing-groq-speed)  
15. Groq's LPU: A Revolutionary Leap in Processing for High-Performance Computing and AI, πρόσβαση Αυγούστου 17, 2025, [https://abhijit-singh.medium.com/groqs-lpu-a-revolutionary-leap-in-processing-for-high-performance-computing-and-ai-03624a1658ee](https://abhijit-singh.medium.com/groqs-lpu-a-revolutionary-leap-in-processing-for-high-performance-computing-and-ai-03624a1658ee)  
16. Groq LPU™ Inference Engine Crushes First Public LLM Benchmark, πρόσβαση Αυγούστου 17, 2025, [https://groq.com/blog/groq-lpu-inference-engine-crushes-first-public-llm-benchmark](https://groq.com/blog/groq-lpu-inference-engine-crushes-first-public-llm-benchmark)  
17. Leap 2025 | Groq is fast inference for AI builders, πρόσβαση Αυγούστου 17, 2025, [https://groq.com/leap2025](https://groq.com/leap2025)  
18. Graphcore Systems \- 2025 Company Profile, Team, Funding, Competitors & Financials, πρόσβαση Αυγούστου 17, 2025, [https://tracxn.com/d/companies/graphcore-systems/\_\_1WwZI-hNZnHFQcSJbeebN0-1h8LjTjeGxM2tzN\_qnRk](https://tracxn.com/d/companies/graphcore-systems/__1WwZI-hNZnHFQcSJbeebN0-1h8LjTjeGxM2tzN_qnRk)  
19. Graphcore: From Unicorn to SoftBank Acquisition – What Happened? \- Turing Post, πρόσβαση Αυγούστου 17, 2025, [https://www.turingpost.com/p/graphcore-unicorn-softbank-acquisition-happened](https://www.turingpost.com/p/graphcore-unicorn-softbank-acquisition-happened)  
20. SoftBank buys Graphcore \- Jon Peddie Research, πρόσβαση Αυγούστου 17, 2025, [https://www.jonpeddie.com/news/softbank-buys-graphcore/](https://www.jonpeddie.com/news/softbank-buys-graphcore/)  
21. SoftBank shifts focus to AI and next-generation chips \- Digital Watch Observatory, πρόσβαση Αυγούστου 17, 2025, [https://dig.watch/updates/softbank-shifts-focus-to-ai-and-next-generation-chips](https://dig.watch/updates/softbank-shifts-focus-to-ai-and-next-generation-chips)  
22. Artificial Intelligence (AI) on AWS \- AI Technology \- AWS, πρόσβαση Αυγούστου 17, 2025, [https://aws.amazon.com/ai/](https://aws.amazon.com/ai/)  
23. Azure AI Innovations 2024: Leading Cloud Future, πρόσβαση Αυγούστου 17, 2025, [https://digital.neweratech.com/articles/azures-ai-driven-future-innovations-to-watch-in-2024](https://digital.neweratech.com/articles/azures-ai-driven-future-innovations-to-watch-in-2024)  
24. Top 20 AI Chip Makers: NVIDIA & Its Competitors in 2025 \- Research AIMultiple, πρόσβαση Αυγούστου 17, 2025, [https://research.aimultiple.com/ai-chip-makers/](https://research.aimultiple.com/ai-chip-makers/)  
25. AI Infrastructure ML and DL Model Training | Google Cloud, πρόσβαση Αυγούστου 17, 2025, [https://cloud.google.com/ai-infrastructure](https://cloud.google.com/ai-infrastructure)  
26. Google Trillium TPU (v6e) introduction : r/LocalLLaMA \- Reddit, πρόσβαση Αυγούστου 17, 2025, [https://www.reddit.com/r/LocalLLaMA/comments/1gnru7c/google\_trillium\_tpu\_v6e\_introduction/](https://www.reddit.com/r/LocalLLaMA/comments/1gnru7c/google_trillium_tpu_v6e_introduction/)  
27. Introduction to Vertex AI | Google Cloud, πρόσβαση Αυγούστου 17, 2025, [https://cloud.google.com/vertex-ai/docs/start/introduction-unified-platform](https://cloud.google.com/vertex-ai/docs/start/introduction-unified-platform)  
28. Google and Oracle partner to bring Gemini AI to Oracle Cloud customers, πρόσβαση Αυγούστου 17, 2025, [https://timesofindia.indiatimes.com/technology/tech-news/google-and-oracle-partner-to-bring-gemini-ai-to-oracle-cloud-customers/articleshow/123307833.cms](https://timesofindia.indiatimes.com/technology/tech-news/google-and-oracle-partner-to-bring-gemini-ai-to-oracle-cloud-customers/articleshow/123307833.cms)  
29. Qualcomm Ushers in the AI PC Era with Snapdragon X Elite at Computex 2025 \- Embedded, πρόσβαση Αυγούστου 17, 2025, [https://www.embedded.com/qualcomm-ushers-in-the-ai-pc-era-with-snapdragon-x-elite-at-computex-2025](https://www.embedded.com/qualcomm-ushers-in-the-ai-pc-era-with-snapdragon-x-elite-at-computex-2025)  
30. AI Titans Clash: Snapdragon X Elite vs Apple M4 vs Exynos 2500 – Which Chip Leads the AI Revolution? \- TS2 Space, πρόσβαση Αυγούστου 17, 2025, [https://ts2.tech/en/ai-titans-clash-snapdragon-x-elite-vs-apple-m4-vs-exynos-2500-which-chip-leads-the-ai-revolution/](https://ts2.tech/en/ai-titans-clash-snapdragon-x-elite-vs-apple-m4-vs-exynos-2500-which-chip-leads-the-ai-revolution/)  
31. Counterpoint Conversations: Fueling and Scaling the Future – Qualcomm Delves into Roadmap for Continued AI PC Growth, πρόσβαση Αυγούστου 17, 2025, [https://www.counterpointresearch.com/insight/counterpoint-conversations-fueling-scaling-future-qualcomm-roadmap-ai-pc-growth/](https://www.counterpointresearch.com/insight/counterpoint-conversations-fueling-scaling-future-qualcomm-roadmap-ai-pc-growth/)  
32. Apple's Silicon Blueprint: Unveiling the Next-Gen Chip Roadmap \- YouTube, πρόσβαση Αυγούστου 17, 2025, [https://www.youtube.com/watch?v=AZRuxcGXvio](https://www.youtube.com/watch?v=AZRuxcGXvio)  
33. Apple M4 \- Wikipedia, πρόσβαση Αυγούστου 17, 2025, [https://en.wikipedia.org/wiki/Apple\_M4](https://en.wikipedia.org/wiki/Apple_M4)  
34. Mac mini \- Technical Specifications \- Apple, πρόσβαση Αυγούστου 17, 2025, [https://www.apple.com/mac-mini/specs/](https://www.apple.com/mac-mini/specs/)  
35. Embedded Systems Developer Kits & Modules from NVIDIA Jetson, πρόσβαση Αυγούστου 17, 2025, [https://www.nvidia.com/en-us/autonomous-machines/embedded-systems/](https://www.nvidia.com/en-us/autonomous-machines/embedded-systems/)  
36. NVIDIA Jetson Thor: New SoC Features Guide \- RidgeRun Developer Wiki, πρόσβαση Αυγούστου 17, 2025, [https://developer.ridgerun.com/wiki/index.php/NVIDIA\_Jetson\_Thor:\_Powering\_the\_Future\_of\_Physical\_AI](https://developer.ridgerun.com/wiki/index.php/NVIDIA_Jetson_Thor:_Powering_the_Future_of_Physical_AI)  
37. LLM inference prices have fallen rapidly but unequally across tasks \- Epoch AI, πρόσβαση Αυγούστου 17, 2025, [https://epoch.ai/data-insights/llm-inference-price-trends](https://epoch.ai/data-insights/llm-inference-price-trends)  
38. Training AI Models and Compute Cost Optimization \- Hyperbolic, πρόσβαση Αυγούστου 17, 2025, [https://www.hyperbolic.ai/blog/training-ai-models-and-compute-cost-optimization](https://www.hyperbolic.ai/blog/training-ai-models-and-compute-cost-optimization)  
39. Large Language Models: Performance vs. Cost \- MentorCruise, πρόσβαση Αυγούστου 17, 2025, [https://mentorcruise.com/blog/how-does-the-quality-of-large-language-models-compare-with-their-costs/](https://mentorcruise.com/blog/how-does-the-quality-of-large-language-models-compare-with-their-costs/)  
40. The 2025 AI Index Report | Stanford HAI, πρόσβαση Αυγούστου 17, 2025, [https://hai.stanford.edu/ai-index/2025-ai-index-report](https://hai.stanford.edu/ai-index/2025-ai-index-report)  
41. AI in 2024: From Big Bang to Primordial Soup | Sequoia Capital, πρόσβαση Αυγούστου 17, 2025, [https://www.sequoiacap.com/article/ai-in-2024/](https://www.sequoiacap.com/article/ai-in-2024/)  
42. AI \+ a16z | Andreessen Horowitz, πρόσβαση Αυγούστου 17, 2025, [https://a16z.com/ai/](https://a16z.com/ai/)  
43. Ex-OpenAI execs raise $200M at $1B valuation for AI materials science startup backed by a16z \- Tech Funding News, πρόσβαση Αυγούστου 17, 2025, [https://techfundingnews.com/ex-openai-execs-raise-200m-at-1b-valuation-for-ai-materials-science-startup-backed-by-a16z/](https://techfundingnews.com/ex-openai-execs-raise-200m-at-1b-valuation-for-ai-materials-science-startup-backed-by-a16z/)  
44. Mubadala is 2024's most active sovereign wealth fund, πρόσβαση Αυγούστου 17, 2025, [https://gulfnews.com/business/markets/mubadala-is-2024s-most-active-sovereign-wealth-fund-1.500009652](https://gulfnews.com/business/markets/mubadala-is-2024s-most-active-sovereign-wealth-fund-1.500009652)  
45. Mubadala vs PIF: Two Giants Reshaping National Economies \- The Arab Today, πρόσβαση Αυγούστου 17, 2025, [https://www.thearabtoday.com/mubadala-vs-pif-how-two-investment-giants-are-changing-their-countries-economies/](https://www.thearabtoday.com/mubadala-vs-pif-how-two-investment-giants-are-changing-their-countries-economies/)  
46. About | Our Milestones \- IQT, πρόσβαση Αυγούστου 17, 2025, [https://www.iqt.org/about/our-milestones](https://www.iqt.org/about/our-milestones)  
47. Portfolio \- IQT, πρόσβαση Αυγούστου 17, 2025, [https://www.iqt.org/portfolio](https://www.iqt.org/portfolio)  
48. Topic: Defence Innovation Accelerator for the North Atlantic (DIANA) \- NATO, πρόσβαση Αυγούστου 17, 2025, [https://www.nato.int/cps/en/natohq/topics\_216199.htm](https://www.nato.int/cps/en/natohq/topics_216199.htm)  
49. The Nato Innovation Fund | NIF, πρόσβαση Αυγούστου 17, 2025, [https://www.nif.fund/](https://www.nif.fund/)  
50. NATO Innovation Fund announces first investment in a DIANA cohort company to boost quantum sensing, πρόσβαση Αυγούστου 17, 2025, [https://www.nif.fund/news/nato-innovation-fund-announces-first-investment-in-a-diana-cohort-company-to-boost-quantum-sensing/](https://www.nif.fund/news/nato-innovation-fund-announces-first-investment-in-a-diana-cohort-company-to-boost-quantum-sensing/)  
51. TSMC's CoWoS and AI-Driven Manufacturing: A Cornerstone of Semiconductor Innovation and Investment Potential \- AInvest, πρόσβαση Αυγούστου 17, 2025, [https://www.ainvest.com/news/tsmc-cowos-ai-driven-manufacturing-cornerstone-semiconductor-innovation-investment-potential-2508/](https://www.ainvest.com/news/tsmc-cowos-ai-driven-manufacturing-cornerstone-semiconductor-innovation-investment-potential-2508/)  
52. TSMC Claims AI Packaging Shortage Likely Through 2024 Despite Expanding Capacity, πρόσβαση Αυγούστου 17, 2025, [https://sourceability.com/post/tsmc-claims-ai-packaging-shortage-likely-through-2024-despite-expanding-capacity](https://sourceability.com/post/tsmc-claims-ai-packaging-shortage-likely-through-2024-despite-expanding-capacity)  
53. AI chip shortages deepen amid tariff risks \- Sourceability, πρόσβαση Αυγούστου 17, 2025, [https://sourceability.com/post/ai-chip-shortages-deepen-amid-tariff-risks](https://sourceability.com/post/ai-chip-shortages-deepen-amid-tariff-risks)  
54. Understanding the Biden Administration's Updated Export Controls \- CSIS, πρόσβαση Αυγούστου 17, 2025, [https://www.csis.org/analysis/understanding-biden-administrations-updated-export-controls](https://www.csis.org/analysis/understanding-biden-administrations-updated-export-controls)  
55. U.S. Department of Commerce Strengthens Export Controls on Advanced Computing and Semiconductor Manufacturing Items | Covington & Burling LLP, πρόσβαση Αυγούστου 17, 2025, [https://www.cov.com/en/news-and-insights/insights/2024/12/us-department-of-commerce-strengthens-export-controls-on-advanced-computing-and-semiconductor-manufacturing-items](https://www.cov.com/en/news-and-insights/insights/2024/12/us-department-of-commerce-strengthens-export-controls-on-advanced-computing-and-semiconductor-manufacturing-items)  
56. US will get a 15% cut of Nvidia and AMD chip sales to China under a new, unusual agreement, πρόσβαση Αυγούστου 17, 2025, [https://apnews.com/article/nvidia-amd-15-revenue-share-deal-c06e20d9c3418f1d0b1292891c4610c6](https://apnews.com/article/nvidia-amd-15-revenue-share-deal-c06e20d9c3418f1d0b1292891c4610c6)  
57. US Export Controls on AI and Semiconductors \- International Center for Law & Economics, πρόσβαση Αυγούστου 17, 2025, [https://laweconcenter.org/resources/us-export-controls-on-ai-and-semiconductors/](https://laweconcenter.org/resources/us-export-controls-on-ai-and-semiconductors/)  
58. Trump's Chip Policy Disrupts Alliances \- OBSERVER RESEARCH FOUNDATION, πρόσβαση Αυγούστου 17, 2025, [https://www.orfonline.org/expert-speak/trump-s-chip-policy-disrupts-alliances](https://www.orfonline.org/expert-speak/trump-s-chip-policy-disrupts-alliances)  
59. Azure OpenAI Service \- Pricing, πρόσβαση Αυγούστου 17, 2025, [https://azure.microsoft.com/en-us/pricing/details/cognitive-services/openai-service/](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/openai-service/)  
60. Inside Intel Gaudi 3: The GenAI Accelerator Built for Enterprise Scale \- UNICOM Engineering, πρόσβαση Αυγούστου 17, 2025, [https://www.unicomengineering.com/blog/new-draft-intel-gaudi-3/](https://www.unicomengineering.com/blog/new-draft-intel-gaudi-3/)  
61. What is Intel Gaudi 3? A portrait of the AI accelerator \- IONOS, πρόσβαση Αυγούστου 17, 2025, [https://www.ionos.com/digitalguide/server/know-how/intel-gaudi-3/](https://www.ionos.com/digitalguide/server/know-how/intel-gaudi-3/)  
62. SoftBank Group's PayPay Files Paperwork for U.S. IPO — Update | Morningstar, πρόσβαση Αυγούστου 17, 2025, [https://www.morningstar.com/news/dow-jones/202508151956/softbank-groups-paypay-files-paperwork-for-us-ipo-update](https://www.morningstar.com/news/dow-jones/202508151956/softbank-groups-paypay-files-paperwork-for-us-ipo-update)  
63. ChatGPT Parent OpenAI (Current & ex-Employees) Plans $6 Billion Secondary Share Sale at $500 Billion Valuation to Investors Including SoftBank & Thrive Capital, Raised $40 Billion at $300 Billion Valuation in 2025 April Led by SoftBank Group & Required to Convert Structure from Non-Profit by 2025 June | Caproasia, πρόσβαση Αυγούστου 17, 2025, [https://www.caproasia.com/2025/08/16/chatgpt-parent-openai-current-ex-employees-plans-6-billion-secondary-share-sale-at-500-billion-valuation-to-investors-including-softbank-thrive-capital-raised-40-billion-at-300-billion-valu/](https://www.caproasia.com/2025/08/16/chatgpt-parent-openai-current-ex-employees-plans-6-billion-secondary-share-sale-at-500-billion-valuation-to-investors-including-softbank-thrive-capital-raised-40-billion-at-300-billion-valu/)