# Refresh ~1min after repo generation!
# Nautilus PCB template repo
**IMPORTANT:** This has been taken and modified from Hermes/rocketry. Changes have been made especially considering part handling.
## Usage:
1. Create a repository using this repo as a template, and name the new repo accordingly for your board
1. A KiCAD project will be automaticaly generated from this template by a github workflow
1. **IMPORTANT: WAIT FOR THE WORKFLOW TO COMPLETE** - You will see a commit by github-actions[bot]

## Naming rules for new repo:
1. Name should follow this structure:  
   **[project-name]-[pcb-name]-PCB**
1. everywhere dashes (`-`) are used where spaces would be
1. **project-name:** name of the project, lowercase (ex.: `nautilus`)
1. **pcb-name:** name of the pcb
    - lowercase
    - preferably short-ish, but *not* abbreviation, dash (-) instead of spaces (i.e. `flight-computer`, or `power`, but **not** ~~`fc`~~, and **not** ~~`pwr`~~)
    - must **not** include `board` (i.e. `power`, but **not** ~~`power-board`~~)
1. Ends with `PCB`, uppercase
1. The name of the project will be the same as the name of the repo

### Correct repo name examples:
- `bernoulli-power-PCB`
- `nicollier-flight-computer-PCB`
- `nicollier-backplane-PCB`
- `hermes-recovery-PCB`

## Repo structure:
**Suppose the name of the repo is `bernoulli-beer-PCB`, the repo structure would be the following:**
```
├── Datasheets/
├── bernoulli-beer-blockdiagram.drawio
├── bernoulli-beer-blockdiagram.pdf
├── PCB/
│   ├── ARIS_frame.kicad_wks
│   ├── can.kicad_sch
│   ├── bernoulli-beer-PCB.kicad_pcb
│   ├── bernoulli-beer-PCB.kicad_prl
│   ├── bernoulli-beer-PCB.kicad_pro
│   ├── bernoulli-beer-PCB.kicad_sch
│   ├── mcu.kicad_sch
│   ├── Outputs/
│   ├── Parts/
│   │   ├── kicad-extra-repo/
│   │   └── kicad-standard-repo/
│   ├── power.kicad_sch
│   ├── stack_format.kicad_sch
│   └── usb.kicad_sch
├── README.md
```

### Datasheets/
Put some useful datasheets here that are helpful for understanding the PCB design
### -blockdiagram.drawio
Put the blockdiagram of the PCB here, and **keep it up-to-date!**
### -blockdiagram.pdf
The blockdiagram exported to pdf, also, very-very important, **keep it up-to-date!!!**
### PCB/
The KiCAD project lives here, some important contents:
#### PCB/Outputs/
A github workflow will automatically export the schematics as PDF, the BOM in CSV, iBOM in HTML, and the PCB as STEP here.
#### PCB/arts/
This directory contains all the extra symbol and footprint libraries that you might add, as well as the kicad-standard-repo and the kicad-extra-repo. The latter two are maintained by ARIS, and are included here as git submodules, you must not modify them!
### README.md
This file contains the description of the PCB. Best README file in every project cycle gets a beer (or sth else) from Georg but maybe even Zoltán but you will have to bother him yourself. Give a good, but brief overview, you can also include images here (for that you should make an `Images/` directory and put them there), etc. Usually this can be quite similar to the confluence documentation you write.

## Explanation 
