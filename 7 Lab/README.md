

## Challenge 5: The Night Light Company
**Goal:** Build a night light that turns on in the dark and off in the light.

**Solution:** Make a voltage divider with a `100KΩ` resistor (top) and the LDR (bottom). In the dark the LDR resistance is high → high output voltage → base turns on the transistor → LED lights. In light the LDR resistance drops → low output voltage → transistor off → LED off.

---

## Challenge 6: The Cascade Fade
**Goal:** Wire 4 RC circuits with 1KΩ resistors so LEDs fade out at 0.235s, 0.735s, 1.6s, and 2.35s.

**Solution:** Use `T = 5RC` to find each capacitance (`C = T / 5R`):
- LED 1: 47µF (single cap)
- LED 2: 147µF (47µF + 100µF in parallel)
- LED 3: 320µF (100µF + 220µF in parallel)
- LED 4: 470µF (single cap)

Press all 4 buttons together, release, and watch them cascade off.

---

## Challenge 7: Don't Make Me Wait
**Goal:** Keep an LED on for ~75 seconds using an RC delayed transistor switch.

**Solution:** Add a 47µF and 100µF capacitor in parallel → `Ct = 147µF`. With the existing 100KΩ resistor: `RC = 100,000 × 0.000147 = 14.7s` → `5 × RC ≈ 73.5s`.