# 🔭 Welcome to the Young Scholars Program 2026!

Hey, welcome aboard! You're about to spend your summer doing **real astrophysics research** — not textbook exercises, but actual science using data from a real space telescope. That's pretty awesome, and we're genuinely excited to have you here.

Don't worry if things feel unfamiliar at first. Everyone starts somewhere, and we'll be with you every step of the way.

---

## 🌌 So, What Are We Actually Studying?

This summer, you'll be exploring **galaxy clusters** — the largest structures in the entire universe. To give you a sense of scale: a single galaxy like our Milky Way contains hundreds of billions of stars. Galaxy clusters contain *hundreds of galaxies*, all bound together by gravity, spread across distances of several **megaparsecs**.

> **Quick unit check:** 1 parsec ≈ 3.26 light-years. A light-year is how far light travels in one year — and light moves at 186,000 miles per second. So yes, these things are *enormous*.

But here's the cool part: most of a galaxy cluster is completely invisible. What you can see — the galaxies themselves — is only a tiny fraction of what's actually there. The rest is:

- 🌡️ **Hot gas** floating between the galaxies (called *intracluster medium*), which glows in X-rays — the same kind of X-rays used in hospitals to image bones!
- 🌑 **Dark matter**, which makes up roughly **80% of the total mass** of a cluster. We can't see it in any kind of light. The only way we know it's there is through *gravity* — it bends and distorts the light from galaxies behind the cluster, like a cosmic magnifying glass.

That last effect is called **gravitational lensing**, and it's one of the most elegant ideas in modern physics. By carefully measuring how background galaxies appear slightly stretched and warped, we can actually *map* where all that invisible dark matter is hiding.

This summer, you'll work with **three types of data** from galaxy clusters:
1. **Galaxy light** (optical images from SuperBIT)
2. **X-ray emission** from hot gas
3. **Dark matter maps** reconstructed from gravitational lensing

Your job is to bring all three together and see how they relate to each other. Pretty wild, right?

---

## 🎈🛰️ Meet SuperBIT

The data you'll be working with comes from **SuperBIT** — a balloon-borne imaging telescope that floats to an altitude where it's *above 99% of Earth's atmosphere*. That means it gets incredibly sharp images, almost like being in space, but at a fraction of the cost of a satellite.

SuperBIT has observed many galaxy clusters, most of which are actively **merging** — two massive clusters colliding in slow motion over millions of years. These are some of the most energetic events in the universe, and they give us a unique window into how dark matter, gas, and galaxies all behave under extreme conditions.

Here are a few stunning images from the telescope: https://sites.physics.utoronto.ca/bit

---

## 🛠️ Task Zero: Getting Set Up

Before diving into science, let's get your tools ready. Here's your checklist:

- [ ] **Download and install [Anaconda](https://www.anaconda.com/products/distribution)** — this is a free Python distribution that makes managing packages easy. Install it on your laptop.
- [ ] **Install the `superbit-lensing` repo** — follow the instructions at [github.com/superbit-collaboration/superbit-lensing](https://github.com/superbit-collaboration/superbit-lensing). It's straightforward, and we're here to help if anything trips you up!
- [ ] **Get your Northeastern University email** — you'll need this for the next step.
- [ ] **Get access to Explorer**, Northeastern's High Performance Computing (HPC) cluster — this is where most of the data lives. You can only request access once you have your NU email, so this might take a little time.

> 💡 **While you're waiting on HPC access:** No worries! The data is also available on OneDrive in the **[YSP2026](https://northeastern-my.sharepoint.com/:f:/r/personal/sa_saha_northeastern_edu/Documents/YSP2026?csf=1&web=1&e=qoXlSy)** folder, so you can start working on your laptop right away.

---

## 📋 Your Projects This Summer

### 🎨 Task 1: Make Beautiful Color Images of Galaxy Clusters

**Notebook:** `notebook/rgb.ipynb`  
**Data:** `/projects/mccleary_group/ysp2026/coadd`

Your first task is to create stunning **RGB color images** of galaxy clusters by combining three different filters: **g** (green), **b** (blue), and **u** (ultraviolet). Think of it like making a photo in Photoshop — except your raw material is light from billions of years ago.

The notebook walks you through how to do this and lets you experiment with brightness, contrast, and color stretching. These images will go directly into your **final presentation**, so make them look good!

Later on, you'll also overlay X-ray data and dark matter maps on top — those make for some truly spectacular visuals.

---

### ☢️ Task 2: Map the Hot Gas with X-ray Contours

**Notebook:** https://github.com/LeilaOhashi/leila_superbit_lensing/blob/notebook-only-clean/notebooks/leila_redseq.ipynb  
**Data:** `/projects/mccleary_group/ysp2026/xray`

Next up, you'll work with **X-ray data** from galaxy clusters — this traces the super-heated gas (we're talking tens of millions of degrees!) that fills the space between galaxies.

You'll create **contour maps** — kind of like a topographic map, but for X-ray brightness — and overlay them on your optical images. 

**A special bonus:** This notebook was created by **Leila Ohashi**, a student from *last year's* YSP program who is heading to Stanford this fall! She'll meet with you on **Wednesday, June 24th at 10 am** to walk you through it and share tips on working with astronomical data.

You'll also get to meet **Dr. Giulia Cerini**, a postdoctoral scientist at JPL (NASA's Jet Propulsion Laboratory) who is an expert in X-ray analysis — date TBD!

