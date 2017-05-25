# odocs.megam.io
Onboard cloud documentation

This is the documentation for the onboard cloud project which helps to unpack, configure hardware to top $$$.

# Motivatioin

Historically we had tries many times using 
## [USB with ISO](https://github.com/megamsys/gitpackager/tree/master/megdc/usb) 

This would install the customized operating system based on ubuntu 14, an agent, and start an control pane inside an
on premise datacenter to do that what they want. The control pane was built using `golang` and had a web interface. 

This inherently has tight order of unpacking vanilla hardware to cloud using a specific order that an admin would do via USB.
![USB](/images/megam_dc.png?raw=true "USB")
![Booted](/images/megam_usb.png?raw=true "OS booted")

This had limitation to control and manage additional hardware using cobbler. But in a datacenter we find machines running already and are provided an SSH ability to connect to. This process was rigid and too much packed including HA and not fully working well.

## [megdc CLI like ceph-deploy](https://github.com/megamsys/megdc)

We found that the key stakeholders who would manage the infrastructure will be  **administrators**, the core of what was built above was converted to pluggable templates based on [Urknall](https://github.com/dynport/urknall) using SSH tunneling. The part to install packages on an operating system using "deb" was easy. But the part to configure the installed software to our need was painfull. Not to mention, the upgrades, rollback on failure.

This mode has the imperative behaviour of saying "get into this node", "install this", then do this.

## [SaaS OnboardCloud valpha](https://github.com/megamsys/onboardcloud) *private repository*


## [SaaS OnboardCloud v1](https://github.com/megamsys/onboardcloud) *private repository*



