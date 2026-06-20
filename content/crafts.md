This is a personal collection of all my current and previous projects, including tweaks I've for this website!

## About what I do

Pretty much the blue-collar of the IT world. I've maintained, deployed and implemented efficient processes, monitoring services and custom devices to improve data center efficiency and operational effectiveness all over the world.

#### Data center energy saver

This [[https://github.com/gagisc/dc-energy-savings|project]] uses Fuse FLIR A310 thermal video and DS18B20 contact sensors connected to a raspberry PI to to reduce hotspot detection latency by 60% and also reduce reactive cooling costs by 18%. 

I got an opportunity to test out this similar architecture at one of the many data centers I've had the opportunity to work at. A lot of factors go into fine tuning your energy consumption, as you need to know the mass of the air, cooling system capacity and the heat capacity of air calculated by:

```
\textbf{Energy to cool by } 1^\circ\mathrm{C}:\[Q = m c_p \Delta T\]where\[m = \rho V,\qquad \Delta T = 1^\circ\mathrm{C}\]
\textbf{Cooling time estimate (with constant cooling power }P\text{):\[t \approx \frac{Q}{P} = \frac{m c_p \Delta T}{P}\]\textbf{Note:} The effective cooling power (cooling capacity) generally decreases as the space temperature approaches the setpoint, so $P$ may depend on temperature; the time estimate assumes $P$ is approximately constant over the interval.
```

#### Intune Self-Heal

A little [project](https://github.com/gagisc/intune-selfheal) that detects devices with enrolment issues and auto-remediates by doing basic troubleshooting like device sync, MDM token refresh or re-create the enrolment token and restart the Intune management extension. Logs everything to Grafana post-execution.

#### This website

I've [customized](https://github.com/gagisc/gagisc.github.io) this website from the original Quartz 5 repo. A big thanks to all the amazing contributors and maintainers who made the project possible. Quartz 5 is a packaged website deployer that allows anyone to easily modify and upload their Obsidian notes directly into their website. A very cool concept that helped me learn and improve programmatically as well.
	About what's been done on this website:
	- Background Lain graphics implemented from the Hyperlain rice
	- Color theme added as well as cstom cvss config to sync match and fade the dark and light themes.
	- All custom pages, hand-written!
No AI was used to make any part of this project :smile:
