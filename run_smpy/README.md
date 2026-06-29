### Running Target Separator and Creating Convergence Maps

This directory contains a config file. The only fields you need to change are the **target name** and **redshift** (look up the redshift from the target list here: [SuperBIT target coordinates](https://github.com/superbit-collaboration/superbit-lensing/blob/main/data/SuperBIT_target_galactic_coords.csv)).

---

#### Step-by-step guide

**1. Set up the alias**

Do a fresh `git pull` of this repo and the `superbit-lensing` repo. Then navigate to `superbit-lensing/utility_scripts` and run:

```bash
python add_smpy_alias.py
source ~/.bashrc
```

This adds a shell alias required for the steps below.

---

**2. Set up a target directory**

Go to `/projects/mccleary_group/ysp2026/kappa_maps`. Several targets are already there — start with those. For existing targets, just copy the config file from this directory into the target's folder and update the `target name` and `redshift` fields.

> For new targets: create a new subdirectory using the name from the target list linked above, then copy and edit the config file the same way.

---

**3. Run the convergence map pipeline**

From inside the target directory (where you placed and edited `config.yaml`), run:

```bash
python run_smpy.py config.yaml
```

This generates **dark matter (convergence) maps** from galaxy shape measurements. Recall from the Source Extractor tutorial: after extracting sources, we measure galaxy shapes — and those shapes are used here to reconstruct the dark matter distribution.

---

**4. Tune parameters for high-SNR maps**

Your goal for each target is to produce a high signal-to-noise convergence map by tuning the following parameters in `config.yaml`:

**Quality cuts:**
```yaml
qual_cuts:
  min_Tpsf: 0.5
  max_sn: 1000
  min_sn: 5.0
  min_T: 0.0
  max_T: 100
```

**KS mapping:**
```yaml
resolution: 0.47        # arcmin
gaussian_kernel: 1.5
```

**Aperture mass:**
```yaml
aperture_mass_Rs: 22.50
```

After each run, two subdirectories — `ks/` and `aperture_mass/` — will be created inside the target directory, containing SNR maps named `snr_<...>.png`. Examine these images: X-ray contours should be overlaid automatically. The dark matter distribution won't always coincide exactly with the X-ray emission, but it should be in the same region.

---

#### Cluster targets

See the full target list: [YSP2026 Cluster Targets](https://github.com/s-Sayan/ysp2026/tree/main#-cluster-targets)