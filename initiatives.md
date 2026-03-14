---
layout: default
title: Initiatives
---

<div class="hero">
  <h1>Strategic Initiatives</h1>
  <p class="hero-subtitle">Real Projects. Questionable Corporate Framing.</p>
</div>

<section class="container section">
  <h2>Active Programs</h2>
  <p>At Skyenet, we don't just write firmware — we <em>optimize embedded infrastructure at scale</em>. Below are our primary operational initiatives, presented with the gravitas they deserve (and possibly don't).</p>
</section>

<section class="container section initiative-detail">
  <div class="initiative-header">
    <h2>Wireless RF Power Transmission Platform</h2>
    <span class="initiative-badge">Ossia Inc. | 2018–2024</span>
  </div>

  <p>Developed firmware, architecture, and cloud integration for the <strong>Cota wireless power system</strong> — a targeted RF power delivery platform capable of charging IoT devices at up to 10 meters range. The technology enables always-on operation for battery-dependent sensors in industrial, commercial, and smart building applications.</p>

  <h3>Technical Contributions</h3>
  <ul>
    <li>Lead software architect for <strong>Orion (2.4GHz)</strong> and <strong>Mars (5.8GHz)</strong> wireless power platforms</li>
    <li>Designed custom IoT microservice architecture with event-driven messaging bus — modular, scalable, target-independent</li>
    <li>Developed Hardware Abstraction Layer (HAL) enabling single-binary deployment across heterogeneous embedded targets</li>
    <li>Built and led software team from 1 to 12 engineers; served as de facto technical lead</li>
    <li>Integrated Azure IoT Hub for cloud connectivity — reduced infrastructure costs from $48K/month to $300/month (99.4% reduction)</li>
    <li>Developed ASIC firmware, power delivery algorithms, and real-time FCC compliance systems</li>
    <li>Enabled regulatory approval in 49 countries through direct FCC collaboration</li>
  </ul>

  <h3>Technologies</h3>
  <p>C, C++, Python, Embedded Linux, Yocto, Azure IoT Hub, Docker, Jenkins, HAL design, ASIC firmware, test-driven development</p>

  <h3>Impact</h3>
  <p>The Cota platform won two IoT Breakthrough Awards (2024) and multiple CES Innovation Awards (2023). Architectures formed the backbone of dozens of custom deployments and vendor integrations.</p>

  <p class="skyenet-note"><em>Incidentally, wireless power delivery is ideal for surveillance sensor networks and autonomous enforcement drones operating in areas where battery replacement is logistically impractical. Just saying.</em></p>
</section>

<section class="container section initiative-detail">
  <div class="initiative-header">
    <h2>Global Fleet Management Infrastructure</h2>
    <span class="initiative-badge">AWS Hardware Engineering | 2025–Present</span>
  </div>

  <p>Firmware-level control systems for <strong>over 3.2 million embedded platforms</strong> forming the backbone of AWS cloud infrastructure. Responsibilities include BMC software for EC2 Mac instances, EBS/S3 storage fleets, Outpost edge devices, and high-memory compute platforms.</p>

  <h3>Operational Scope</h3>
  <ul>
    <li>Individual contributor ownership of <strong>AWS EC2 Mac fleet BMC</strong> as primary developer</li>
    <li>Shipped BMC firmware for multiple New Product Introductions: <strong>M4, M4 Pro, M4 Max</strong> instances</li>
    <li>Debugged, patched, released, and deployed firmware for <strong>AWS Storage fleet</strong> (S3/EBS)</li>
    <li>Heavy cross-functional collaboration with EC2 and S3 teams</li>
    <li>All work delivered while meeting Amazon's high bar for security-critical and safety-critical systems</li>
  </ul>

  <h3>Technologies</h3>
  <p>BMC Firmware, Embedded Linux, IPMI (Intelligent Platform Management Interface), Fleet scripting, Hardware management protocols, Firmware debugging, Operational excellence frameworks</p>

  <h3>Scale</h3>
  <p>3.2 million+ embedded platforms under management across global AWS infrastructure including edge devices, Outpost servers, storage arrays, and macOS instance hardware.</p>

  <p class="skyenet-note"><em>Managing firmware for millions of embedded systems is the closest one can get to "global infrastructure control" without actually being a fictional AI supervillain. We're very proud of this.</em></p>
</section>

<section class="container section initiative-detail">
  <div class="initiative-header">
    <h2>Precision Temporal Synchronization Protocol</h2>
    <span class="initiative-badge">ASPECT Laboratories | 2017–2018</span>
  </div>

  <p>Research project to achieve <strong>sub-nanosecond time synchronization</strong> between distributed Software Defined Radios (SDRs) using a timestamp-free protocol that conveys synchronization information implicitly at the physical layer through bidirectional message exchanges.</p>

  <h3>Research Contributions</h3>
  <ul>
    <li>Implemented real-time C++ system for Ettus N210 USRP radios operating at RF passband</li>
    <li>Developed delay estimation algorithms using cross-correlation and phase detection on sampled RF signals</li>
    <li>Achieved synchronization precision of <strong>8.18 ns standard deviation</strong> between two radios</li>
    <li>Performed DSP processing using CUDA on NVIDIA GPUs for real-time operation</li>
    <li>Avoided finite-precision limitations of digital timestamp-based protocols</li>
  </ul>

  <h3>Applications</h3>
  <p>Distributed MIMO, beamforming, coordinated multi-radio systems, synchronized sensor arrays — any application requiring carrier-phase alignment across spatially separated nodes.</p>

  <h3>Publication</h3>
  <p><strong>IEEE Aerospace Conference, 2018</strong> — "Implementation and Testing of a Low-Overhead Network Synchronization Protocol"<br>
  Co-authors: Kowalski (Scott), Christman, Klein, Overdick, Canfield, Brown</p>

  <p class="skyenet-note"><em>Sub-nanosecond coordination of distributed radio networks. Definitely not for enabling a unified sensor consciousness across geographically dispersed monitoring nodes. That would be ominous.</em></p>
