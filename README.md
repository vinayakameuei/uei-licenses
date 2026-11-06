# UEI package licenses

License files for UEI packages built by the `meta-uei-arm` Yocto layer.
Each folder holds the `COPYING` summary and `LICENSES/` texts to commit to
the root of the matching SVN module.

| Folder | SVN module | Yocto recipe | Packages | Recipe `LICENSE` |
|---|---|---|---|---|
| [DAQ_IOMC](DAQ_IOMC/COPYING) | `DAQ_IOMC` | `kernel-module-daqiomc` | `kernel-module-pdnadev-*`, `kernel-module-pdnabus-*` | `GPL-2.0-or-later & GPL-3.0-with-GCC-exception & Proprietary` (`pdnabus`: `GPL-2.0-or-later`) |
| [DAQLib](DAQLib/COPYING) | `DAQLib` | `daqlib` | `libpowerdna*` | `Proprietary` |
| [UEIiDDS](UEIiDDS/COPYING) | `UEIPAC/UEIiDDS` | `uei-idds-instr` | `uei-idds-instr` | `Proprietary & PD` |
| [libueisimtarget](libueisimtarget/COPYING) | `UEIPAC/UEISim/libueisimtarget` | `libueisimtarget` | `libueisimtarget*` | `Proprietary` |
| [UEIModbus](UEIModbus/COPYING) | `UEIPAC/UEIModbus` | `ueimodbus` | `ueimodbus` | `Proprietary` |
| [libpdnaconfig](libpdnaconfig/COPYING) | `UEIPAC/tools/libPDNAConfig` | `libpdnaconfig` | `libpdnaconfig*` | `Proprietary & PD` |
| [libshareddata](libshareddata/COPYING) | `UEIPAC/tools/libshareddata` | `libshareddata` | `libshareddata*` | `Proprietary & PD` |
| [libueidaq](libueidaq/COPYING) | `Framework` | `libueidaq` | `libueidaq*` | `Proprietary & PD` |
| [ueipallib](ueipallib/COPYING) | `Common/UeiPalLib` | `ueipallib` | `ueipallib-dev`, `ueipallib-staticdev` | `Proprietary & LGPL-3.0-or-later & PD` |
| [dmapserver](dmapserver/COPYING) | `UEIPAC/tools/dmapserver` | `dmapserver` | `dmapserver*` | `Proprietary` |
| [pdnaserver](pdnaserver/COPYING) | `UEIPAC/tools/pdnaserver` | `pdnaserver` | `pdnaserver` | `Proprietary` |
| [paramenv](paramenv/COPYING) | `Yocto/Utilities/paramenv` | `paramenv` | `paramenv` | `GPL-2.0-or-later & Proprietary` |
| [listlayers](listlayers/COPYING) | `UEIPAC/tools/listlayers` | `listlayers` | `listlayers` | `Proprietary` |
| [ueitests](ueitests/COPYING) | `UEIPAC/tests` | `ueitests` | `ueitests` | `Proprietary` |
| [ueidatalogger](ueidatalogger/COPYING) | `UEIPAC/tools/datalogger` | `ueidatalogger` | `ueidatalogger` | `Proprietary` |
| [ueiopcserver](ueiopcserver/COPYING) | `UEIPAC/UeiOpcUa/UeiOpcServer` | `ueiopcserver` | `ueiopcserver` | `Proprietary` (UEI + Unified Automation SDK) |
| [ueiopcuasdk](ueiopcuasdk/COPYING) | `UEIPAC/UeiOpcUa/opcua_sdk` | `ueiopcuasdk` | `ueiopcuasdk*` | `Proprietary & MIT` |
| [ueivistas](ueivistas/COPYING) | `UEIPAC/UEIVistas` | `ueivistas` | `ueivistas` | `Proprietary` |
| [ueidaqpython](ueidaqpython/COPYING) | `Framework/Python` | `ueidaqpython` | `ueidaqpython` | `Proprietary & BSD-3-Clause` (NumPy `numpy.i`) |
| [ueiwebconfig](ueiwebconfig/COPYING) | `UEIPAC/tools/webconfig` | `ueiwebconfig` | `ueiwebconfig` | `Proprietary & PD` |
| [ueiroot-wwwfs](ueiroot-wwwfs/COPYING) | `UEIPAC/file_system` | `ueiroot-wwwfs` | `ueiroot-wwwfs` | `Proprietary & MIT` |
| [ueiroot-tsnconfig](ueiroot-tsnconfig/COPYING) | `PDNA_MX6SX/kirkstone/ueiroot-tsnconfig` | `ueiroot-tsnconfig` | `ueiroot-tsnconfig` | `Proprietary & GPL-2.0-only` |
| [ueiroot-tsndemo](ueiroot-tsndemo/COPYING) | `PDNA_MX6SX/kirkstone/ueiroot-tsndemo` | `ueiroot-tsndemo` | `ueiroot-tsndemo` | `Proprietary & BSD-3-Clause & GPL-2.0-only` |
| [ueiroot-rootfs](ueiroot-rootfs/COPYING) | `PDNA_MX6SX/kirkstone/ueiroot-rootfs` | `ueiroot-rootfs` | `ueiroot-rootfs` | `Proprietary & GPL-2.0-only` |
| [ueiuser-rootfs](ueiuser-rootfs/COPYING) | `PDNA_MX6SX/kirkstone/ueiuser-rootfs` | `ueiuser-rootfs` | `ueiuser-rootfs` | `Proprietary & BSD-3-Clause` |
| [ueimds-rootfs](ueimds-rootfs/COPYING) | `UEIPAC/UEIiDDS/MDS` | `ueimds-rootfs` | `ueimds-rootfs*` | `Proprietary & BSD-2-Clause-Views` (MDS + CoreDX + Jim Tcl) |
| [ueiexamples](ueiexamples/COPYING) | `UEIPAC/examples` | `ueiexamples` | `ueiexamples*` | `Proprietary & BSD-3-Clause` |
| [ueicppexamples](ueicppexamples/COPYING) | `Framework/CPP/examples` | `ueicppexamples` | `ueicppexamples` | `Proprietary` |

