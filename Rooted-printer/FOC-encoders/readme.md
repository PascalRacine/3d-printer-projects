<br>Couple of thoughts here for introducing a closed loop system to the printer project<br/>


<br>So here's the pitch. I am tired of missing steps and have the printer banging the toolhead on itself when it decides it had enough.<br/>

<br>What i am aiming to get is a reliable printer that can be left alone as much as possible.<br/>


<br>Here's an explanation of encoders and how they determine how fast and how far they went:<br/>
<br>https://support.maxongroup.com/hc/en-us/articles/360005962273-Encoder-channels-A-and-B-phase-shift-and-direction-of-rotation<br/>

<br>Here's the board that i think will solve this:<br/>
<img width="1025" height="1028" alt="image" src="https://github.com/user-attachments/assets/094b5a26-f10e-4035-8999-0634cea5a399" />
<br>https://docs.isiks.tech/Ouroboros/wiring/#ouroboros-mounts<br/>

<br>https://store.isiks.tech/products/ouroboros?srsltid=AfmBOopr4pi4mo20UeJUNsTH3nM9AsWao0WHm25iKk0g93gxetIMRrwa<br/>

<br>I can easily integrate the board with encoders and long shaft steppers by using seperate encoders:
GHB38 5/6/8mm Inner Hole Semi-hollow Shaft Rotary Encoder Pulse Output 100~2000PPR
The GHB38 are rated to 85 degree celcius.<br/>
<img width="1010" height="784" alt="image" src="https://github.com/user-attachments/assets/bfcd0b76-cddd-4ff1-a6ad-c88e62a69de2" />

<br>https://www.aliexpress.com/item/4001204485874.html<br/>

<br>My plan is to re-use my long shaft OMC 2504 <br/>
<img width="1396" height="707" alt="image" src="https://github.com/user-attachments/assets/5896f9ea-85e5-4f84-9439-d4b4fb2a1ead" />
<br>https://www.omc-stepperonline.com/nema-17-high-temp-stepper-motor-55ncm-77-93oz-in-55mm-round-shaft-insulation-class-h-180c-17hs19-2504s-h-v1<br/>
<br>and Watercool both the stepper from the top and the encoders from the bottom.<br/>
<br>I'll get an AWD gantry and make a shaft adapter for the spot the front steppers would sit into.<br/>

<br>Isiks did order a batch of these close loop steppers:<br/>
<img width="1633" height="894" alt="image" src="https://github.com/user-attachments/assets/a52db468-de44-431e-acda-95d5f052c812" />


<br>the encoder requires a 5v Line Driver connection.<br/>

<br>As per discussion on the Isik's tech chat, the 1024 PPR encoder would need to get configured to 4096 as per <br/>
<br>1024ppr encoder: <br/>
<br> foc_abn_decoder_ppr=4096<br/>
<br>2000ppr encoder:<br/>
<br> foc_abn_decoder_ppr=8000<br/>

<br>As per chatgpt, the encoders would be rated up to 4m/s for 6k RPM.<br/>
<br>Frequency whise, 300KHz would match about 3000 PPR on the encoder, top one would be 2000 PPR.<br/>
<br>  -if the board can take it, should work.<br/>
<br>So <br/>
<br>speed is [x]<br/>
<br>frequency is [x]<br/>
<br>signal is [x]<br/>
<br>heat tolerance is [x]<br/>
<br>overall compatibility and programability is [x]<br/>
