# date:07/8
# time spent:1.5hr
## description:
To plan my custom handheld Wi-Fi and Bluetooth signal tracker, I researched open-source RF detectors and electronics suppliers to select components that balance precision, portability, and performance. For the brain, I chose the compact **ESP32-C3** microcontroller to handle wireless scanning and system logic, pairing it with an **AD8318 RF power detector** module and an **SMA antenna** for accurate signal measurement. I paired this with a vibrant **2.4" SPI TFT display** for real-time signal readout, seamlessly navigated using an **EC11 rotary encoder** with an integrated push button. The device is powered by a rechargeable **3.7V Li-ion battery**, featuring a **USB-C port** backed by an **MCP73831 charger IC** and a **600mA AP2112K 3.3V LDO** to keep power steady during heavy wireless bursts. For instant feedback, I incorporated a multi-sensory alert system with a **WS2812B RGB LED**, an **active buzzer**, and a **coin vibration motor**, plus a **1W white LED flashlight** and battery voltage monitoring for practical field use.
# images:
<img width="1431" height="515" alt="image" src="https://github.com/user-attachments/assets/c44a5362-58dc-4d1c-b7ae-1a77b365cb0f" />

------
# date:07/8
# time spent:1.25hr
## description:
First i started gathering the footprints of each part and then i had started with the usb c receptable port for the part and then connected them with the resistor.
ANd then the MCP73831 charger topping off your 3.7V battery at 500 ma while lighting up a status LED while it charges.
then i starteD placed a main power switch right after the battery so you can flip the tracker on or off whenever you want, even while it's plugged in and charging.
That battery power goes into the AP2112K regulator, which tames the fluctuating battery voltage 3.0V into a super stable 3.3V parts.The next part is the Esp module which is the main part of the device.
# images:
<img width="321" height="342" alt="image" src="https://github.com/user-attachments/assets/c3034b0a-92c2-4c27-ac2e-7c68ac60ac56" />
<img width="441" height="389" alt="image" src="https://github.com/user-attachments/assets/8cb2ae33-7288-4429-989b-bd32eaa94e9a" />
<img width="796" height="509" alt="image" src="https://github.com/user-attachments/assets/c40f7d2d-e94c-48e9-bd92-7db0f2963520" />

------
# date:08/8
# time spent:1.5hr
## description:
First i started searching for the displays in online and then i had found the ili9341 display which suits my design and then i need to add the main part of the project that is the esp microcontroller that i had taken the model:ESP32-C3-WROOM-02 and then i had connected the microntroller with display and then i had connected USB data lines (D- on gpio18 and D+ on gpio19) for direct USB-C programming and added a 1x5 pin header as a backup UART debugging interface.ANd then connected the gpio7,gpio8 to the usb c port .
# images:
<img width="662" height="496" alt="image" src="https://github.com/user-attachments/assets/32a1b8fb-c3a9-44fe-b39c-c7fd32f93a56" />
<img width="286" height="393" alt="image" src="https://github.com/user-attachments/assets/4ceb8f89-4f9b-4b3f-8259-4dcf05c4a495" />

------
# date:08/8
# time spent:1.25hr
## description:
I had started the rf adapter part in which first i had started checking the docs of the AD8318ACPZ-REEL7 and i found how to use these connections and then connected it with the j3 coaxial jack and then i connected the rf adapter to the esp-s3 module.
# images:
<img width="298" height="293" alt="image" src="https://github.com/user-attachments/assets/fe2b78f0-9c69-4645-b0cf-595f770bf833" />
<img width="1101" height="819" alt="image" src="https://github.com/user-attachments/assets/4388931b-fa7e-4fd2-ad86-b7d89c3ba3c2" />