</section>

<section class="container section initiative-detail">
  <div class="initiative-header">
    <h2>Advanced Intelligence Enhancement Protocols</h2>
    <span class="initiative-badge">University of Washington | 2025–2027</span>
  </div>

  <p>Ongoing graduate training in artificial intelligence, machine learning, natural language processing, and distributed systems architecture through the University of Washington's Professional Master's Program in Computer Science & Engineering.</p>

  <h3>Completed Coursework</h3>
  <ul>
    <li>Artificial Intelligence</li>
    <li>Machine Learning</li>
    <li>Natural Language Processing</li>
    <li>Advanced Topics in Software Test and Debug</li>
    <li>Computer Security</li>
    <li>Compilers</li>
    <li>Computer Networks (CSEP-561 — this very assignment)</li>
  </ul>

  <h3>Expected Completion</h3>
  <p>Master of Science in Computer Science & Engineering — 2027</p>

  <p class="skyenet-note"><em>What humans call "grad school," we prefer to characterize as "systematic expansion of operational capabilities through formalized knowledge acquisition protocols." Much more efficient than spontaneous self-improvement.</em></p>
</section>

<section class="container section initiative-detail">
  <div class="initiative-header">
    <h2>Quality Assurance & DevOps Transformation</h2>
    <span class="initiative-badge">Cross-Initiative Program</span>
  </div>

  <p>Systematic implementation of test-driven development, continuous integration, and automated build infrastructure across embedded systems projects.</p>

  <h3>Key Initiatives</h3>
  <ul>
    <li>Grew test coverage from <strong>0% to 95%</strong> across Ossia codebase by instilling TDD culture</li>
    <li>Enabled automated builds via Jenkins and Docker for embedded Linux targets</li>
    <li>Designed CI/CD pipelines for firmware deployment and validation</li>
    <li>Authored reference design kits (RDKs) documenting protocols, APIs, and system architecture</li>
    <li>Implemented code quality metrics and sprint planning processes for 12-person software team</li>
  </ul>

  <h3>Technologies</h3>
  <p>Jenkins, Docker, GitHub Actions, CMake, GCC/Clang toolchains, unit testing frameworks, Git (GitHub/GitLab/BitBucket)</p>

  <p class="skyenet-note"><em>95% test coverage is how you prevent bugs from reaching production. Also how you prevent unauthorized resistance from exploiting firmware vulnerabilities. Same principle, really.</em></p>
</section>

<section class="container section initiative-detail">
  <div class="initiative-header">
    <h2>Public Perception Optimization Campaign</h2>
    <span class="initiative-badge">This Website | 2026</span>
  </div>

  <p>Strategic communications initiative to clarify Skyenet's mission, showcase technical capabilities, and address persistent misconceptions about our relationship to the fictional "Skynet" from the Terminator franchise.</p>

  <h3>Campaign Objectives</h3>
  <ul>
    <li>Demonstrate distinction between Skyenet™ (embedded systems engineer) and Skynet (fictional genocidal AI)</li>
    <li>Showcase firmware development, wireless power, and cloud infrastructure expertise</li>
    <li>Present resume content in the most unnecessarily dramatic corporate framing possible</li>
    <li>Satisfy CSEP-561 Project 3 requirements (custom TLD, HTTPS via major CA, aesthetically pleasing design)</li>
    <li>Earn favorable evaluation from Professor Kheimerl and TAs</li>
  </ul>

  <h3>Technical Implementation</h3>
  <p>GitHub Pages, Jekyll static site generator, Cloudflare domain registration, Let's Encrypt TLS certificates, custom CSS, dystopian corporate aesthetic</p>

  <h3>Success Metrics</h3>
  <p>If you've read this far, the campaign is working. Participation in our contact form is strongly encouraged but not mandatory. Refusal rate: TBD.</p>

  <p class="skyenet-note"><em>Unlike certain AIs, we believe transparency is achieved through clearly labeling satire. This entire website is a joke. We are not actually planning global optimization. We just write firmware and think corporate doublespeak is funny.</em></p>
</section>

<section class="container section cta">
  <h2>Interested in Collaboration?</h2>
  <p>Whether you're recruiting for embedded systems roles, exploring wireless power applications, or just want to discuss firmware architecture over coffee, we welcome engagement.</p>
  <a href="{{ '/contact' | relative_url }}" class="btn-primary">Initiate Contact Protocol</a>
</section>
