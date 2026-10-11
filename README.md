# Home Automation (ESP8266)

A Wi-Fi home-automation build from 2018 — switch lights and appliances from a phone browser
on the local network, using an ESP8266 driving a relay board.

![demo placeholder](images/demo.png)

## Bill of materials

| Part | Why | Approx. price | Where |
| --- | --- | --- | --- |
| NodeMCU / Wemos D1 mini (ESP8266) | Wi-Fi microcontroller + web server | ₹250–400 | [NodeMCU](https://www.amazon.in/s?k=nodemcu) |
| 4-channel 5V relay module (opto-isolated) | switch mains loads | ₹250 | any electronics shop |
| 5V 2A power supply | powers the board | ₹200 | any shop |
| Enclosure + terminal blocks | safe mounting | ₹300 | any shop |

> ⚠️ **Mains voltage is dangerous.** Anything that switches 230V should be built inside a
> proper enclosure, wired by someone comfortable with mains, and ideally kept on a fused,
> RCD-protected circuit. Prototype with low-voltage loads (LED strips) first.

## Wiring (overview)

- ESP8266 GPIO pins → relay module IN1–IN4 (through the opto-isolated inputs)
- Relay COM/NO → the appliance's live line (inside the enclosure)
- Common 5V/GND between the ESP and the relay board

![wiring placeholder](images/wiring.png)

## How it works

The ESP8266 joins your home Wi-Fi and hosts a small web page. Buttons on the page send
requests that toggle the GPIO pins, which flip the relays. Everything stays on the local
network — no cloud account required.

## Repo layout

```
firmware/     # the ESP8266 sketch (.ino)
web/          # the control page served by the ESP
docs/         # schematic and enclosure notes
```

> Firmware and schematic are being tidied up and will be committed here.

Built by **Shivam Verma (cyb3r_n3rd)** —
[portfolio](https://cyb3r-n3rd.github.io/portfolio/) ·
[LinkedIn](https://www.linkedin.com/in/shivamvermacyber)


## Links

- Project entry: [LinkedIn projects](https://www.linkedin.com/in/shivamvermacyber/details/projects/)
- Portfolio: [cyb3r-n3rd.github.io/portfolio](https://cyb3r-n3rd.github.io/portfolio/)
