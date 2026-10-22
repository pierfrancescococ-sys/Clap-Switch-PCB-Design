# Design revision and assembly notes

This repository preserves evidence of different stages of an academic hardware workflow rather than pretending all files were generated simultaneously from one unchanging revision.

## Snapshots and provenance

1. **Fabrication Gerbers:** ZIP recovered from the JLCPCB order for `Gerber_PCB4_2026-05-09_Y2`. These are the files used in the board manufacturing order, dated **2026-05-09** in the archive name.
2. **CAD project:** locally exported EasyEDA Pro `.epro2` file dated **2026-10-22**. It is editable and includes schematic and PCB design resources.
3. **BOM:** locally exported EasyEDA BOM in `.xlsx` format, dated **2026-10-22**. This is the CAD BOM rather than a verified as-purchased receipt.
4. **Physical build:** photographs and a university laboratory report describing manual THT assembly and functional testing.

## Relevant discrepancies

- In the CAD schematic and exported BOM, resistor **R2 is 4.7 kΩ**. A cached PCB property listed **4.64 kΩ** during a later EasyEDA `Import Changes` preview. The assembled board used **4.7 kΩ**, a practical commercial-value substitution explained in the report.
- In the CAD schematic and exported BOM, **D1 is 1N4004**. The assembled circuit used **1N4007** according to the project report and builder. Both are members of the 1N400x rectifier family but their ratings are not identical.
- A later DRC check identified a schematic–PCB **netlist/property synchronization warning**. The inspected preview showed component-name and designator updates (for example Q2→T2 and U1→LED1) and property changes. No automatic synchronization was applied when preparing these GitHub materials. The review does **not** establish that every possible schematic/PCB difference has been resolved.

Consequently, the **Gerbers are the original fabrication reference**, whereas the source project is a later editable snapshot. Formal revision-equivalence, electrical rule verification and a fresh DRC pass remain outside the evidence provided here. Avoid treating the later export as an independently verified manufacturing revision.

## Documentation policy

- No values or datasheets were silently changed in the original export.
- The human-readable CSV reports the CAD BOM and separately calls out known as-built substitutions.
- The documented laboratory testing verified relay switching and LED state after correcting the LED orientation; no mains installation or compliance testing was performed.
