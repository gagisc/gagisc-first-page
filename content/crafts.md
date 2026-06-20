This is a personal collection of all my current and previous projects, including tweaks I've for this website!

## About what I do

Pretty much the blue-collar of the IT world. I've maintained, deployed and implemented efficient processes, monitoring services and custom devices to improve data center efficiency and operational effectiveness all over the world.

#### Data center power guardian

This [project](https://github.com/gagisc/Power-Guardian) was made by me to detect power anomalies within the Eaton ePDU G3, APC Smart-UPS SRT and Schneider Galaxy UPS systems. We were also later able to improve the energy efficiency by detecting over-provisioned PDUs to save energy. This was needed as some of the data centers where this test was run did not have the required infrastructure to power their local grids back with the excess power (still in construction at that point in time).

All values here are simulations, which will need to be replaced with real world APIs and SNMP pollers to collect and push logs to grafana or prometheus. Since this project does not run on real world devices, additional tweaks WILL be needed before this is deployed in production.

Finally, I wanted to point out that, maintaining these sensors and adjusting the PDUs were most of the work that went into making sure that all systems were working as expected. On some days, manual intervention was needed to fix sensors 40 feet high and sometimes, the system would auto-remediate based on configured guardrails and processes.

#### Data center energy saver

This [project](https://github.com/gagisc/dc-energy-savings) uses Fuse FLIR A310 thermal video and DS18B20 contact sensors connected to a raspberry PI to to reduce hotspot detection latency by 60% and also reduce reactive cooling costs by 18%. 

I got an opportunity to test out this similar architecture at one of the many data centers I've had the opportunity to work at. A lot of factors go into fine tuning your energy consumption, as you need to know the mass of the air, cooling system capacity and the heat capacity of air calculated by:

$$ 
t = \frac{C}{U A} \ln\!\left(\frac{T_{\text{room}} - T_{\text{out}}}{T_{\text{room}} - 1 - T_{\text{out}}}\right) \quad 
$$
 
$$ 
\text{where } \newline 
t=\text{time to cool by }1^\circ\text{C},\; \newline 
C=\text{thermal capacitance J/}^\circ\text{C},\; \newline 
U=\text{overall heat transfer coefficient},(BTU/hr·ft^2·^\circ F or W/m^2·^\circ C)\; \newline 
A=\text{heat transfer area}, (\text{ft}^2 \text{ or m}^2) \; \newline
T_{\text{room}}=\text{initial room temperature},(^\circ F or ^\circ C)\; \newline
T_{\text{out}}=\text{outside temperature}, (^\circ F or ^\circ C) 
$$

The case study shown in this project was a (simulated) reading that was monitored over a set period before landing at a raise of a 2 degree setpoint for 10 minutes. This varies extremely between data centers and spaces inside the data center. For larger and tier 3 data centers, it is recommended to use professional monitoring solutions that use hundreds of sensors to control and detect anomalies in the cooling and electrical systems.

A major part of this project was maintaining the sensors and the pi boards to ensure smooth operation. Fixing pipes and leaks in the cooling system was also a part of the job that went into daily checks and PMVs. Finally, it is important to keep in mind that scaling involves more sensors, more points of failures and also more maintenance. The advantage of automation is the speed at which we can deploy solutions, not that we can offload responsibility to a machine. As I've developed more skills and taken on more responsibilities, I've become that much more proficient at it.
#### Intune Self-Heal

A little [project](https://github.com/gagisc/intune-selfheal) that detects devices with enrolment issues and auto-remediates by doing basic troubleshooting like device sync, MDM token refresh or re-create the enrolment token and restart the Intune management extension. Logs everything to Grafana post-execution.

#### This website

I've [customized](https://github.com/gagisc/gagisc.github.io) this website from the original Quartz 5 repo. A big thanks to all the amazing contributors and maintainers who made the project possible. Quartz 5 is a packaged website deployer that allows anyone to easily modify and upload their Obsidian notes directly into their website. A very cool concept that helped me learn and improve programmatically as well.

About what's been done on this website:
- Added the lain background graphic from the [hyprlain](https://github.com/gagisc/Hyprlain) rice for linux systems
- Added the background night and day themes
- All custom, hand-written pages!


**No AI was used to make any part of this project and website** 😃