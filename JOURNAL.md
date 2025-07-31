---
title: Clackintosh
author: unowen
description: a nice mechanical keyboard to go with my mac
created_at: "2025-07-20"
completed_on: "2025-07-31"
tota time: "22hr"
---

---
# July 20th: Research
I researched about building mechanical keyboard, made the inital list of features that I am planning to include, explored websites related to mechanical keyboards (ranging from online stores, to various subreddits and youtube videos). Also, looked at some already approved mech keyboards projects submitted for highhway for more info + inspiration.

**(Initial) List of Features:**
- wireless connectivity (and therefore bluetooth + battery) [decided upon nice!nano v2 and li-ion 1100maH battery for now]
- layout = TKL/75% (depending upon if i wish to include a i2c expander or not in pcb) => 87/88 keys OR 81/84/85 keys
- dropping the rotary encoder for now
- sound = thoc (some kind of linear/tactile switches --> prob mx red/brown/black, might look at gateron for cheaper options) (will put some packing foam underneath as mod, not planning to include proper foam for mech keeb yet)
- keycaps --> white-to-blue gradient side printed keycaps (the printed label should be translucent so that rgb light can shine through)
- 3D printed case --> might inclide a nice tilt for better ergo --> white coloured
- per-key rgb via sk2852mini-e leds

**Total time spent: 1.5hr**
---

# July 21st - July 22nd: Schematic for PCB
Made the schematic for the keyboard's pcb. this took a lot of googling, asking in #highway in hackclub's slack, and also some perplexity-done research (because why not) (cross-checked everyhting though).
Made the following updates to the overall project plans as well:
- decided to go ahead with the 75% layout - 81 keys
- added the rotary encoder (since i had to use an i2c expander anyway becuase of the neopixels)

Found a design (mostly just the layout) inspiration:
![keeb inspo](https://imgaz.staticbg.com/thumb/large/oaupload/banggood/images/B2/08/0aa98611-ab68-45b0-be14-be7ab895574e.jpg.webp)

Screnshot of the Schem:
<img width="1337" height="944" alt="Screenshot 2025-07-23 at 12 39 24 AM" src="https://github.com/user-attachments/assets/0c4aae12-2dd9-4654-8c72-4430f62ecf63" />
<img width="1526" height="1073" alt="Screenshot 2025-07-25 at 11 38 41 PM" src="https://github.com/user-attachments/assets/f10d29f3-f775-4625-84d1-cc458908e8e2" />


**Total time spent: 6.5hr**
---

# July 24th: PCB Schem Touchups
Edited the schem to better account for battery life, etc. Made the following updates:
- found a 10000mah battery for powering the setup (added symbol to kicad schem, yes i did not have it before)
- added capacitor + resisitor to neopixels chain (still not sure which specifications ones => decided between (220-470uF range for caps)? and 330-470ohm range for resistor)
- found out that since i only need a underglow, 20 neopixels would be enough instead of all 82 for per-key rgb
- asked in some places (#highway slack and reddit] for cross-verifying my schematic (always good to make sure) [link to reddit post]

Screenshots of the Schem: (better organized in sub-sheets)
  <img width="1342" height="908" alt="root_schem" src="https://github.com/user-attachments/assets/de77d7d8-8f36-415a-8d86-499ddb7fbe5a" />
<img width="644" height="820" alt="swithces_schem" src="https://github.com/user-attachments/assets/5e756d20-3f3d-4d41-8d17-d233b1032a77" />
<img width="1025" height="332" alt="neopixels_schem" src="https://github.com/user-attachments/assets/baddb14a-f328-4ca9-a2a6-c0d5395af28b" />


**Total time spent: 3.5hr**
---

# July 27th - July 28th: PCB Schem Touchups 2 + PCB Placement
**Made some major edits to the schem:**
- changed the key matrix to better resemble the actual keyboard
- added a slide switch (because, well, I forgot to do it before)
- added footprints

**PCB Placement**
- used Keyboard Layout Placer Plugin in KiCad to position the keys in the appropriate place as per decided layout
- made the decided layout in the Keyboard Layout Maker to get the json file
- placed the MCU, battery holder, etc.
- added 3D model for the switch, which i was adding on the worng side, fixed the issue there (took a lot of time)
- wiring is still left

did more research + parts sourcing work informally (i.e checked where all available and at which price range)

Screenshots of the Schem:
 <img width="2240" height="1260" alt="switches_schem_new" src="https://github.com/user-attachments/assets/bf702b60-c10e-443f-b2a5-ba10a3e3b507" />

Screenshots of the PCB (unwired):
<img width="1502" height="841" alt="pcb" src="https://github.com/user-attachments/assets/e99dca17-a1d1-4f6c-a1fc-7a509b2a060b" />

Screenshot of the Keyboard Layout:
<img width="2020" height="1214" alt="Keeb_Layout" src="https://github.com/user-attachments/assets/6caf62cc-36e2-4975-9cd0-2b8ac7889214" />

plan for next ses: add 3d models to pcb + final checks for correctness, start with case CAD

**Total time spent: 4hr**
---

# July 29-30th: PCB Finalized
- added decoupling caps to neopixels after a lot of help from people
- did the final wiring of the pcb
- added 3d models to the pcb of the components
- made CAD base + plate for the keeb case
- updated layout json (it did not have a gap i wanted in between func. row and the num row (refer inspiration img))

<images>

**Total time spent: 4hr (took way too long becuase i had to manually add each key)**
---


# July 31st: Keeb Finalize
- added 3d model of pcb to CAD
- finishing touches to case CAD
- re-verifying everything => found out battery needed some re-modelling of the case
- finalized repo for shipping


<final images in readme>
  
**Total time spent: 2.5hr**
---


**TOTAL TIME SPENT = 22hr (schem took wayy too long)**
