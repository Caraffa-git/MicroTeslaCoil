# μTeslaCoil
Small PCB for push-pull tesla coil with 50V boost converter

![schematic](/img/schematic.png)

## Notes and test results (<a href="https://github.com/Caraffa-git/MicroTeslaCoil/tree/b3fdc67581c9563461222aec662bbb1328c567a8">b3fdc67</a>)
The coil works, but aside from some not-so-wise design decisions that I changed in the current version, I encountered a few problems.
- At first the idea was to use a slayer-exciter sized secondary but as it turned out driving a coil with a frequency close to 5MHz can be challenging. I ended up using a slightly larger secondary with a resonance frequency close to 500-600kHz.
- The lack of TVS diodes cost me some IGBTs so I added them in this version. As it turns out, reverse connection of the primary winding causes high voltage spikes and thus damage to the circuit.
- The inverter I used has a limit of ~60V output, but as it turns out we have some headroom (voltage spikes reach ~120V where IGBTs are rated at 200V) so you can experiment with another inverter. I think the circuit should be able to withstand about 80V on the input.

|   |   |   |
|---|---|---|
| ![Photo 2](/img/PIC_2.png) |![Photo 3](/img/PIC_3.png) | ![Photo 4](/img/PIC_4.png)|

![](/img/PCB_1.png)
![](/img/PCB_2.png)
![base](/img/PIC_1)

## TODO
- Add Q3 gate protection
- Add U2 VCC regulation/protection 

## Links
https://www.youtube.com/watch?v=w9AY5RUtEMk   
https://tefatronix.g6.cz/display.php?page=sstc4&lang=en   
~~https://blog.naver.com/3happy3gong3/222702706706~~   
https://github.com/Caraffa-git/PCB-Art