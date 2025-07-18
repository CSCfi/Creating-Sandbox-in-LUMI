# Singularity Sandbox Containers on LUM: CLI Tools & Secure Browser

This project contains two Singularity container environments for use on the LUMI supercomputer. Both are built using Ubuntu 22.04 and targeted at different CLI use cases:

1. **`web_browsing.def`** – A lightweight development CLI environment (with `curl`, `wget`, `lynx`)
2. **`online_shopping.def`** – A secure, private browsing CLI environment using `tor`, `torsocks`, `lynx`, and `w3m`

---

## 📦 Container 1: `web browsing.def` – CLI Tools Sandbox

A simple Ubuntu-based environment for general command-line use.

### Includes:
- `wget`
- `curl`
- `lynx`

### Build:
```bash
module load LUMI/24.03 systools
singularity build --sandbox web_browsing.sif web_browsing.def
```



## 📦 Container 2: onlineshopping.def – Secure CLI Browser Sandbox

A containerized CLI browsing environment designed for private, anonymized web access.

### Includes:
- `tor`
- `torsocks`
- `lynx`
- `w3m`
Timezone: Europe/Helsinki
Locale: en_US.UTF-8

### Build:
```bash
module load LUMI/24.06 systools
singularity build --sandbox onlineshopping.sif online_shopping.def
```
