# FullDuplex_Signaling

First Method:

Using a boost converter the MPP can be tracked by sampling voltage and current when the transistor is switching.  

If the power is higher when the switch is opening than when it is closing that means the current is too low (and thus the system must increase conduction time).  
![current too low image](https://raw.githubusercontent.com/Xaetral/FullDuplex_Signaling/refs/heads/main/low_current.png "Current Too Low")  

If the power is higher when the switch is closing than when it is opening that means the current is too high (and thus the system must decrease conduction time).  
![current too high image](https://raw.githubusercontent.com/Xaetral/FullDuplex_Signaling/refs/heads/main/high_current.png "Current Too High")  

If it is roughly equal that means we have reached MPP.  
![maximum power point image](https://raw.githubusercontent.com/Xaetral/FullDuplex_Signaling/refs/heads/main/max_power_point.png "Maximum Power Point")  

The image below shows an equivalent circuit of a 100W solar panel with a MPP of around 17V 3A.
![solar panel equivalent circuit image](https://raw.githubusercontent.com/Xaetral/FullDuplex_Signaling/refs/heads/main/solar_panel.png "Solar Panel Equivalent Circuit")  

Second Method:

Using a buck converter the MPP can be tracked by continuously measuring voltage and current and computing its derivative.  
If it is going up, that means the switch is in the right state.  
If it is going down, that means the switch must be switched.  
Note that in real condition with varying amount of illumination and thus power output, the derivative must be compared to its previous value instead of zero.  
![buck mppt image](https://raw.githubusercontent.com/Xaetral/FullDuplex_Signaling/refs/heads/main/buck.png "Buck MPPT")  
