# Olm-PCB

- [Olm-PCB](#olm-pcb)
  - [General Information](#general-information)
    - [Related Projects](#related-projects)
  - [Technologies used](#technologies-used)
  - [Usage](#usage)
  - [DIY](#diy)
    - [Controls](#controls)
  - [Project status](#project-status)
    - [Room for improvement](#room-for-improvement)
  - [Acknowledgements](#acknowledgements)
  - [Contact](#contact)
  - [License](#license)

## General Information

This repo hosts the schematics and CAD files for the PCB of the [_Olm_][olm] project.

The _Olm_ is both an interactive sculpture and a tool for randomly generating ambient soundscapes and music. It is a digital, aleatoric synthesizer housed in a hand-crafted enclosure of plywood, plaster and aluminum.

The designs enable the creation of an instrument or similar projects using the Daisy Seed. Once assembled, it supports up to three potentiometers and two switches via JST connectors. Features include USB-rechargeable battery power, a headphone amplifier, and 1/4 jack audio outputs for stereo and phones, with mono output control and outputs for LED status lights. Mono output control and LED status lights are programmable through the Daisy Seed.

![olm_proc_03](https://github.com/MaxKablaam/olm-pcb/assets/55173884/f019e93d-e367-405a-8945-a753d3e0c1d0)

### Related Projects

- [Olm][olm]
- [Olm-pd][olm-pd]

## Technologies used

- [Electro-Smith][electrosmith] [Daisy Seed][seed]
- [Adafruit PowerBoost 500 Charger][power-boost]

## Usage

The schematic files are designed in KiCad, a free and open-source PCB design tool. To view the schematics, download KiCad. PDF versions are also accessible in the repository.

For integrating the board with a pure-data patch, use the `olm_components.json` file. This file should be used when flashing the patch to the Daisy Seed with [Plugdata][plugdata] or [pd2dsy][pd2dsy].

## DIY

In the `kicad_project/Export` folder, you'll find all necessary files for manufacturing the board. I successfully used these files to produce the board at an affordable cost with [JLCPCB][jlc].

### Controls

- **Potentiometers**: Use a linear 10K potentiometer. Attach its leads to a 3-pin JST PH connector as shown in the schematics.
- **Switches**: Any simple two-lead switch will work, though I used [Kailh Box Jade keyboard switches](https://www.kailh.net/products/kailh-box-thick-clicky-switch-set). Connect the leads to a 2-pin JST PH connector, the connection order doesn't matter.
- **Cabling**: You can create custom cables using heat-shrink tubing, which can be integrated into any unique enclosure you design.

![DPOiuQq8q8](https://github.com/MaxKablaam/olm-pcb/assets/55173884/e32e58db-9439-4e66-b663-5e0186a46b7e)

## Project status

Project is _Complete_!

### Room for improvement

While the PCB aspect of the _Olm_ project is finished, there are always things that can be improved upon in future projects.

- **Headphone Amplifier**: The existing design is outdated and could be enhanced in future versions.
- **Surface-Mount Technology (SMT)**: The use of Through-Hole Technology (THT) was a personal choice due to my unfamiliarity with SMT and not wanting to acquire any more new tools or skills for this complex project. However, retrospectively, SMT might have simplified the process. Future projects will likely adopt SMT.
- **Rechargeable Battery Implementation**: This version employs the [Adafruit Power Boost 500][power-boost] daughter-board for battery charging. For future designs, I plan to integrate a simpler, custom charger directly onto the PCB, which would be more cost-effective and space-efficient.

## Acknowledgements

This project owes its success to the dedication of the Daisy Seed engineers and the invaluable support of their communities. Special acknowledgments go to:

- [Daisy Seed Discord][daisy-discord]
<!-- - Takumi Ogata: That helpful dude on the daisy seed discord, for his help, and tutorials TODO -->

<img src="https://github.com/MaxKablaam/olm-pcb/assets/55173884/7419c108-2e8b-4bfb-a574-1037cf15c295" alt="PCB assembled" width="500">

## Contact

Created by [Eric Max Kaplin][me].

## License

This project is open source and unless otherwise specified in specific files, available under the [GPL-3 License][license].

[olm]: https://ericmaxkaplin.com/content/projects/olm/
[olm-pd]: https://github.com/MaxKablaam/olm-pd
[electrosmith]: https://www.electro-smith.com/
[seed]: https://www.electro-smith.com/daisy/daisy
[power-boost]: https://www.adafruit.com/product/1944
[jlc]: https://jlcpcb.com/
[plugdata]: https://plugdata.org/
[pd2dsy]: https://github.com/electro-smith/pd2dsy
[daisy-discord]: https://discord.gg/ByHBnMtQTR
[license]: https://www.gnu.org/licenses/gpl-3.0.en.html
[me]: https://ericmaxkaplin.com/
