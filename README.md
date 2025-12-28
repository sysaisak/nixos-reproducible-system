# NixOS Configuration

This repository contains my current **NixOS system configuration**, managed as a single `configuration.nix` file.

The goal of this repo is to:

* Keep a **clear and understandable** system configuration
* Document real-world **sysadmin-oriented NixOS usage**
* Avoid unnecessary complexity while learning NixOS deeply

---

## Structure

```
.
├── configuration.nix
└── README.md
```

At the moment, everything lives inside `configuration.nix`. I am intentionally **not modularizing yet**.

---

## System highlights

Some things configured in this system:

* NVIDIA + iGPU **PRIME offloading**
* Steam with `nvidia-offload`

> This configuration is meant to be *practical*, not minimal nor aesthetic-focused.

---

## Usage

This repository is intended for **personal use and learning**.

If you want to test or adapt it:

```bash
sudo cp configuration.nix /etc/nixos/configuration.nix
sudo nixos-rebuild switch
```

**Warning**: Hardware-specific options (GPU, drivers, kernel modules) may not match your system.

---

> Simple configs are easier to debug. Complexity can wait.
