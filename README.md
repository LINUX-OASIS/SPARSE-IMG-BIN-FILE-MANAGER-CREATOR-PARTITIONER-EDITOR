# 💾 SPARSE IMG/BIN FILE MANAGER, CREATOR, PARTITIONER & EDITOR 💾

![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg?style=for-the-badge)
![Language](https://img.shields.io/badge/language-Bash-brightgreen.svg?style=for-the-badge)
![Maintained](https://img.shields.io/badge/Maintained%3F-yes-green.svg?style=for-the-badge)
![GitHub issues](https://img.shields.io/github/issues/LINUX-OASIS/SPARSE-IMG-BIN-FILE-MANAGER-CREATOR-PARTITIONER-EDITOR?style=for-the-badge&color=yellow)
![GitHub pull requests](https://img.shields.io/github/issues-pr/LINUX-OASIS/SPARSE-IMG-BIN-FILE-MANAGER-CREATOR-PARTITIONER-EDITOR?style=for-the-badge&color=lightgrey)
![GitHub stars](https://img.shields.io/github/stars/LINUX-OASIS/SPARSE-IMG-BIN-FILE-MANAGER-CREATOR-PARTITIONER-EDITOR?style=for-the-badge&color=orange)
![Forks](https://img.shields.io/github/forks/LINUX-OASIS/SPARSE-IMG-BIN-FILE-MANAGER-CREATOR-PARTITIONER-EDITOR?style=for-the-badge&color=informational)

<p align="center">
  <img src="https://forthebadge.com/images/badges/built-with-love.svg" />
</p>

A powerful, all-in-one Bash script that provides a friendly `whiptail` menu-driven interface for managing `.img` and `.bin` disk images. Whether you're creating a giant sparse file for a VM, formatting it, editing partitions, or mounting/unmounting, this tool has you covered.

It's designed to be intuitive, robust, and a little bit fun. 🥳

---

## ✨ Features

This script wraps powerful disk utilities into a simple, interactive TUI:

*   🥞 **Create Sparse Images:** Interactively create sparse `.img` files of any size (MB, GB, TB).
*   🍱 **Format Images:** Format entire images with a single partition using various filesystems (EXT4, BTRFS, FAT32, exFAT, NTFS).
*   🫙 **Sparsify Files:** Convert existing, non-sparse files into sparse files to save precious disk space.
*   🥭 **Mount/Unmount:** Easily mount and unmount image files, automatically handling loop device setup (`losetup -fP`) and teardown.
*   🍣 **Partition Editor:** Launch the powerful `cgdisk` TUI to create, modify, and manage partitions within your image files.
*   ✨ **Format Partitions:** After partitioning, selectively format your newly created partitions with your chosen filesystem.
*   🤖 **Auto-Dependency Check:** Automatically checks for required packages and offers to install them for you.
*   🎨 **Colorful & Interactive:** Uses `whiptail` and `tput` for a pleasant and user-friendly terminal experience.

## 🖥️ Preview

A glimpse of the main menu you'll be working with:

```
  ┌───────────────────────────────────────────────────────────────��[...]
  │ ◉ SPARSE FILE ◉ MANAGER ◉ CREATOR ◉ EDITOR ◉                            │
  ├───────────────────────────────────────────────────────────────��[...]
  │ Select Option                                                             │
  │ ┌──────────────────────────────────────────────────────────────�[...]
  │ │1 [CREATE]🥞  🥞 CREATE custom SPARSE FILE                             │ │
  │ │2 [MAKE]🫙    🫙 MAKE AN EXISTING FILE SPARSE                           │ │
  │ │3 [FORMAT]🍱  🍱 FORMAT AN IMAGE FILE WITH A FILESYSTEM (.IMG/.BIN)    │ │
  │ │4 [MOUNT $PWD]🥭   🥭 MOUNT (.IMG/.BIN) FILE CORRECTLY in $PWD          │ │
  │ │5 [MOUNT]🥭   🥭 MOUNT (.IMG/.BIN) FILE CORRECTLY BY INPUTING ABSOLUTE P │ │
  │ │6 [PARTITIONS $PWD]🍣 🍣 CREATE / MODIFY / FORMAT PARTITIONS OF .IMG/. │ │
  │ │7 [PARTITIONS]🍣 🍣 (absolute PATH) CREATE / MODIFY / FORMAT PARTITION │ │
  │ │8 [UNMOUNT]🦞 🦞 UNMOUNT (.IMG/.BIN) FILE CORRECTLY                     │ │
  │ └──────────────────────────────────────────────────────────────�[...]
  ├───────────────────────────────────────────────────────────────��[...]
  │                      <Ok>                      <Cancel>                     │
  └───────────────────────────────────────────────────────────────��[...]
```

## 🐧 Compatibility

This script is designed for Debian-based Linux distributions that use the `apt` package manager. It has been tested and is known to be compatible with:
*   Debian
*   Ubuntu (and flavors like Kubuntu, Xubuntu, etc.)
*   Linux Mint
*   ...and other Debian/Ubuntu derivatives.

## ⚙️ Dependencies

The script requires several command-line tools to function. It will automatically check if they are installed and, if not, will attempt to install them using `sudo apt install`.

**Required Dependencies:**
*   `whiptail` (for the user interface)
*   `parted` (for partitioning)
*   `dosfstools` (for FAT32 support)
*   `mtools`
*   `exfatprogs` (for exFAT support)
*   `ntfs-3g` (provides `mkfs.ntfs` for NTFS support)

## 🚀 Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/LINUX-OASIS/SPARSE-IMG-BIN-FILE-MANAGER-CREATOR-PARTITIONER-EDITOR.git
    cd SPARSE-IMG-BIN-FILE-MANAGER-CREATOR-PARTITIONER-EDITOR
    ```

2.  **Make the script executable:**
    ```bash
    chmod +x custom-SPARSE-IMG-BIN-FILE-MANAGER-CREATOR-PARTITIONER-EDITOR.sh
    ```

3.  **Run the script:**
    ```bash
    ./custom-SPARSE-IMG-BIN-FILE-MANAGER-CREATOR-PARTITIONER-EDITOR.sh
    ```

> **⚠️ Important:** The script requires root privileges for many operations (`losetup`, `mount`, `parted`, etc.) and will use `sudo`. You will be prompted for your password. Use with caution, especially when working with disk images and partitions.

---

## 💬 Contributing

Pull requests, issues, and suggestions are warmly welcomed!  
See [`CONTRIBUTING.md`](https://github.com/LINUX-OASIS/SPARSE-IMG-BIN-FILE-MANAGER-CREATOR-PARTITIONER-EDITOR/blob/main/CONTRIBUTING.md) for guidelines.

## 🌐 Links

*   [Issues](https://github.com/LINUX-OASIS/SPARSE-IMG-BIN-FILE-MANAGER-CREATOR-PARTITIONER-EDITOR/issues)
*   [Pull Requests](https://github.com/LINUX-OASIS/SPARSE-IMG-BIN-FILE-MANAGER-CREATOR-PARTITIONER-EDITOR/pulls)
*   [Releases](https://github.com/LINUX-OASIS/SPARSE-IMG-BIN-FILE-MANAGER-CREATOR-PARTITIONER-EDITOR/releases)
*   [Wiki](https://github.com/LINUX-OASIS/SPARSE-IMG-BIN-FILE-MANAGER-CREATOR-PARTITIONER-EDITOR/wiki)

## 🧙‍♂️ Maintainer

*   **LINUX-OASIS**

## 📜 License

This project is licensed under the GNU General Public License v3.0. See the LICENSE file for details.

```
Copyright (C) 2024 LINUX-OASIS

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
 the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```