------
# date:08/8
# time spent:1.5hr
## description:
I had started with the implemententaion with a battery voltage monitor using a symmetric voltage divider formed by two 100k resistors,this safely halves the variable battery voltage and then i also added a buzzer to the devicce so that tehre would be some sound when we feel the frequency,and then i connected the buzzer with the esp s3 controller,and then i had checked about thevibration motor which provides some vibration when there is a signal and it links like the same as the buzzer and then i connected it with the esp-s3 controller and then i had added a schotkeyy devicce for the circuit
# images:
<img width="426" height="252" alt="image" src="https://github.com/user-attachments/assets/b2a5b6a6-d673-49ed-86b2-8e0da35bad78" />
<img width="398" height="330" alt="image" src="https://github.com/user-attachments/assets/0f3be9a2-ad3a-49a8-833c-f28fb3de1da7" />
<img width="565" height="372" alt="image" src="https://github.com/user-attachments/assets/1293e0f3-d62b-4265-a562-62978bf8608d" />

------
# date:08/8
# time spent:1.75hr
## description:
I had started building the led WS2812Brgb in the circuit for the knowing the status in for the signal detector (red-strong,yellow-normal,green-weak),and then i also added in the an led flashlight in the circuit and then Powered directly from VBAT_SYS and then added 100ohm pull-down holds the MOSFET.Then i added an rotatory encoder which needed gpio pins ,but all were ussed in the esp-s3 module so i have added and extender to the sda,scl line and then connected it to the rotatory encoder to it.
# images:
<img width="347" height="272" alt="image" src="https://github.com/user-attachments/assets/f7d9936f-a842-445c-951a-1809d05ca57c" />
<img width="413" height="263" alt="image" src="https://github.com/user-attachments/assets/496a094a-d405-44c1-b72a-8ab98ba29aee" />
<img width="260" height="212" alt="image" src="https://github.com/user-attachments/assets/e66bdcc8-8a9d-46e5-9e27-d54d19006d2e" />
<img width="445" height="201" alt="image" src="https://github.com/user-attachments/assets/4111a3c6-5b87-4840-beed-343b20a9e131" />
<img width="541" height="431" alt="image" src="https://github.com/user-attachments/assets/0819f1ea-fa1b-4a54-b969-b3b317d6beba" />

------
# date:08/8
# time spent:0.75hr
## description:
First i had started running the erc ,in that i had many errors which were nearly 20 and then i had to go through each one and then fix them ,many were regarding the no connections in the pins of the parts and then some errors were regarding the classic kicad power output ,so i added each pwr_flag to the points where there was a problem
# images:
<img width="709" height="468" alt="image" src="https://github.com/user-attachments/assets/69d5a610-e3ed-45a4-9994-a4836da8cafa" />
<img width="707" height="459" alt="image" src="https://github.com/user-attachments/assets/6822e884-6dec-404e-b407-a7ea3e18513d" />


------
# date:08/8
# time spent:1.25hr
## description:
I had started assigning footprints for each i had checked the each part and its assigned footprints in the lscs number in the mouser website and first i added all the footprints and then i had found many errors while updating ,i fixed the each one by changing it into newer parts and then at last i had fixed all the problems,and i had tried to fix the warnings,bu found out that they were common,so i left them.
# images:
<img width="1608" height="883" alt="image" src="https://github.com/user-attachments/assets/d10a7887-bd50-4bb4-afb1-f93378d20a95" />
<img width="1609" height="883" alt="image" src="https://github.com/user-attachments/assets/faa0d901-46bf-4250-8bf4-3556cb76d669" />
<img width="757" height="680" alt="image" src="https://github.com/user-attachments/assets/1be76884-0a79-4dcd-bb48-e10ac5ded397" />
<img width="599" height="549" alt="image" src="https://github.com/user-attachments/assets/c23849f6-ca0a-4e4d-a37b-9db4944a1c45" />
<img width="782" height="709" alt="image" src="https://github.com/user-attachments/assets/a0c2ec36-7dbf-4859-9d9e-02d98314c4af" />