Folder names are the SVN module name for the first five packages and the
recipe name for the rest. `COPYING` belongs in the recipe's `S` directory.

## Open compliance items

1. `kernel-module-daqiomc`, `paramenv`: GPL code linked with UEI PowerDNA-licensed / all-rights-reserved code.
2. `ueipallib`: LGPL-3.0 sxmlc linked statically into `libUeiPal.a` (shipped in the image).
3. `ueiopcuasdk`: Unified Automation SLA 2.5 forbids distributing the SDK headers; keep `-dev`/`-staticdev` out of images and SDKs.
4. `ueimds-rootfs`, `uei-idds-instr`: redistribution terms for MDS iDDS and CoreDX DDS binaries.
5. Third-party terms to confirm: Altera Jam STAPL, nmeap `COPYING`, NXP TSN demo scripts, Jim Tcl components.
6. Almost no UEI source file has a copyright/SPDX header.

Search for `[REVIEW NOTE - remove before commit]` in the folders for details.

## Layout

```
<SVN module>/
├── COPYING        short summary: which files are under which license
└── LICENSES/      full text of every license used, named by SPDX id
```

- Each source file states its license with an `SPDX-License-Identifier:`
  line. If `COPYING` and a file header disagree, the file header applies.
- Standard licenses (GPL, GCC exception) are verbatim copies of the texts in
  `poky/meta/files/common-licenses`.
- UEI and third-party licenses without an SPDX id use `LicenseRef-*` names.
- Lines marked `[REVIEW NOTE - remove before commit]` are open decisions.

## Yocto recipe usage

Once `COPYING` is committed to the SVN module root, point the recipe at it
(paths are relative to `S`):

```bitbake
LIC_FILES_CHKSUM = " \
    file://COPYING;md5=<md5sum COPYING> \
    file://LICENSES/LicenseRef-UEI-PowerDNA.txt;md5=<md5sum> \
"
```

Keep the recipe `LICENSE` and the licenses listed in `COPYING` in sync.
For `uei-idds-instr`, `S` is `UEIiDDS/uei-idds-instr`, so use
`file://../COPYING` and `file://../LICENSES/...`.
