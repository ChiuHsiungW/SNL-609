# SNL-609 (DaVinci) - MobileNet V2 FVP Simulation

This repository contains the deployment artifacts for **MobileNet V2 1.0 224 (INT8)**. These files are optimized for the **Arm Ethos-U65 NPU** and are intended for verification using **Arm Fixed Virtual Platforms (FVP)**.

---

## 📂 Artifacts Overview

* **`ethos-u65-img_class.axf`**: The executable image containing debug symbols and section placement.

---

## 🚀 Running on FVP

To launch the simulation, follow these steps to pass the `.axf` file to the FVP:

### Option 1: From the Build Directory
Change directory to the generated cmake build folder which contains the `.axf` file output in the `bin` subdirectory:

!(SNL609_mobilenetv2_FVP_SSE-300.png)

```bash
cd <SNL-609>
<path_to_FVP>/FVP_Corstone_SSE-300/models/Linux64_GCC-9.3/FVP_Corstone_SSE-300_Ethos-U65 -a ./SNL-609/ethos-u65-img_class.axf -C ethosu.num_macs=512


