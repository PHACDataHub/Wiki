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
Vivian's Dream State:
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

Between zero trust and working in the open (even out private GitHub repos must be 100% unclassified content), there shouldn't be a security imperative to develop in managed dev environments. Yes, managed and monitored dev environments provide better security posture (maybe) and visibility (true, although our zero trust boundaries should provide visibility where it matters most), but I think it's marginal for us and should be compared against costs to dev efficiency.