---

### 🔴 Task 3: Find the Cluster Members

**Notebook:** `notebook/redseq.ipynb`

Here's a fun detective problem: if you look at an image of a galaxy cluster, you're seeing *thousands* of galaxies — but not all of them are actually part of the cluster. Many are just in the foreground or background, coincidentally in the same direction in the sky.

How do you find which ones actually *belong* to the cluster? It turns out galaxies in a cluster tend to share similar colors (they're mostly old, reddish galaxies). By looking at color patterns — a technique called the **red sequence** — you can identify likely cluster members.

You'll save your final catalog of cluster members for use in later analysis, and also create **overlay maps** combining your cluster galaxy map with existing dark matter maps.

---

### 🗺️ Task 4: Make Dark Matter Maps (The Grand Finale!)

This is the most advanced task, and it's genuinely cutting-edge science.

Using a technique called **Kaiser-Squires inversion**, you'll take the subtle distortions in background galaxy shapes and reconstruct a **convergence map** — essentially a 2D map of where all the mass (mostly dark matter) is located in the cluster.

You'll experiment with different parameters and evaluate your results using **signal-to-noise ratio (SNR)** — a measure of how confidently you've detected something above the noise. Higher SNR = cleaner detection.

---

## 🌍 Cluster Targets

You have data for a whole bunch of clusters! Feel free to divide them among yourselves — we recommend tracking progress in a shared Google Sheet (like [this one](https://docs.google.com/spreadsheets/d/1PdYF34n7FV2bDfDlDr8NZSN06H1iTEX3BPRIU2FTYyY/edit?usp=sharing) from last year's students):

| | | | |
|---|---|---|---|
| 1E0657_Bullet | Abell2384a | Abell3571 | AbellS780 |
| Abell141 | Abell2384b | Abell3667 | ACT_CL_J0012_0855_J0012_0857 |
| Abell1689 | Abell3365 | Abell3716S | COSMOS113 |
| Abell2163 | Abell3411 | Abell3827 | COSMOSk |
| Abell2345 | Abell3526 | AbellS0592 | MACSJ0416d1m2403 |
| Abell2384b | Abell3526 | MACSJ0723d3_7327_JWST | MACSJ1105d7m1014 |
| MACSJ1931d8m2635 | MS1008d1m1224 | MS2137m2353 | PLCKG287d0p32d9 |
| RXCJ1314d4m2515 | RXCJ1514d9m1523 | RXCJ2003d5m2323 | SMACSJ2031d8m4036 |
| SPTCLJ0411 | Z20_SPT_CLJ0135m5904 | | |

The data lives at: `/projects/mccleary_group/ysp2026/coadd`

---

## 📅 How the Summer Works

Here's roughly what your days and weeks will look like:

- **Daily check-ins (~9:30 am):** Sayan will stop by to chat for 15–30 minutes — ask questions, share what you've found, or just say hi.
- **Weekly meeting with Prof. McCleary:** You'll give her a brief update on your progress. Don't stress — these are casual and she's wonderful.
- **Tuesday 1:00 pm — Cosmology Group Meeting:** You'll sit in on the weekly meeting with grad students, postdocs, undergrads, and faculty working on all kinds of astrophysics and cosmology. It's a great way to see what the broader research community is up to!
- **End-of-summer presentation:** You'll present your results to the group. Your RGB images, X-ray overlays, and mass maps will all be part of this!

---

## 💬 A Note Before You Begin

You don't need to already know Python. You don't need to already know astronomy. What you *do* need is curiosity and a willingness to try things and ask questions when you're stuck — and trust us, everyone gets stuck. That's just science.

We're genuinely glad you're here. Let's go find some dark matter. 🚀