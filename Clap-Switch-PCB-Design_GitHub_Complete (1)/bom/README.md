# Bill of Materials (BOM)

- `EasyEDA_BOM_2026-10-22.xlsx`: **unmodified exported BOM** from the saved EasyEDA project.
- `components-from-CAD-BOM.csv`: condensed version for browsing on GitHub, built from the 16 populated BOM lines, with designator and quantity retained and a note on known substitutions. The export also contains a trailing non-component row, omitted from this readable CSV.

The BOM includes manufacturer and supplier codes linked to the **CAD-library selection**; exact purchase identities for every mounted component have not been independently confirmed.

**Documented as-built differences:** R2 was populated with 4.7 kΩ (matching schematic/BOM but not an older cached PCB property of 4.64 kΩ). D1 is listed as 1N4004 in the schematic/BOM; the physical board uses 1N4007. See the [revision notes](../docs/design-revision-notes.md).
