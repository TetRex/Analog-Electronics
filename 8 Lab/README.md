
## Challenge 8: You Shall Not Pass!
**Goal:** Build a band-pass filter that passes only 800–1600 Hz.

**Solution:** Chain a high-pass and low-pass filter in series:
- **High-pass** (blocks below ~800 Hz): `1µF cap + 200Ω resistor` → cutoff ≈ 796 Hz
- **Low-pass** (blocks above ~1600 Hz): `100nF cap + 1KΩ resistor` → cutoff ≈ 1591 Hz

Signals between 800–1600 Hz pass both filters unattenuated.

---

## Challenge 9: I Can't Hear You!
**Goal:** Build a 9V transistor amplifier to boost the microphone's tiny signal.

**Solution:** Design a common-emitter amplifier (`Vcc=9V, Ic=1mA, β=100`), wire the mic output through a coupling cap to the base, and add a 100µF bypass cap across Re. The amplifier gain is approximately `Rc/Re = 4×` without the bypass cap, and much higher with it for AC signals.

---

## Challenge 10: Rock and Roll Light Show
**Goal:** Make LEDs flash in response to sound picked up by the microphone.

**Solution:** Feed the amplifier's output into the **base of a second transistor** wired as a switch. Connect `Vcc → 200Ω → 3 LEDs in parallel → collector`, with the emitter grounded. The small amplified audio signal turns the transistor on, driving enough current to light the LEDs. Optionally, add a reverse-biased diode to ground at the base to discharge negative charge and increase sensitivity.