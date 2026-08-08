<img width="241" height="25" alt="image" src="https://github.com/user-attachments/assets/6c86c383-9491-4772-a24c-a137074de44c" /># date:07/8
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
