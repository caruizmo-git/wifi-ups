# Licensing Scheme

This project uses multiple licenses depending on the type of content. This
multi-license approach is common in open hardware projects because different
types of artifacts (source code, hardware designs, documentation) are best
served by different licenses.

## Quick Reference

| Path | License | Type of content |
|------|---------|-----------------|
| `firmware/` | MIT License | Embedded source code (ESP-IDF, C/C++) |
| `pcb-a/` | CERN-OHL-P v2 | Hardware design files (KiCad, DC-DC PCB) |
| `pcb-b/` | CERN-OHL-P v2 | Hardware design files (KiCad, Power Mgmt PCB) |
| `pcb-c/` | CERN-OHL-P v2 | Hardware design files (KiCad, Control PCB) |
| `shared-libs/` | CERN-OHL-P v2 | Shared symbol/footprint libraries |
| `mechanical/` | CERN-OHL-P v2 | Enclosure designs, mechanical drawings |
| `docs/` | CC BY 4.0 | Documentation, design specs, user guides |
| `datasheets/` | Manufacturers' copyright | Reference material only (not relicensed) |
| Other top-level files | MIT License | Default for miscellaneous files |

Full text of each license is provided in the `LICENSES/` directory.

## Rationale

### MIT License for firmware (`firmware/`)

The MIT License is the de facto standard in the embedded systems and
ESP-IDF/Arduino ecosystem. It is maximally permissive, compatible with
virtually all other open source licenses, and well understood by students
and hobbyists. This choice maximizes the educational reuse of the firmware:
anyone can adapt the code for their own projects, including commercial
ones, with only the requirement of preserving the copyright notice.

### CERN-OHL-P v2 for hardware (`pcb-*/`, `shared-libs/`, `mechanical/`)

The CERN Open Hardware License (CERN-OHL) is specifically designed for
hardware designs and is the most widely recognized hardware-specific
license in the open hardware community.

CERN-OHL v2 comes in three variants:

- **CERN-OHL-P** (Permissive): equivalent in spirit to MIT for hardware
- **CERN-OHL-W** (Weakly reciprocal): modifications to hardware must be
  shared, but not the software running on it
- **CERN-OHL-S** (Strongly reciprocal): equivalent in spirit to GPL for
  hardware; all modifications must be shared

We chose the Permissive variant because the educational goals of this
project align better with maximum freedom of use. Students and makers can
take this design, modify it, and even productize it without restriction
beyond attribution.

### CC BY 4.0 for documentation (`docs/`)

Creative Commons Attribution 4.0 International is the standard license for
open documentation, especially academic and educational material. It
allows anyone to share and adapt the documentation for any purpose,
including commercial use, as long as proper attribution is given.

This license fits the academic context well: this project is used as
teaching material in the VLSI specialization program at Universidad Latina
de Costa Rica, and CC BY 4.0 facilitates reuse by other educators while
preserving authorship credit.

### Manufacturer copyright for datasheets (`datasheets/`)

The PDF datasheets included for reference in the `datasheets/` directory
are copyright of their respective manufacturers (Texas Instruments,
Analog Devices, Vishay, Espressif, Coilcraft, LiTime, and others). They
are included in this repository **for reference convenience only** and
are NOT covered by any of the licenses above. Their reuse is subject to
the original manufacturers' terms, which generally permit redistribution
for non-commercial educational purposes but restrict modification.

If you redistribute this project (for example, forking it for your own
work), consider replacing the contents of `datasheets/` with a README
that links to the manufacturers' download pages instead of bundling the
PDFs directly.

## How to Comply with Each License

### MIT (firmware)

Include the copyright notice and the MIT license text in any distribution
of the code or derivative works. That is the only requirement.

### CERN-OHL-P v2 (hardware)

When you distribute the hardware designs or products manufactured from
them:

1. Include the copyright notice and the CERN-OHL-P license text
2. Include a notice indicating that the design is based on this project
3. If you have modified the designs, document the modifications (date and
   identity of the modifier) in the source files
4. Make the modified source available to recipients of the product

### CC BY 4.0 (documentation)

When you use, share, or adapt the documentation:

1. Give appropriate credit to the original author (Carlos)
2. Provide a link to the CC BY 4.0 license
3. Indicate if changes were made (a brief note suffices)

You may use the documentation for any purpose, including commercially.

### Datasheets

The convenience copies in `datasheets/` are not relicensed. If you need
to redistribute datasheet content, download fresh copies directly from
the manufacturers and follow their terms.

## SPDX Identifiers

For automated license detection tools and source file headers, the
following SPDX identifiers correspond to the licenses used:

- MIT License: `SPDX-License-Identifier: MIT`
- CERN-OHL-P v2: `SPDX-License-Identifier: CERN-OHL-P-2.0`
- CC BY 4.0: `SPDX-License-Identifier: CC-BY-4.0`

For source files in `firmware/`, consider adding the SPDX identifier as a
comment at the top of each file:

```c
// SPDX-License-Identifier: MIT
// Copyright (c) 2026 Carlos Ruiz
```

## Contact

For questions about licensing or to request a different licensing
arrangement for specific use cases, contact: caruizmo.oxygen@gmail.com

---

*This licensing scheme follows best practices established by major open
hardware projects (Arduino, Adafruit, SparkFun) and the SPDX License List
maintained by the Linux Foundation.*
