# UltraStation
### A Scalable Workstation System based around PCIe interconnect

---
## FAQs
### Why?
###

### Allow for Scalable yet manageable systems
A lot of workloads need multiple hosts and/or a huge load of peripherals to be connected and managed.
- Traditional Deskside Chassis and Rackmount Cases do not scale well and are physically constrained in terms of expansion options.
###

### Enable bigger Systems
Being able to hook up a lot of Storage, Accelerators, Interfaces and other Expansions beyond the limits of classical Chassis configurations does have a lot of nieche applications that are underserved.
- For example to allow for commercial off-the-shelp designs in A/V production and broadcast as well as Rendering and CAD workloads.
###

### Establish a multi-vendor & multi-provider Standard for facilitating these demands
This will keep costs down, increase adoption and enhance operability.
- By only specifying the necessities and allowing for maximum flexibility, the Systems Integrators can customize the Setup to the needs and constraints of it's Use-Case.

##
### How?
Use of Common, off-the-shelf standards and solutions.
###

### [19" Rackmount](https://en.wikipedia.org/wiki/19-inch_rack)
This keeps costs for cases down whilst also providing means of mechanically mounting said components in a safe and secure manner.
###

### 48V DC Power Rails
This reduces the need for multiple power supplies whilst also easing integration into varying electricity Standards and Setups as well as UPSes and Redundency.
- Utilizing [OpenCompute Power Systems](https://www.opencompute.org/projects/rack-and-power) to allow for high-density yet affordable systems.
###

### Centralized Airflow and [liquid cooling system](https://en.wikipedia.org/wiki/Computer_cooling#Liquid_cooling)
In line with rackmount conventions, the System will pull in cool ambient air from the front and exhaust hot air to the rear.
- A [Massive radiator at the rear](https://www.youtube.com/watch?v=tbRe1k2k0ow) is being used to utilize a high-pressure & high-flow rate cooling solution to keep components at reasonable temperatures.
  - [Spill-free couplings](https://www.staubli.com/global/en/fluid-connectors/products/quick-and-dry-disconnect-couplings/thermal-management/sph-ba-cg-aluminum-bayonet.html) allow for the addition or removal of units with ease.
  - Using [Propan-1-ol](https://en.wikipedia.org/wiki/Propan-1-ol) as coolant at ambient pressure allows for a wide temperature range of -100°C - 80°C.
  - Alternatively, use of Water at [subambient pressure](https://www.engineeringtoolbox.com/water-evacuation-pressure-temperature-d_1686.html) may yield options for [two-phase systems](https://en.wikipedia.org/wiki/Coolant#Two-phase) but is disrecommended due to the vacuum requirement and the safety issues re: electronics. 
    - However the specification isn't fixed yet so a [boiling liquid cooling loop](https://www.youtube.com/watch?v=RXNAbVi1j6k) may still be in the cards.
- Support for external cooling loops via a [shell and tube](https://en.wikipedia.org/wiki/Shell-and-tube_heat_exchanger) [heat exchanger](https://en.wikipedia.org/wiki/Heat_exchanger) is easily possible with the design, so [whole-room watercooling](https://www.youtube.com/watch?v=b8bLtg9J1Oc&list=PL8mG-RkN2uTyVqLN5OSZxn3Z4t1_xFunu) and other [central heat managment solutions](https://www.youtube.com/watch?v=BpNf4wYNPWo) can be used, which reduce inefficiencies through conversion compared to A/C -> Ambient Air.
- [Immersion-based liquid cooling](https://www.youtube.com/watch?v=fQfolP7NoNc) has been discarded as of yet due to compatibility issues with components.
  - The lack of easy access to [good cooling fluids certified](https://www.youtube.com/watch?v=RyFoNDa0pbI) for [that use-case](https://www.youtube.com/watch?v=YyKIZPuepl8) and subsequent costs of the system make it a [more expensive solution that is harder to maintain and integrate](https://www.youtube.com/watch?v=U6LQeFmY-IU) by virtue of being not compatible with existing solutions.
    - The ability to put an UltraStation [deskside like a traditional High-End Workstation](https://www.youtube.com/watch?v=5TRr2oWeSw0) is key to it's useability and accessibility.

###
### (Optical) [PCI Express](https://en.wikipedia.org/wiki/PCI_Express) - based Interconnect
Using [SFF-8644 Connectors](http://sup.xenya.si/sup/info/finisar/SFF-8644.pdf) to allow for transparent PCIe cabling solutions.
- This allows the use of cheap [off-the-shelf adaptors](https://dolphinics.com/products/MXH932.html) as well as [copper](https://www.dolphinics.com/products/PCI_Express_Gen4_SFF-8644_cables.html) and espechally [active optical cables](https://www.dolphinics.com/download/CABLES/MSFC4xM_Product_Brief.pdf) to interconnect the components.
###

### [PCI Express](https://en.wikipedia.org/wiki/PCI_Express) Switched "Backplane"
Using a [Switch for the high-speed PCIe-based interconnect between modules](http://www.dolphinics.com/products/MXS924.html) provides a transparent yet efficient way to access multiple peripherals beyond the amount of directly interconnectable lanes.
- This also allows for multiple-host/targets to be used and provide a more stable option than the [low-end narrowband solutions used in many cases](https://www.aliexpress.com/item/PCI-E-1X-Expansion-Kit-1-to-4-Ports-Switch-PCIe-x16-slots-Multiplier-Hub-Riser/32818453487.html).
###

### Ethernet-Based "Control Plane"
Utilizing [PoE and Gigabit Ethernet to manage modules, backplanes and hosts](https://eu.store.ui.com/eu/en/collections/unifi-switching-pro-power-over-ethernet) with ease.
- This also allows for [Lights-Out-Managment](https://www.techtarget.com/searchdatacenter/definition/lights-out-management) of components and thus ["warm-swapping"](https://en.wikipedia.org/wiki/Hot_swapping) of components not designed to be hot-swappable.
###

---
##

---
## Acknowledgements
### [SiliconGraphics Computer Systems](https://en.wikipedia.org/wiki/Silicon_Graphics) / sgi 
#### [Onyx](https://en.wikipedia.org/wiki/SGI_Onyx)
This is one of the main inspirations for the UltraStation.
- A [scalable yet modular System Architecture](https://www.youtube.com/watch?v=Bo3lUw9GUJA&t=190s) that allows for reconfiguration and upgrades of the System.
###### For those interested in it, Dodroid [made an excellent video about it](https://www.youtube.com/watch?v=Bo3lUw9GUJA) to checkout.
#### [SN1 / SN-MIPS-based Systems](https://www.youtube.com/watch?v=lEcw_oTKTa0&t=1408s) like the Onyx3000.

##
### An expired Trademark
There [has been a trademark for the name UltraStation](https://register.dpma.de/DPMAregister/marke/register/395501105/DE) which lapsed in 2005 under the Register DE39550110.
