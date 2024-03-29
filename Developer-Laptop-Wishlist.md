Stuff goes here

Minimum 64 GB RAM for processing.

Need to be able to install Dev tools, vscode, docker etc...
access to teams and outlook emails a nice-to-have

option 1:
Macbook Pro 14 or 16 inch
- 64 GB Ram
- 1TB 
- Admin Privileges

---
## Ben's thoughts

||Ideal|Alternative|
|---|---|---|
|Hardware|Mac Book Air with M2 chip|Data Science laptop|
|Software|Local Admin Privilege's|Full control of a Virtual Desktop|

---

## Jia's laptop wish list:

Macbook Air 13 with M2 chip. (so far I'm also good working on the government issue laptop with access to GCP)

---
## Vivian's Dream State:
-> Outlook and MS Teams accessible from the Public Cloud
-> Cloud9 (https://aws.amazon.com/cloud9/) or Codespaces (https://github.com/f)eatures/codespaces)

That's all I'd need!~

---
## Stephen's tier list (personal preference, options I'd ideally have, not exclusive of other options co-existing):
- Tier 1:
  - bring your own device (BYOD) as an option + external Outlook and MS Teams access
  - BYOD as an option, using iPhone for Outlook and MS Teams (to me, it's not too different)
- Tier 2:
  - PHAC owned and hardware-life-cycle managed ThinkPad as an option, BYO-OS, external Outlook and MS Teams access to sweeten the deal
    - as reference, my own ThinkPad T14 Gen 2 with 16 GB of RAM and a 250GB SSD has been plenty so far. Millage will vary of course, I'm not processing large data locally 
- Tier 3:
  - PHAC owned and life cycle managed MacBooks for everyone; don't mind if management extends to the OS and software patches as long as I have unrestricted admin privileges on the device my self. External outlook and MS Teams access to sweeten the deal
...
- Tier 999:
  - local admin and developer environment support on corporate windows laptops. They'll need to be _very_ beefed up to handle the unremovable bloatware these come with. Windows as our dev OS will be a challenge, and local VMs for linux are just further bloat/points of failure. Principle of least surprise is out the window, as software and policy changes designed and tested for standard corporate use (non admin, limited set of software) can blow up our dev environments at any time
  - developer environments on remote _corporate_ virtual machines, accessed from existing corporate hardware. I've seen it before and it cost a bundle and wrecked productivity right down to the second-to-second input delay. It's also a lot of points of failure than a local machine, and is entirely dependent on internet access
    - I'd trust public cloud dev env options like Cloud9 or Codespaces more, but I've not explored them enough to really judge them. They do share a reliance on stable internet access

## Stephen's thoughts in greater depth:
Personally, I prefer a BYOD option. Not saying that should be the default or imposed on anyone, but it's what I'd take for my self if at all possible. My personal dev machine is customized from the OS on up, I've got muscle memory with it and have a good idea what's going on with it (principle of least surprise). For my own developer experience and efficiency, it's as good as it gets.

I can even take or leave access from that device to Outlook and MS Teams; I've found the work iPhone to be sufficient for the majority of "on network" communications (although opening up MS Teams at least would be a big nice-to-have). Whatever we do, we'll need to get on the corporate laptops occasionally for intranet resources or to view any sensitive documents, although I've always found that to be a couple-times-a-week need at most.

Between zero trust and working in the open (even our private GitHub repos must be 100% unclassified content), there shouldn't be a security imperative to develop in managed dev environments. Yes, managed and monitored dev environments provide better security posture (maybe) and visibility (true, although our zero trust boundaries should provide visibility where it matters most), but I think it's marginal for us and should be compared against costs to dev efficiency.

----

Not really a developer, so the biggest problem that I notice is not being able to install/use the most basic things like a shell...admin privileges is already stated, but I want to add my name so that it's clear that lots of people feel this way! - Kat

I personally also agree with BYOD, developers are most comfortable with their own computers and having an extra computer that can do the same as our own is not necessary. Opening up MS Teams and Outlook to external access will be the best solution while keeping government applications locked to our work laptops. All applications on our laptops already have locked access with our Entrust Digital IDs which is why I think unlocking our PHAC emails to be accessed externally can be viable. - Kajan

## ZACHARY's THOUGHTS

After conversations yesterday, Jia mentioned that VMs in GCP can be converted to Virtual Desktop Environments w/ various operating systems and open admin rights. These could be possibly scaled on-demand to meet RAM/Core/vGPU requirements?  This is like what NRCAN provided StatCan supporting PHAC during the COVID TF, and it proved to be nimble and powerful enough....However, if physical laptops are going to be the path: unfortunately the new Macbooks are not compatible with our current GIS software needs and the chipset does not allow for virtualization or dual-boot. Therefore, I'd be looking for something with minimum 64 GB RAM, 16 core, some sort of GPU, and SSD storage, Windows 11 based, and local admin. "...Mac systems configured with Apple Silicon (Mx), or non-Intel processors, are not compatible until Microsoft Windows OS environments are supported on Apple processors. If you already have an incompatible Mac and want to run ArcGIS Pro, consider the following options:

Connect to a supported on-premises hosted VM.
Deploy and connect to a cloud-hosted VM."

If none of these are viable ^^^^ then a _subsidized_, BYOD environment would be the best. My home tower is probably cheaper for me to procure and would take less time to hit the ground running than waiting for a 10 year study and getting something underpowered/unusable or

https://store.minisforum.com/collections/amd-%C2%AE-ryzen-%C2%AE/products/elitemini-hx90g?variant=44023099228405


Neptune HX77G/HX99G/HX80G

Sale price USD $879.00
Neptune Series HX99G is powered by AMD Ryzen™ 9 6900HX and AMD Radeon™ RX 6600M
Minisforum HX99G

Processor

AMD Ryzen™ 9 6900HX, 8 Cores/16 Threads
(Total L2 Cache 4MB , Total L3 Cache 16MB , Base Clock 3.3 GHz , up to 4.9 GHz)

GPU

AMD Radeon™ RX 6600M(GDDR6 8GB)

Memory

DDR5 Dual channel (SODIMM Slots×2)

Supports a maximum of 64GB (32GB x 2) of DDR5

Storage

M.2 2280 PCIe4.0 SSD (up to 2TB)

Storage Expansion

M.2 2280 SSD Slot (Support NGFF SATA or NVMe PCIe4.0 SSD)

Wireless Connectivity

M.2 2230 WIFI Support (Wi-Fi 6，BlueTooth 5.2)

Video Output

① HDMI (4K@60Hz) ×2

② USB4 (8K@60Hz)×2

Audio Output

HDMI ×2, Headphone Jack ×1

Ports & Buttons

RJ45 2.5 Gigabit Ethernet Port ×1
USB3.2 Gen1 Type-A Port ×1 (Front)
USB3.2 Gen1 Type-C Port ×1 (Front)
USB3.2 Gen1 Type-A Port ×2 (Rear)
USB3.2 Gen2 Type-A Port ×1 (Rear)
USB4 Type-C Port ×2
HDMI ×2
Clear CMOS ×1
Microphone Jack ×1
Headphone Jack ×1

Power

DC 19V (Adapter Included)

System

Windows 11

Product Dimension

205*203*69.3 (mm) / 8.07*7.99*2.73 (inch)

Package Dimension

233*233*160 (mm) / 9.17*9.17*6.3 (inch)

Net Weight

1.21 kg (2.67 lbs)

Package Weight

2.72 kg (6 lbs)

Package Content

HX99G × 1
Power Adapter × 1
Power Cable × 1
HDMI Cable × 1
Base Support Frame × 1
Base Bottom Plate × 1
Technical Documents × 1
Mounting Screw Set × 1
***

## Bainers Bargain

This is the deal I would make with the desktop crew. I(my director) will absolve you of all risk in the management and support of my work device and in turn I will take on the responsibility of providing my own patching, scanning and technical support. As part of this trade, you will give me access to local admin AND access to the Windows Defender reports for this device.

I only need a modern laptop, 32gb of ram and a SSD. If I can get local admin, all I want to install on the Windows side is WSL2. 

