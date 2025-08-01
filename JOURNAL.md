---
title: Clackintosh
author: unowen
description: a wireless mechanical keebto go with my mac
created_at: "2025-07-20"
completed_on: "2025-07-31"
tota time: "25.5hr"
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

# July 29-30th: PCB Finalized + made Case
- added decoupling caps to neopixels after a lot of help from people
- did the final wiring of the pcb
- added 3d models to the pcb of the components

- made CAD base + plate for the keeb case
- updated layout json (it did not have a gap i wanted in between func. row and the num row (refer inspiration img))

(the case still has some issues i hope they fixed by tomorrow!)
<img width="2022" height="1216" alt="error" src="https://github.com/user-attachments/assets/0a315463-1580-49a4-aa2f-881c3ffb241c" />


**Total time spent: 5hr (took way too long becuase i had to manually add each key + erros in CAD)**
---

# July 31st: Keeb Finalize
- added 3d model of pcb to CAD
- finishing touches to case CAD
- re-verifying everything => found out battery needed some re-modelling of the case
- finalized repo for shipping

<img width="1822" height="1158" alt="pcb_root" src="https://github.com/user-attachments/assets/ee4f2783-12d9-45ad-b18d-57ef27e31721" />
<img width="1835" height="301" alt="pcb_neopixels" src="https://github.com/user-attachments/assets/48723bb7-be73-42fa-8a01-9f2f16187c45" />
<img width="1839" height="1154" alt="pcb_switches" src="https://github.com/user-attachments/assets/cbbd329b-a10e-4f0e-8d12-38757a6dc319" />
<img width="1936" height="1041" alt="pcb" src="https://github.com/user-attachments/assets/ca63f38d-e5f6-42ad-b48a-dbb9a26fd5cd" />
<img width="1433" height="785" alt="pcb_3d_front" src="https://github.com/user-attachments/assets/b0b1f606-db5c-4cd4-9cf6-6067cc1a33ab" />

**Total time spent: 2.5hr**
---

# Aug 1st: Resolving Issues
needed to update the case and the pcb as told by reviewer

Made the following changes:
- added a wristrest to the keeb case
- created and added a logo to the case + PCB
- added wave patterns on the case and wrist rest to match the blue gradient keycap theme
- added a final look inspiration
- let go of the sticker grafitti wall idea, will put a few aesthetic matching ones only now
- got the decoupling capacitors closer to the neopixels
- added labels to all capacitors for values
- updated value for pullup resistors on i2c expander

<all updated images in the readme>

**Total Time Spend: 2.5hr**
---

**TOTAL TIME SPENT = 23hr (schem took wayy too long)**
