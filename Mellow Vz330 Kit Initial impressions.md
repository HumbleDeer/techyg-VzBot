# Mellow VZ Bot 330

|   |   |
|---|---|
|![Greg's Maker Corner](https://github.com/HumbleDeer/techyg-VzBot/assets/16231288/9580b7c7-a708-4953-a85a-7081973e37ac) | ![Provok3d](https://github.com/HumbleDeer/techyg-VzBot/assets/16231288/14d270aa-d9e3-4e25-93da-554f2908cd2e) |

Sponsored by Provok3d.com  
July 2023

This document is a writeup of my ini4al impressions immediately following my VzBot 330 Mellow build, which is intended to augment my Ini4al Impressions video posted on Youtube.

Find my Youtube Channel here: http://www.gregsmakercorner.com/

If you are considering buying a VzBot 3d printer and are based in the United States, please consider buying from Provok3d who is one of the few authorized dealers in the US. This company sponsored my build and I am VERY appreciative! 

https://provok3d.com/vzbot*330/?v=0a10a0b3e53b

## Overall Summary

* Building a VzBot is an ambitious but rewarding build. This machine is intended for DIY enthusiasts and tweakers who want to push 3d printing to the limits. While other DIY designs may offer similar benefits, you might spend a bit more time tweaking, upgrading and going down rabbit holes on to get there.
* With the VzBot, you can expect high speeds (10*20K acceleration, 500 mm/sec as a starting point) with a large build volume (330mm) immediately after completing a well*built, squared and fully tightened printer. With a finely tuned machine, you can expect to achieve 50K*100K accelerations and print beyond 1 meter per second. Wow!
* At the present time, this level of speed and performance is not available "off the shelf" though printers like the Bambu P1P are definitely gaining ground.
* For my very first print, I used a 10K acceleration and 300 mm/sec print speed. The printer had no issue keeping up though it jolts around a bit because the table the printer sat on was not very stable. While I have only done initial testing, I believe this printer easily lives up to the promises of high speed.
* The Mellow Fly VzBot does include the necessary components (CPAP fan, RSCS fans, Goliath hot end) to achieve amazing speeds. However, keep in mind that in order to achieve these speeds you will need a very sturdy and stable surface, and may need to bolt the printer down. You will also need to take many steps to tune and calibrate the printer.
* The Mellow Fly VzBot does not rely on printed parts for any crucial parts of the drive train and gantry, but instead uses CNC metal parts which provides an increased level of rigidity that is suited for high speed and high temp printing. It is possible to build a VzBot with printed parts and still get good results, however.
* With that in mind, you will still need 2 rolls (1kg each) of primary color and 1 roll (1kg) of accent color.
* The VzBot 330 Mellow Kit does not include everything you need to complete the printer build, but it does include most components. See the end of this document for additional part recommendations, tools, etc.
* The Vzbot 330 is an open*source design, with the exception of the CNC metal parts which must be obtained from 3rd party vendors.
* The Github for VzBot 3 30 designs here: https://github.com/VzBoT3D/VzBoT-Vz330
* According to the Github documentation, a VzBot 330 can be sourced starting at $800. The Mellow Kit is around $1600 but also includes CNC parts and many other high*end components like LDO Super Power motors and rails.

## Want to see my build log? Join the VzBot discord and check it out here

https://discord.com/channels/829828765512106054/

## My recommendations

* I recommend the VzBot Mellow kit for experienced builders who want to be on the cutting edge of 3d printing and squeeze every ounce of performance out of a printer.
* This printer is also ideal for those who want fast print time without having to buy multiple machines and enjoy tinkering and tweaking.
* If you are new to 3d printing I recommend building a Voron 0 first, which would be an excellent printer to “boot strap” many of the parts for this machine which need to be printed in ASA or ABS and will also test your skills/readiness. If you can successfully build a Voron 0 you should be able to complete this build without too many issues.
* This is a DIY printer and building/tweaking is a hobby in itself. If you are mainly interested in the outcome of printing (3d printed parts) and do not enjoy tweaking, fixing, etc. look elsewhere.

## VZBot Build Process

* The VzBot documentation has been emerging from simple Github pages with pictures, to what I would consider an "MVP" (minimum viable product) philosophy. Think of the manual more as guidelines vs. step by step instructions.
* I went into this build with the idea that I would build it as stock as possible. There were a few places I was tempted to go outside of stock but for the most part I resisted the urge and stuck with the intended design. I felt this would be best to give a good review of the kit and help guide other builders.

## Mellow Fly Kit

* The Mellow kit is a good start and has high quality components where it really matters, especially for the motors and of course CNC parts. You will definitely need to augment your kit with additional components to complete it. There are some obvious components that you will need* for example a Raspberry Pi or equivalent. I also needed several different sizes of fasteners that weren't included. I've listed the vast majority of components I used in the video description if you would like to get a feel. Expect to spend around $xx*$xxx depending on what you may already have on hand.

## Build Time

* It took me less than 3 weeks to build this printer. I was working on it part*time, weekends and evenings, and also recording video along the way. An experienced builder who has previously built Core XY printers (such as Voron, RatRig, or Annex) could possibly complete the build in a long weekend "best case". Realistically, I would budget at least 1*2 weeks to build.

## Mechanical Build

* The mechanical build was very straight forward up until back panel. The build complexity is very similar to build a Voron Trident, or a Prusa Mk3/4.
* Unfortunately, the panels needed additional prep work. Drilling was required to open up holes for power supply (which were too tight), and new holes were required for DIN Rail mounting.
* Drilling aluminum is not particularly difficult with the proper tools, but it may be a barrier for some.

## Electronics, Wiring and Crimping

* The electronics portion of the build is tedious and time consuming, and could be a significant challenge especially for those who do not have experience crimping, soldering, etc.
* **WARNING.** The Mellow Fly kit I received included an under spec’d AC power inlet, and it should be discarded. Some builders have reported the inlet melting when heating both the bed and hot end, which draws a significant amount of power. I purchased a replacement AC inlet on Amazon but it would be best to get one (a standard c14 ac inlet) from a reputable company like Mouser or Digikey ideally with a certification.
* You will be working with mains power, two power supplies (24v and 48v), and an SSR for the AC bed. While this isn't difficult to wire up, you really need to use care while wiring and also make sure you are earthing properly. **Consult with an electrician if you are not sure.**
* You will need to carefully consider layout of^ the wiring. The VzBot design team deliberately does not prescribe a wiring layout, because there are so many possible directions to take, as well as optional/potential upgrades. For example, some builders may opt for multiple SSR's for high temp chamber heating, as well as additional fans.
* My kit did not include very many connectors outside of JST and a few small spade terminals for the Super 8 Pro board. With that in mind you will need to source these depending on the direction you go. You will also need several different crimpers. I ended up crimping Spade Terminals for power supplies, Raspberry Pi, JST PH for fan connectors to the 5160's, Ferrules for the 5160's, and JST XH connectors for many other connections (fans, thermistors, etc.).

## Where I ran into challenges

* On occasion the manual was not as clear as I was hoping, and I had to consult the CAD diagram for clarification. In some cases, I couldn't find what I was looking for, so I went and asked in the Discord. There are several helpful members there and also times where the design team answered my question. I found the community very helpful though I know Discord is not everyone's cup of tea.
* Having to drill the back panel was not expected but it wasn't too difficult. Fortunately, I had the proper drill bits and tools.
* It took me a while to figure out how I wanted to lay out electronics including the DIN mount, wire channels, wagos, etc. I wanted to go with a stock layout as much as possible. I also looked at a few other builds in the Discord showcase and build log to decide what I wanted to do.
* I was stuck for a few hours troubleshooting klipper communication errors with the 5160 motor drivers. Thanks to discord users, including porkcube who helped me sort out a setting I needed for the driver to work. I also noticed the stepper adapters use a connector that does not really seat well, and reseating/firmly connecting these also helped.
* Another frustrating issue was the mellow fly thermistor broke while I was installing it. I later learned that this is common due to the type of cement they use to secure the wiring. I was able to order a replacement thermistor, though not a PT1000, but has been working fine. I recommend getting a few of the Triangle Labs thermistors from AliExpress.
* The machine is very heavy. The further I went in the build, the heavier the machine got. I recommend holding off on installing the heated bed / plate until the end of the build for this reason.
* As I went through my build log I created recommendations for the manual as well as the Mellow Fly kit. You can search my build log for “RECOMMENDATIONS” to see these, and I also plan to provide a consolidated list to both VzBot design team, and Mellow.

## Additional components and tools

### Components

Additional components I used or recommend are below. These are all affiliate links. If you use these links, it helps me out and costs you nothing.

* Polylite ASA (2 rolls of primary color, 1 roll of accent color) * https://amzn.to/44MV8Dz
* SSR DIN Mount * https://amzn.to/3rVonFB
* HEPA filter * https://amzn.to/3rL2PLX
* LED Light * https://amzn.to/45809Gw
* Rubber Feet * https://amzn.to/44NqUjM
* Tobsun 24v to 5v DC*DC converter * https://amzn.to/43NzcXL
* AC Inlet * https://amzn.to/457NROi
* 100K M3 Thermistor * https://amzn.to/44N3yL
* Small .25 inch Braided Cable Sleeve for Back Panel Motor Wiring * https://amzn.to/457et2g
* Medium .5 inch Braided Cable Sleeve for Toolhead Wiring * https://amzn.to/3OcDcez
* M2 Flathead Self Tapping Screws * https://amzn.to/44R9dzV
* M2.5 Button Head Screws * https://amzn.to/4512XG
* Reusable Cable Ties * https://amzn.to/3QhfekU
* Synthetic Lube for Lead Screw: https://amzn.to/3FUyptf
* Blue Permatex for Fasteners: https://amzn.to/3ATPmjE
* Isopropyl Alcohol (Spray Bottle): https://amzn.to/3lRp1Pe
* 16 awg wiring for AC * https://amzn.to/3YkcfdG
* Heat shrink kit * https://amzn.to/3Qc4STw
* Spade Terminals * https://amzn.to/3YkZhw

### Tools

Tools I used or recommend are below. These are all affiliate links. If you use these links, it
helps me out and costs you nothing.

* PA*09 Engineer Crimping tool: https://amzn.to/3aLgZB
* Titan Ratcheting Crimper: https://amzn.to/3aKaONE
* Ferrule Crimping Tool: https://amzn.to/2Z3axDb
* Heat gun: https://amzn.to/3OyD2P
* Drill / Tap combo: https://amzn.to/3QlLSBZ
* Drill bits: https://amzn.to/3Ydc43z
* Drill Bit Cutting Fluid: https://amzn.to/3DwB7oW
* Hakko Soldering Station: https://amzn.to/3FZtsiM
* Hakko Heat Insert Tool: https://amzn.to/3aLh6N
* Small Screwdriver Set: https://amzn.to/3DNNc7h
* Heavy Duty Scissors: https://amzn.to/3DObKNm
* Metric Bondhus Hex Drivers (Ball Driver): https://amzn.to/3vpjti
* Metric Wiha Hex Drivers: https://amzn.to/3vp5Tv
* Metal Ruler: https://amzn.to/3n5YsoQ
