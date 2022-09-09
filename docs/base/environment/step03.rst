Create a pair of virtual machines
=================================

**Objective**: Create a pair of virtual machines to host your application 

**Why**

A *virtual machine* was originally defined by Popek and Goldberg as *an efficient, isolated duplicate of a real computer machine.* Current use includes virtual machines that have no direct correspondence to any real hardware. The physical, *real-world* hardware running the VM is generally referred to as the 'host', and the virtual machine emulated on that machine is generally referred to as the *guest*. A host can emulate several guests, each of which can emulate different operating systems and hardware platforms.

Reference: https://en.wikipedia.org/wiki/Virtual_machine

Applications hosted on these virtual machines will be made secure, highly-available, and expose analytics, through various F5XC, NGINX, and BIG-IP challenges.

**How**

Microsoft Azure:
  - https://docs.microsoft.com/en-us/learn/modules/create-linux-virtual-machine-in-azure/

Amazon Web Services:
  - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html

Google Cloud Platform:
  - https://cloud.google.com/compute/docs/create-linux-vm-instance