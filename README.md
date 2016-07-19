# Automated TruSeq Total RNA Library Preparation Installation Guide #
**For Agilent NGS Workstation Option B**

## Contents ##
1. [Description](#description)
2. [Requirements](#requirements)
3. [Installation](#installation)
4. [Protocol](#protocol)
5. [License](#license)

## Description ##
This document describes how to set up NGI Stockholms TruSeq Stranded Total RNA method for the Agilent NGS Workstation. This protocol is used to prepare up to 96 samples with Illumina’s TruSeq Stranded Total RNA kit.

## Requirements ##
- Agilent NGS Workstation :warning: <i><b>Option B only</i></b>
- Consumables
   - Eppendorf twin.tec 96 PCR plate (Eppendorf, cat# 0030 128.672 (int); 951020460 (US))
   - Nunc deepwell 1.3 mL plate (Thermo Scientific, cat# 260251)
   - ABgene 2.2 mL storage plate Mk.II (Thermo Scientific, cat# AB-0933)
- Labware definitions*
- Liquid classes definition*

\* provided in `all_labware_liquids.vzp`

#### Included files ####
```
all_labware_liquids.vzp
stranded_RNA_1.3.5.pro
```

## Installation ##
### Download files ###

##### Using Git #####
Clone into `https://github.com/ngi-automation/truseq-total-rna.git` from the `Protocol Files` directory:

```bash
cd "C:\VWorks Workspace\Protocol Files"
git clone https://github.com/ngi-automation/truseq-total-rna.git
```

Alternatively, download the compressed folder from:
[`https://github.com/ngi-automation/truseq-total-rna/archive/master.zip`][zip]
and extract to `C:\VWorks Workspace\Protocol Files`. Rename the resulting `truseq-total-rna-master` folder to `truseq-total-rna`. The path to the folder containing the extracted files should then be `C:\VWorks Workspace\Protocol Files\truseq-total-rna`.

### Configure ###
#### Labware and and liquid class definitions ####
Use the import feature in VWorks from `File › Import`in the toolbar and select the `all-labware-liquids.vzp` file included. See the [VWorks Knowledge Base][import] for more information.

#### Device files ####
Device files and profiles are system specific and will not be provided. The "standard" Bravo configuration is used in the TruSeq RNA protocols:

##### Standard configuration #####
Position | Type | Part#
-------: | ---- | -----
1&ndash;3, 8  | Deck Platepad | `G5498b#004`
4, 6     | Peltier Thermal Station (Inheco) | `G5498b#021`
5        | Orbital Shaking Station | `G5498b#033`
7        | Magnetic Bead Accessory | `G5498b#008`
9        | Thermal Station (ThermoCube) | `G5498b#036`/`7`/`8`

:warning:  Each `.pro` file **must have the correct device file set**.

See the [VWorks Knowledge Base][device-file] for more information on how to select the device file.

## Protocol ##

:warning: **Work in progress**

[Link to PDF with instructions][sop].

## License ##
> Licensed under the Apache License, Version 2.0 (the "License");
> you may not use this file except in compliance with the License.
> You may obtain a copy of the License at
>
> http://www.apache.org/licenses/LICENSE-2.0
>
> Unless required by applicable law or agreed to in writing, software
> distributed under the License is distributed on an "AS IS" BASIS,
> WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
> See the License for the specific language governing permissions and limitations under the License.

The full license can also be found in the file LICENSE and must included when redistributing the software.

If this method is used to generate results for publication we ask that you include a reference to this repository, something like:
```
Automation protocols made available by NGI Sweden at https://github.com/ngi-automation/truseq-total-rna
```
*VWorks Automation Control*, *Bravo* and other things relating to the *Agilent NGS Workstation* are trademarks owned by Agilent Technologies, Inc. (Santa Clara, CA 95052-8058, US).

*TruSeq* and *TruSeq Stranded Total RNA* are trademarks owned by Illumina, Inc. (San Diego, CA 92122 US).

[email]: mailto:joel.gruselius@scilifelab.se "E-mail author"
[ngi]: https://portal.scilifelab.se/genomics/ "NGI Stockholm"
[scilife]: http://www.scilifelab.se/platforms/ngi/ "SciLifeLab"
[zip]: https://github.com/ngi-automation/truseq-total-rna/archive/master.zip
[import]: http://www.velocity11.com/techdocs/AutomationSolutionsKB/vworks4_ug/11_Troubleshooting.15.03.html#2005458
[catalog]: http://www.chem.agilent.com/Library/catalogs/Public/5991-0369EN.pdf
[sop]: https://goo.gl/Gt90AB
[device-file]: http://www.velocity11.com/techdocs/AutomationSolutionsKB/vworks4_ug/02_CreateProtocolBasic.04.08.html#1981042

---

>[National Genomics Infrastructure][ngi] at [SciLifeLab][scilife]  
<joel.gruselius@scilifelab.se>  
December 2015
