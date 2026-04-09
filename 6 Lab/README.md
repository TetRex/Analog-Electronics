
## Challenge 1: Bright Bright Lights
**Goal:** 4 LEDs at full brightness — removing one doesn't affect the others.

**Solution:** Wire each LED in its own parallel path: `Vcc → 200Ω → LED → ground`. Each gets full voltage independently.

---

## Challenge 2: Meter Mystery
**Goal:** Produce exactly 9mA using only 200Ω resistors and a 9V battery.

**Solution:** `V = IR → R = 9V / 0.009A = 1000Ω`. Wire **five 200Ω resistors in series**. Confirm with ammeter.

---

## Challenge 3: Turn the Lights Off
**Goal:** LEDs are on by default and turn off when their button is pressed.

**Solution:** Wire each LED always-on, then connect a button in parallel with the LED going straight to ground. Pressing the button short-circuits the LED — current bypasses it and the LED goes off.

---

## Challenge 4: Color the Rainbow
**Goal:** Control a tri-color LED with buttons, an LDR, and a potentiometer to mix colors.

**Solution:**
- 🔴 Red: `Vcc → 200Ω → button → R terminal`
- 🟢 Green: `Vcc → 200Ω → LDR → button → G terminal`
- 🔵 Blue: `Vcc → pot → 200Ω → button → B terminal` (pot terminal 3 to ground)
- Common GND leg to ground.

Press button combos and adjust the pot/LDR to mix colors.