# Solar_MPPT

First Method:

Using a boost converter the MPP can be tracked by sampling voltage and current when the transistor is switching.  

If the power is higher when the switch is opening than when it is closing that means the current is too low (and thus the system must increase conduction time).  
![current too low image](https://raw.githubusercontent.com/Xaetral/Solar_MPPT/refs/heads/main/low_current.png "Current Too Low")  

If the power is higher when the switch is closing than when it is opening that means the current is too high (and thus the system must decrease conduction time).  
![current too high image](https://raw.githubusercontent.com/Xaetral/Solar_MPPT/refs/heads/main/high_current.png "Current Too High")  

If it is roughly equal that means we have reached MPP.  
![maximum power point image](https://raw.githubusercontent.com/Xaetral/Solar_MPPT/refs/heads/main/max_power_point.png "Maximum Power Point")  

The image below shows an equivalent circuit of a 100W solar panel with a MPP of around 17V 3A.
![solar panel equivalent circuit image](https://raw.githubusercontent.com/Xaetral/Solar_MPPT/refs/heads/main/solar_panel.png "Solar Panel Equivalent Circuit")  

Second Method:

Still using a boost converter the MPP can be tracked by continuously measuring voltage and current and computing its derivative.  
If it is going up, that means the switch is in the right state.  
If it is going down, that means the switch must be switched.  
Note that for it to not be affected by variation in solar illumination the control loop needs to be substantially faster than these variations.  
![derivative mppt image](https://raw.githubusercontent.com/Xaetral/Solar_MPPT/refs/heads/main/derivative.png "Derivative MPPT")  

Third Method:

Placing a capacitor on the panel output allows discontinuous input current like it is the case with a buck converter.
![buck converter mppt image](https://raw.githubusercontent.com/Xaetral/Solar_MPPT/refs/heads/main/buck.png "Buck Converter MPPT")  