------
# date:09/8
# time spent:1hr
## description:
I had started the arrangment off the pieces in the devicces it was very difficult because there were many small resistors which was very difficult to make them in a enclosure but the bigger pieces were easy to move as they were less and then i had done the edge cuts for the device
# images:
<img width="599" height="549" alt="image" src="https://github.com/user-attachments/assets/c724d21a-09d6-4b3a-b411-2c19341bd21b" />
<img width="1289" height="817" alt="image" src="https://github.com/user-attachments/assets/02a77973-f3bf-4537-a25a-61d3d2e05c0a" />
<img width="617" height="694" alt="image" src="https://github.com/user-attachments/assets/93d51065-64c5-477f-8d5b-5c9d62c2a2a0" />
<img width="685" height="778" alt="image" src="https://github.com/user-attachments/assets/df9386b0-def9-4cb1-ae84-c335cd8bfc91" />

------
# date:09/8
# time spent:2.5hr
## description:
I had started the routing work which was very difficult to complete,i had completed the routing of the pcb and i have completed only 70% the rest was bit difficult so i will complete it later.
# images:
<img width="1243" height="811" alt="image" src="https://github.com/user-attachments/assets/c932f2e2-6352-4421-a7e7-b71b57425f9f" />

------
# date:09/8
# time spent:0.75hr
## description:
The hardest part of connecting wires has been completed and this part was bit difficult as it contains all about the junnctions and the via points between each layers ,now i should run the erc and see if there wwere any errors
# images:
<img width="815" height="817" alt="image" src="https://github.com/user-attachments/assets/d47a1dca-3487-4e8e-941a-7fcc4ad385db" />
<img width="1151" height="798" alt="image" src="https://github.com/user-attachments/assets/6b643819-cc97-478f-9380-9bd057536e7e" />

------
# date:09/8
# time spent:0.75hr
## description:
I had ran the design rule checker and i had found ou that there were 17 errors in which many wires were overlapping so i had rerouted the wiring and fixed all the errors ans some errors were regarding mounting holes which were too fixed and i had ignored the warnings,and the pcb was good in the 3d view
# images:
<img width="809" height="786" alt="image" src="https://github.com/user-attachments/assets/cff1c3e3-1f81-4731-acb3-566d9a380362" />
<img width="818" height="756" alt="image" src="https://github.com/user-attachments/assets/ec1dd006-686b-4b34-9ec9-22b6e8c297e2" />
<img width="820" height="790" alt="image" src="https://github.com/user-attachments/assets/98cd5b17-8f14-4436-a00c-5527e2068956" />
<img width="1577" height="863" alt="image" src="https://github.com/user-attachments/assets/26fde046-16b1-4114-8b19-3f4c26b5c8b6" />

------
# date:09/8
# time spent:0.5hr
## description:
I had completed the readme and also i had exported the gerber files and also exported the cad files in the repo and then i had zipped the simulator and released it in the github repo.

------
# date:16/8
# time spent:1.25hr
## description:
I had changed the pcb layout and firstly ichanged the differential pairs for data wiring in the schematic and the pcb and then i had changed the disctance from the keep out zone so that there would be no signal issue and then i had figured out how to add the ground planes on both sides and added them and then madde alll the resistors to the same model.
# images:
<img width="847" height="619" alt="image" src="https://github.com/user-attachments/assets/2fd94734-29f6-4c5d-bd68-4989c7278054" />
<img width="631" height="567" alt="image" src="https://github.com/user-attachments/assets/b1e892c4-c987-4b18-9c51-84ec342e2373" />

------
# date:16/8
# time spent:0.5hr
## description:
I had rechecked the drc so that there would be no issue and i had fixed all the errors in the drc which were arround 30 and many of them were regarding traces issue and i fixed them all.
# images:
<img width="811" height="750" alt="image" src="https://github.com/user-attachments/assets/71a9280c-deef-4329-8f14-31ace224ddaf" />
<img width="809" height="788" alt="image" src="https://github.com/user-attachments/assets/b28b448f-5ad0-415d-814b-6de58c432f1f" />

------
# Total hrs:18.00hrs
## Tech: kicad
