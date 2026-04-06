# D-shaped motor shaft fit tolerance

**Created:** 4/5/2026 20:14:20  
**Updated:** 4/5/2026 20:14:35  
**Exported:** 4/5/2026 21:38:19  
**Link:** [https://claude.ai/chat/e8098f23-4d4b-4862-a528-8f29b72c51ce](https://claude.ai/chat/e8098f23-4d4b-4862-a528-8f29b72c51ce)  

## Prompt:
4/5/2026, 8:14:20 PM

I'm trying to build a 3D model piece that can accept a D-shaped motor shaft.    I'm doing the work in Tinkercad.   I used a caliper to measure the diameter of the shaft at the round part as well as the diameter at the flat part.   I constructed in Tinker CAD a cylinder that had a hole in it with the exact dimensions that I measured with the caliper.  The hole is not large enough and I can't force the motorshaft into the hole That was made with precise measurements.  How much of an affordance should I give beyond the size of the measurements that I created with the caliper?   The diameter of the the circle of the motor shaft is four millimeters, And at the flat part of the D shape it's 3.5 millimeters



## Response:
4/5/2026, 8:14:35 PM



````plaintext
Thought process: Identified FDM tolerance issue and prescribed clearance adjustments.

The user is asking about tolerance/clearance to add when 3D printing a hole for a D-shaped motor shaft.

For FDM 3D printing, holes typically print smaller than designed due to plastic expansion and layer adhesion. A common rule of thumb is to add 0.2-0.4mm clearance.

For a 4mm shaft, I'd recommend:
- Add 0.2-0.3mm to the diameter (so 4.2-4.3mm for the circular part)
- The flat part: similarly add 0.2-0.3mm

This is a standard FDM tolerance question.
````

This is a very common 3D printing gotcha! The issue is that FDM (filament) printers tend to print holes *smaller* than designed, due to a few factors:

- Plastic expansion as it cools
- Layer lines slightly intruding inward
- The circular approximation in sliced geometry

**General Rule of Thumb**

For a tight but functional fit (like a motor shaft), add **0.2–0.3 mm to the diameter** of the hole. For a loose/slip fit, go up to **0.4–0.5 mm**.

**For Your Specific Shaft**

Since you want a snug but insertable fit:

| Measurement | Caliper Reading | Recommended Hole Size |
|---|---|---|
| Round diameter | 4.0 mm | **4.2–4.3 mm** |
| D-flat depth | 3.5 mm | **3.7–3.8 mm** |

Start with **+0.2 mm** and test print just the hole section (a small block, not the whole part). If it's still too tight, reprint at +0.3 mm. This saves a lot of time vs. reprinting the full piece each iteration.

**A Few Extra Tips**

- **Print orientation matters** — if the hole is printed horizontally (shaft goes in parallel to the bed), it tends to be slightly more oval. Vertical orientation usually gives rounder, more accurate holes.
- **Drill it out** — for round portions, a 4mm drill bit run through by hand after printing is a quick and precise fix without reprinting.
- **Sand the flat** — the D-flat is harder to drill, but a small flat needle file can remove just enough material.
- **Test with a calibration print** — if you do a lot of shaft/hub work, it's worth printing a small "shaft fit tester" block with holes at 4.0, 4.1, 4.2, 4.3 mm to dial in your specific printer's offset once and for all.





---
Powered by [Claude Exporter](https://www.ai-chat-exporter.net)