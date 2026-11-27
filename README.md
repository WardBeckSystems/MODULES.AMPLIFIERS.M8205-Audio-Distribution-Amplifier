# M8205 Audio Distribution Amplifier · Amplifiers

Ward-Beck Systems M8205, 1986|19. Wiki page: [M8205 on WBSps.ca](https://wardbecksystems.github.io/WBSps.ca/PAGES/M8205.html)

| Folder | What is in it | Files |
|---|---|---|
| [SCHEMATICS/](SCHEMATICS/) | electrical drawings: schematics, functional diagrams, component layouts, wiring | 6 |
| [MECHANICAL/](MECHANICAL/) | front panels, cover plates, metalwork, assemblies; the front panel as vectors | 22 |
| [PINOUTS/](PINOUTS/) | the RTO-144 connector: connection sheets, connector layouts, rear views | 3 |
| [MANUALS/](MANUALS/) | manuals, manual pages, price lists, brochures, documents | 6 |
| [PHOTOS/](PHOTOS/) | photographs of the module | 14 |
| [SOFTWARE/](SOFTWARE/) | program listings, firmware, the plugin | 1 |
| [KICAD/](KICAD/) | KiCad schematics traced from the drawings, the symbol, PCB projects | 3 |
| [OCR/](OCR/) | the note of every file: date, origin, title block, OCR text | 26 |

<!-- module data: tools/module_specs.py, tools/forum_quotes.py -->

**On the WBSps forum (2006|39 - 2014|47):** [4 topics](FORUM.md): what owners and technicians said about it.

## Circuit description

From [1995 - M8205 - 8205-02-001 - COMPONENT LAYOUT.wp](MANUALS/1995%20-%20M8205%20-%208205-02-001%20-%20COMPONENT%20LAYOUT.wp) page 1 (read by OCR; check against the pages). As data: [`CircuitDescription.json`](CircuitDescription.json).

<details><summary>Read it</summary>

4 Parts List 4-1 to 4-4

5 Drawings:

Schematic B 8205-02-001 Component Layout B 8205-06-001 (Note: 0 dBu = 0.774V rms)

Gain: (Bridging) +30 dB to -6 dB continuously variable. (Bridging Gain).

Frequency Response: +/-0.1 dB 15 Hz to 25 kHz.

Noise: 120 dB below maximum output at unity gain.

104 dB below the nominal +8 dBm output level at unity gain.

75 dB below the nominal +8 dBm output level at maximum gain. (measured with an average responding meter over a 20 Hz to 20 kHz bandwidth).

Harmonic Distortion: Less than 0.01% 15Hz to 25 kHz, up to +24 dBm output level with 8 isolated outputs simultaneously driven. (Typically less than 0.005%).

Input Level: -22 dBu to +14 dBu nominal, for +8 dBm output. +30 dBm maximum.

Input Impedance: 30,000 ohms or greater, balanced.

Source Impedance: 600 ohms or less, balanced.

Common Mode Rejection: Greater than 80 dB, 20 Hz to 20 kHz.

Common Mode Voltage: +/-25 volts peak.

Output Level: +8 dBm nominal, +24 dBm maximum at each output, up to 8 outputs maximum.

Output Impedance: 600 ohms resistive, each output actively balanced.

Load Impedance: 600 ohms balanced for each isolated output.

Output Isolation: Greater than 85 dB, 15 Hz to 25 kHz. Better than 95 dB mid band.

Output Offset: Less than +/-500 microvolts.

Phasing: The numbered terminal of the input pair and the numbered terminal of the output pair are in phase.

Power Requirements: +/-22 volts DC, 40 mA idling, 190 mA full load output.

Ambient Temperature: 0 to 50 degrees Celsius.

Dimensions: 1.00&quot; wide x 2.75&quot; high x 10.60&quot; deep.

(25.4 mm x 70.0 mm x 270.0 mm).

Weight: 0.5 lbs (227 gms).

**GENERAL**

The M8205 Audio Distribution Amplifier was designed to be a transparent component to an audio distribution system. Its beyond the state of the art technical performance along with ultra reliability will result in years of trouble free service.

The input circuitry is configured to provide an actively balanced bridging load to the audio source. It rejects large common mode voltages that may exist between the source and destination points of signal path.

The front panel continuously variable sensitivity control covers a 36 dB gain range. This gain range accommodates input signal levels from -22 dBm to +14 dBm fora nominal +8 dBm output signal level. The sensitivity adjustment is normally made via a small screwdriver, optionally this control maybe supplied with a small trim setting knob.

The ultra low noise characteristics of the preamplifier circuity result ina signal to noise ration of greater than 104 dB at the unity gain sensitivity setting, decreasing to only 75 dB at a -22 dBm input sensitivity.

The eight actively balanced 600 ohm outputs normally operate at a nominal signal level of +8 dBm. a maximum output capability of +24 dBm is provided with all outputs simultaneously loaded. The output splitter networks are integral to the amplifier card assembly, providing greater than 95 dB of isolation between individual outputs.

The compact size and low standby power requirements of this amplifier permit high density audio distribution systems to be configured. The MF82 mounting frame houses twelve M8205 Audio Distribution Amplifiers, with two redundant M8245 Power supplies in only two rack units of a standard nineteen inch equipment rack.

Input

The input signal to the amplifier is applied at connector pins 1 &amp; A, and the input shield connects to pin B.

R1 and R2 sets the amplifier's input impedance to 30,000 ohms. IC U1 with its associated components makeup the preamplifier circuitry. CR1 through CR4 provide limiting to excessively applied input signal levels.

C4 and R9 are adjusted to provide optimum common mode signal rejection across the audio band.

The front panel sensitivity control R14A/R14B controls the amount of feedback that is applied around preamplifier IC U1B and buffer amplifier U2A. This two stage sensitivity control arrangement results in very high signal to noise characteristics being maintained over wide gain variations.

The audio output signal from buffer amplifier U2A is coupled to the output power amplifier stages through coupling capacitor C10.

Output

The actively balanced output power amplifier is composed of two sections. The upper half comprising of driver U3 and complimentary power transistors Q5 and Q6, and the lower half consisting of U4 and complimentary power transistors Q2 and Q3.

This power output stage is capable of delivering in excess of 4 watts continuously with no detrimental effects. A shorted output will have very little affect on the remaining outputs.

Q1 and Q4 are bias setting transistors which thermally track the amplifier's ambient temperature, thereby maintaining the correct quiescent currents for the complimentary output power transistor.

DC output offset voltages maybe trimmed down to the microvolt region by adjusting R19 and R36. Once set there is little need for making further adjustment, only in the event that either IC U3 or U4 is replaced. Since the two power output stages are DC coupled R19 should be adjusted first and then R36.

Power Supply Decoupling

The ±22 volt DC supply bus voltages appearing at the amplifier connector pins 15 &amp; Sand 13 &amp; Pare isolated from the amplifier circuitry via fusing resistors R52 and R53. The incoming ±22 volt supply voltages are filtered by C18 through C21, after which they connect directly to the amplfier's power output stages.

Q7 and Q8 form the positive and negative supply decouplers for the preamplifier and buffer IC's U1 and U2. These decoupling circuits filter and drop the supply voltages to ±18 volts.

The typical quiescent supply current for the M8205 is 35 mA. At the full rated output of +24 dBm into eight 600 ohm loads the supply current is 190 mA. C1 Capacitor 220 uF/10 V Kemet T390F227M010AS

**C1A &quot; SOT**

C2 &quot; 220 uF/10 V Kemet T390F227M010AS

**C2A &quot; SOT**

C3 &quot; 15 pF Philips 2222-638-10159 C4 &quot; 2-18 pF &quot; 2222-809-05003 C5 &quot; 10 uF/35 V Kemet T390C106M035AS

C6 &quot; 10 pF Philips 2222-638-10109 C7 &quot; 10 uF/35 V Kemet T390C106M035AS C8 &quot; 0.1 uF/100 V Sprague 1C10X7R104M050B C9 &quot; 0.1 uF/100 V &quot; &quot; C10 &quot; 68 uF/10 V Kemet T390D686M010AS

C11 &quot; 56 pF Philips 2222-638-46569 C12 &quot; 22 pF &quot; 2222-638-10229 C13 &quot; 10 uF/35 V Kemet T390C106M035AS C14 &quot; 4.7 uF/10V &quot; T390B475M010AS C15 &quot; 10 pF Philips 2222-638-10109

C16 &quot; 10 uF/35 V Kemet T390C106M035AS C17 &quot; 4.7 uF/10V &quot; T390B475M010AS C18 &quot; 22 uF/35 V &quot; T390E226M035AS C19 &quot; 22 uF/35 V &quot; &quot; C20 &quot; 100 uF/25 V Philips 03116101

C21 &quot; 100 uF/25 V &quot; &quot; C22 &quot; 10 uF/35 V Kemet T390C106M035AS C23 &quot; 10 uF/35 V &quot; &quot; C24 &quot; 22 uF/25 V Siemens 85200 C25 &quot; 22 uF/25 V &quot; &quot;

C26 &quot; 15 pF Philips 2222-638-10159 C27 &quot; 15 pF &quot; &quot; C28 &quot; 33 pF &quot; 2222-638-10339 C29 &quot; 100 pF &quot; 2222-638-58101 C30 &quot; 47 pF &quot; 2222-638-34479

C31 &quot; 47 pF &quot; &quot;

CR1 to Diode Fairchild 1N4148

Q1 Transistor Na­tional 2N4401

**Q8 &quot; &quot; 2N6730**

R1 Resistor 1/4W 1% 16K2 Philips MR25 F

**R8 &quot; &quot; 8K25 &quot; &quot;**

R9 Potentiometer 5K Bourns 3006P 5K R10 Resistor 1/4W 1% 8K25 Philips MR25 F

**R13 &quot; &quot; 3K &quot; &quot;**

R14 Potentiometer 5K Clarostat 10-065 R15 Resistor 1/4W 5% 30K Philips CR25

**R18 &quot; &quot; 10K &quot; &quot;**

R19 Potentiometer 100K Bourns 3006P 100K R20 Resistor 1/4W 5% 22K Philips CR25

**R23 &quot; &quot; 6K8 &quot; &quot;**

R24 Resistor 1/4W 5% 5K6 Philips CR25

**R26 &quot; &quot; 2.2 &quot; &quot;**

R27 to &quot; 1/2W 1% 301 &quot; MR30 F

**R35 &quot; 1/4W 1% 4K75 &quot; MR25 F**

R36 Poten­tiometer 100K Bourns 3006P 100K

R37 Resistor 1/4W 5% 47K Philips CR25

**R43 &quot; &quot; 2.2 &quot; &quot;**

R44 to &quot; 1/2W 1% 301 &quot; MR30 F

**R59 &quot; &quot; 30K &quot; &quot;**

U1 Integrated Circuit National LM833N

</details>

<!-- /module data -->

## Photos

_Photographs of the module itself: front, back, inside, racked._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKOUU2dWlIQWJFaFU/view?resourcekey=0-iyGmVuCdZwSi-JnjIiFQIQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKOUU2dWlIQWJFaFU&resourcekey=0-iyGmVuCdZwSi-JnjIiFQIQ" width="240" alt="1995 - M8205 - 2013-03-14 11_20_34.jpg"></a><br><sub>1995|28 · 2013-03-14 11_20_34</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKZTZob1JwNEZFYjg/view?resourcekey=0-YVNV8jr0qVg9HFpoKVno9A" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKZTZob1JwNEZFYjg&resourcekey=0-YVNV8jr0qVg9HFpoKVno9A" width="240" alt="1995 - M8205 - 2013-03-14 11_20_37.jpg"></a><br><sub>1995|28 · 2013-03-14 11_20_37</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKcWtIcWpubGs1Tnc/view?resourcekey=0-IoW2hKdEfDIjWcyki7IvsA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKcWtIcWpubGs1Tnc&resourcekey=0-IoW2hKdEfDIjWcyki7IvsA" width="240" alt="1995 - M8205 - 2013-03-14 11_20_45.jpg"></a><br><sub>1995|28 · 2013-03-14 11_20_45</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKNkxMSy0wbzR6SDA/view?resourcekey=0-ymBHWUtq7InAvvSYJiTOOw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKNkxMSy0wbzR6SDA&resourcekey=0-ymBHWUtq7InAvvSYJiTOOw" width="240" alt="1995 - M8205 - 2013-03-14 11_20_46.jpg"></a><br><sub>1995|28 · 2013-03-14 11_20_46</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKbTdxcFh5UXlGbU0/view?resourcekey=0-5ZF4Ah40oRiY04IqNOCx6Q" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKbTdxcFh5UXlGbU0&resourcekey=0-5ZF4Ah40oRiY04IqNOCx6Q" width="240" alt="1995 - M8205 - 2013-03-14 11_20_48.jpg"></a><br><sub>1995|28 · 2013-03-14 11_20_48</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKOHNBd2hxYWJfbWc/view?resourcekey=0-AJNIU5cKGcPF8GKtchpsVA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKOHNBd2hxYWJfbWc&resourcekey=0-AJNIU5cKGcPF8GKtchpsVA" width="240" alt="1995 - M8205 - 2013-03-14 11_20_50.jpg"></a><br><sub>1995|28 · 2013-03-14 11_20_50</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKbndhb3BzeEpIb1U/view?resourcekey=0-8_Ea8r5OLsYmZe2NQdTyEw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKbndhb3BzeEpIb1U&resourcekey=0-8_Ea8r5OLsYmZe2NQdTyEw" width="240" alt="1995 - M8205 - 2013-03-14 11_20_55.jpg"></a><br><sub>1995|28 · 2013-03-14 11_20_55</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKSmdwZUpXZWxjbjA/view?resourcekey=0-jm9rp8ociP00GpGZMXmswg" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKSmdwZUpXZWxjbjA&resourcekey=0-jm9rp8ociP00GpGZMXmswg" width="240" alt="1995 - M8205 - 2013-03-14 11_21_04.jpg"></a><br><sub>1995|28 · 2013-03-14 11_21_04</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKMkhnSl9NVno0N0U/view?resourcekey=0-JN_k-saUCYXMIqW8KdNduQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKMkhnSl9NVno0N0U&resourcekey=0-JN_k-saUCYXMIqW8KdNduQ" width="240" alt="1995 - M8205 - 2013-03-14 11_21_09.jpg"></a><br><sub>1995|28 · 2013-03-14 11_21_09</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKcXJ5MWZuaHRkRUk/view?resourcekey=0-zEzXEFmtsCtIrOFbgzmiRA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKcXJ5MWZuaHRkRUk&resourcekey=0-zEzXEFmtsCtIrOFbgzmiRA" width="240" alt="1995 - M8205 - 2013-03-14 11_21_11.jpg"></a><br><sub>1995|28 · 2013-03-14 11_21_11</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKTlZXZzZ1YnFuY28/view?resourcekey=0-jJtw3XPscn5zrETNGzGsFA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKTlZXZzZ1YnFuY28&resourcekey=0-jJtw3XPscn5zrETNGzGsFA" width="240" alt="1995 - M8205 - 2013-03-14 11_21_19.jpg"></a><br><sub>1995|28 · 2013-03-14 11_21_19</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKZmxTQ2dGNXpVWDQ/view?resourcekey=0-y31WqoSAt5qNXu2sxb3D9w" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKZmxTQ2dGNXpVWDQ&resourcekey=0-y31WqoSAt5qNXu2sxb3D9w" width="240" alt="1995 - M8205 - Distribution Amp 003.jpg"></a><br><sub>1995|28 · Distribution Amp 003</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKZkg5d3FHYXBNNlE/view?resourcekey=0-f_f-JGFK-TgkkvoS6M04-g" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKZkg5d3FHYXBNNlE&resourcekey=0-f_f-JGFK-TgkkvoS6M04-g" width="240" alt="1995 - M8205 - file.jpg"></a><br><sub>1995|28 · file</sub></td></tr>
</table>

## Mechanical

_Mechanical drawings: front panels, cover plates, metalwork and hardware (-03- drawings), AutoCAD files, each with its `(EXTRACTED).svg` vectors; `<module> - front panel.svg` is the front panel as vectors._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1hds95EEJkOAdQ4MhwGljZhM7_g1Kpo4n/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1hds95EEJkOAdQ4MhwGljZhM7_g1Kpo4n" width="240" alt="1990 - M8205 - DOC - 900416-04-001 - SELECTOR PANELS LIMITATION ROWS WITH CHARACTERS PER PUSHBUTTON.jpg"></a><br><sub>1990|23 · DOC - 900416-04-001 - SELECTOR PANELS LIMITATION ROWS WITH CHARACTERS PER PUSHBUTTON · <a href="MECHANICAL/1990%20-%20M8205%20-%20DOC%20-%20900416-04-001%20-%20SELECTOR%20PANELS%20LIMITATION%20ROWS%20WITH%20CHARACTERS%20PER%20PUSHBUTTON%20(EXTRACTED).svg">vectors</a></sub></td></tr>
</table>

Not on Google Drive yet: `1986 - 8205-03-003 - HEATSINK USED ON 14-147 & 14-148 PCB (M8205 & M8206 DA) - DRN J - ISS 1.png`, `1987 - 8205-03-005 - INSULATING WAFER (USED ON PCB 14-147 & 14-148) - DRN GEB - ENG GEB MAY - ISS 1.png`, `1989 - 8205-03-004 - HANDLE P.C. BOARD PULLER USED ON D8212 FRAME - DRN J - ISS 2.png`

## Schematics

_Electrical drawings: schematics (-02-), functional diagrams (-01-), component layouts (-06-), wiring (-09-), PCB files (.pcb .dsn), and beside each scan its `(EXTRACTED).svg`: the vectors traced from it._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1AjIWt-mon_AeNAOtO7-FXiJk3PJpzpzm/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1AjIWt-mon_AeNAOtO7-FXiJk3PJpzpzm" width="240" alt="1995 - M8205 - DOC - 950272-01-002 - IERN MULT MULT BROADVEW CASTLE FRANK SHERBOURNE YCNGE.jpg"></a><br><sub>1995|28 · DOC - 950272-01-002 - IERN MULT MULT BROADVEW CASTLE FRANK SHERBOURNE YCNGE · <a href="SCHEMATICS/1995%20-%20M8205%20-%20DOC%20-%20950272-01-002%20-%20IERN%20MULT%20MULT%20BROADVEW%20CASTLE%20FRANK%20SHERBOURNE%20YCNGE%20(EXTRACTED).svg">vectors</a></sub></td></tr>
</table>

## Manuals and documents

_Manuals and manual pages, price lists, RTO-144 connection sheets, brochures, ads and other document scans._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKY0JpNk1qaUxDVWM/view?resourcekey=0-dUgh5IqoN5H2VeBru5sm2g" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKY0JpNk1qaUxDVWM&resourcekey=0-dUgh5IqoN5H2VeBru5sm2g" width="240" alt="1989 - M8205 - DOC - 8200 brochure 1989 a.jpg"></a><br><sub>1989|22 · DOC - 8200 brochure 1989 a</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKRURFWk1kYV92bFU/view?resourcekey=0-yQTr_qUte9I8Sz3N381yGw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKRURFWk1kYV92bFU&resourcekey=0-yQTr_qUte9I8Sz3N381yGw" width="240" alt="1995 - M8205 - Distribution Amp 001.jpg"></a><br><sub>1995|28 · Distribution Amp 001</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKeEN4Sm1YcXN1VDQ/view?resourcekey=0-p1cN19_Zmw6-Y6VJgY-HxA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKeEN4Sm1YcXN1VDQ&resourcekey=0-p1cN19_Zmw6-Y6VJgY-HxA" width="240" alt="1995 - M8205 - Distribution Amp 002.jpg"></a><br><sub>1995|28 · Distribution Amp 002</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKVnFJV0pGY1VadDA/view?resourcekey=0-r-UfnQ6grxNVG60Ml268NQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKVnFJV0pGY1VadDA&resourcekey=0-r-UfnQ6grxNVG60Ml268NQ" width="240" alt="19xx - M8205 - DOC - 8200 brochure a.jpg"></a><br><sub>19xx - M8205 - DOC - 8200 brochure a</sub></td></tr>
</table>

## KiCad

_KiCad: a schematic (`.kicad_sch`) traced from each electrical drawing, the module symbol (`.kicad_sym`) and its PCB projects. Traced schematics are the line work only: redraw with symbols over them._

- [1995 - M8205 - DOC - 950272-01-002 - IERN MULT MULT BROADVEW CASTLE FRANK SHERBOURNE YCNGE.kicad_sch](KICAD/1995%20-%20M8205%20-%20DOC%20-%20950272-01-002%20-%20IERN%20MULT%20MULT%20BROADVEW%20CASTLE%20FRANK%20SHERBOURNE%20YCNGE.kicad_sch)
- [M8205.kicad_sym](KICAD/M8205.kicad_sym)
- [index.html](KICAD/index.html)

## Software

- [index.html](SOFTWARE/index.html)

---
Archive: Anthony Peter Kuzub · [WBSps.ca](https://WBSps.ca) · [WBSps.Kuzub.com](https://WBSps.Kuzub.com)
