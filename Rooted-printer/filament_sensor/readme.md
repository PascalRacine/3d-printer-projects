Filament sensor using an IR sensor with a 5mm gap.
The sensor enables enough plastic mass in the middle to properly clean the hole with reamers.
<br />
<p>Tools to get:<br />
-2mm Reamer;<br />
-4mm reamer; and<br />
-M10 bottoming tap. (not really required)</p>
<br />
<p>Hardware to get:<br />
m2.5 12mm long screws<br />
m2.5 hex nut</p>
<br />
<p>sensor:<br />
-https://www.digikey.ca/en/products/detail/omron-electronics-inc-emc-div/EE-SX3164-P2/6946429<br />
-https://www.digikey.ca/en/products/detail/omron-electronics-inc-emc-div/EE-5002-1M/8124128</p>
<p>There are other 5mm sensor in the same brand, you need the 5vDC version(ideally you got a 3pin sensor on your board that has 5v rather then 3.3v):<br />
<img width="1293" height="662" alt="image" src="https://github.com/user-attachments/assets/3f072c6e-2eb5-43ee-b6aa-209dbecc00d0" />
<img width="172" height="202" alt="image" src="https://github.com/user-attachments/assets/2daddfbe-a517-4d5a-b38f-15d620607ab4" /></p>
<p>The sensor is rated from -20C to 85C
this is the pinout for the sensor:<br />
<img width="1242" height="810" alt="image" src="https://github.com/user-attachments/assets/95d0a1e9-3da6-4e51-b135-09d4dbb0c776" />

<p>Connector:<br />
if you want to get the connector and pin it yourself, but i would recommend the pre-crimped cables:<br />
https://www.digikey.ca/en/products/detail/jst-sales-america-inc/GHR-03V-S/807815?s=N4IgTCBcDaIOIAkBKBaADAZgGooMoAIQBdAXyA <br />
the cheapest and lowest amount of pins to buy is in packs of 100 tho<br />
https://www.digikey.ca/en/products/detail/jst-sales-america-inc/SSHL-002T-P0-2/27687535 <br />




<p>fitting:<br />
either: <br />
-M10 coupler for 4mm ptfe tube or;<br />
-ecas04 fitting</p>

<p>I got a BTT EZ-Max board which gives me endstop pins with 5VDC
<img width="313" height="67" alt="image" src="https://github.com/user-attachments/assets/34185f81-6a57-4b89-b46c-262b57f64135" /></p>

<p>When testing the sensor with a 5v DC power source, i get 0.7V or 0V.
this is the klipper configuration:</p>

<p>Please let me know if you got a better klipper config for this.</p>

<p>[filament_switch_sensor switch_sensor]
switch_pin: ^!PF2<br />
pause_on_runout: True<br />
runout_gcode:<br />
&nbsp;    SET_IDLE_TIMEOUT TIMEOUT=7200 ; Increase idle timeout<br />
&nbsp;    M118 Filament empty<br />
insert_gcode:</p>


<img width="459" height="756" alt="image" src="https://github.com/user-attachments/assets/6f86f711-c1e5-4c7d-98e0-1ac642e53f28" />

<img width="682" height="568" alt="image" src="https://github.com/user-attachments/assets/29664ed1-466d-445d-b54e-757056359ea6" />

<img width="691" height="615" alt="image" src="https://github.com/user-attachments/assets/bcf373c9-a1f6-49b3-ac69-73162ce4d813" />
