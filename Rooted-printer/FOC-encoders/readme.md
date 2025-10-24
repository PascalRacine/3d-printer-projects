Couple of thoughts here for introducing a closed loop system to the printer project


So here's the pitch. I am tired of missing steps and have the printer banging the toolhead on itself when it decides it had enough.

What i am aiming to get is a reliable printer that can be left alone as much as possible.

Here's the board that i think will solve this:
<img width="1025" height="1028" alt="image" src="https://github.com/user-attachments/assets/094b5a26-f10e-4035-8999-0634cea5a399" />
https://docs.isiks.tech/Ouroboros/wiring/#ouroboros-mounts

https://store.isiks.tech/products/ouroboros?srsltid=AfmBOopr4pi4mo20UeJUNsTH3nM9AsWao0WHm25iKk0g93gxetIMRrwa

I can easily integrate the board with encoders and long shaft steppers by using seperate encoders:
GHB38 5/6/8mm Inner Hole Semi-hollow Shaft Rotary Encoder Pulse Output 100~2000PPR
The GHB38 are rated to 85 degree celcius.
<img width="1010" height="784" alt="image" src="https://github.com/user-attachments/assets/bfcd0b76-cddd-4ff1-a6ad-c88e62a69de2" />

https://www.aliexpress.com/item/4001204485874.html

My plan is to re-use my long shaft OMC 2504 
<img width="1396" height="707" alt="image" src="https://github.com/user-attachments/assets/5896f9ea-85e5-4f84-9439-d4b4fb2a1ead" />
https://www.omc-stepperonline.com/nema-17-high-temp-stepper-motor-55ncm-77-93oz-in-55mm-round-shaft-insulation-class-h-180c-17hs19-2504s-h-v1
and Watercool both the stepper from the top and the encoders from the bottom.
I'll get an AWD gantry and make a shaft adapter for the spot the front steppers would sit into.

Isiks did order a batch of these close loop steppers:
<img width="1633" height="894" alt="image" src="https://github.com/user-attachments/assets/a52db468-de44-431e-acda-95d5f052c812" />


the encoder requires a 5v Line Driver connection.

As per discussion on the Isik's tech chat, the 1024 PPR encoder would need to get configured to 4096 as per 
1024ppr encoder: 
 foc_abn_decoder_ppr=4096
2000ppr encoder:
 foc_abn_decoder_ppr=8000

As per chatgpt, the encoders would be rated up to 4m/s for 6k RPM.
Frequency whise, 300KHz would match about 3000 PPR on the encoder, top one would be 2000 PPR.
  -if the board can take it, should work.
So 
speed is [x]
frequency is [x]
signal is [x]
heat tolerance is [x]
overall compatibility and programability is [x]
