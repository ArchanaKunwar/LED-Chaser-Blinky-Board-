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

![image.png](https://cdn.hackclub.com/01a0b59e-5cff-713d-8a01-c441a35ce639/image.png)

---

![image.png](https://cdn.hackclub.com/01a0b59e-6028-7a15-a15c-00ebd722fddc/2026-09-18_23-28-39.png)

---

![image.png](https://cdn.hackclub.com/01a0b59e-6371-718a-8593-0a0cb90c3f08/2026-09-18_23-28-43.png)

---
 
![full schematic - it actually looks decent](Images/Schematic.png)

---
 
 
**Time spent:** 3 hours (mostly googling tbh)
 
---
