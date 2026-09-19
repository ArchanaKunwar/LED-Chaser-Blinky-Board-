# Blinky Board (555 LED Chaser) Journal
 
---
 
## Entry 1 — Finally started, schematic done!!
 
ok so i finally opened KiCad after putting it off for like 3 days. ngl i was kinda intimidated but the guide made it pretty straightforward.
 
the plan is simple: 555 timer in astable mode = it just keeps oscillating forever, clocking the CD4017 counter. the 4017 then lights up 10 LEDs one at a time in sequence. pretty sick concept honestly.
 
### Stuff i placed
 
- **NE555P** — the timer
- **CD4017** — decade counter
- **1k resistor** — for the 555 timing
- **Potentiometer (RV)** — to control speed (this is the fun part, you can make it go zoom or snail pace)
- **100nF cap** — normal ceramic one
- **10uF electrolytic cap** — POLARIZED so direction matters!! almost messed this up
- **470Ω resistor** — shared by all LEDs
- **10 LEDs**

### Problems i hit
 
- pin names were confusing af at first. like why is it `CLKEN` and not just `CLK_EN`? took me a sec to figure out clock inhibit means "stop the clock" so we ground it
- wires were EVERYWHERE and it looked like spaghetti. switched to using labels instead and it looks way cleaner now
- the 555 astable config had me googling for like 20 mins. the capacitor goes between pin 2 and 6?? and then to ground?? eventually got it tho
### Screenshots

---

![image.png](https://cdn.hackclub.com/01a0b59e-6028-7a15-a15c-00ebd722fddc/2026-09-18_23-28-39.png)

---

![image.png](https://cdn.hackclub.com/01a0b59e-6371-718a-8593-0a0cb90c3f08/2026-09-18_23-28-43.png)

---
 
![full schematic - it actually looks decent](Images/Schematic.png)

---
 
 
**Time spent:** 3 hours (mostly googling tbh)
 
---


## Entry 2 — Footprints (this was kinda annoying)
 
assigned footprints to everything today. honestly this part was lowkey tedious but whatever.
 
### CD4017 footprint situation
 
so the guide said the CD4017 footprint isn't in KiCad by default which is actually so annoying?? like why wouldn't they include it. had to download from Ultra Librarian and import it. the import process was kinda confusing but i followed the guide step by step.  
 
![footprint](https://cdn.hackclub.com/01a0b78d-cc72-7cdc-b238-e25c1ad22c69/image.png)
 
checked pin spacing against the datasheet and everything seemed to line up. the 4017 is 2.54mm pitch which is standard for DIP so we good.
 
ran **Update PCB from Schematic** and everything showed up in the PCB editor in a big pile in the corner lol. 
 
### What went wrong
 
- spent like 30 mins confused about why my CD4017 symbol didn't have a footprint assigned. turns out i had to manually add it because it's not in the default library. dumb.

### Screenshots
 
![assigning](https://cdn.hackclub.com/01a0b78d-cf67-729b-9836-b4fcec51f780/2026-09-19_08-29-49.png)

![assigning](https://cdn.hackclub.com/01a0b78d-d257-7aa9-8c11-2cb43d7fe1ec/2026-09-19_08-29-51.png)
 
**Time spent:** 1.5 hours
 
---
