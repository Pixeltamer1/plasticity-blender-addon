# 🎯 Plasticity → Blender Bridge
> Real-time live link between [Plasticity](https://plasticity.xyz) and Blender — updated for **Blender 4.2 – 5.2**

![Blender](https://img.shields.io/badge/Blender-4.2%20–%205.2-orange?logo=blender&logoColor=white)
![Plasticity](https://img.shields.io/badge/Plasticity-Compatible-blue)
![License](https://img.shields.io/badge/License-GPL%20v2-green)

---

![Demo](assets/Plasticity.gif)

---

## ✨ Features

- 🔴 **Live Link** — Any change in Plasticity reflects instantly in Blender
- 🔄 **Manual Refresh** — Pull the latest mesh on demand
- 📐 **Refacet Control** — Choose between Tri / Ngon with custom Tolerance & Angle
- 🎨 **Face Utilities** — Auto Mark Edges, Merge UV Seams, Paint Faces by ID
- ✅ **Blender 5.2 Ready** — Uses the new `blender_manifest.toml` extension system

---

## 📦 Installation

### Requirements
- Blender **4.2 – 5.2** (tested on 5.0, 5.1, 5.2)
- Plasticity (any recent version with Server support)

### Steps
1. Download the latest `.zip` from [Releases](../../releases)
2. In Blender: `Edit → Preferences → Get Extensions`
3. Click the dropdown arrow (top right) → **Install from Disk...**
4. Select the downloaded `.zip`
5. Enable the addon ✅

---

## 🚀 Usage

### 1. Enable the server in Plasticity
`P (Preferences) → Server → Enable`

### 2. Connect from Blender
- Press `N` in the 3D Viewport to open the Sidebar
- Go to the **Plasticity** tab
- Enter `localhost:8980` and press **Connect**

### 3. Work

| Action | Button |
|--------|--------|
| Pull latest mesh | **Refresh** |
| Auto-sync changes | **Live Link** |
| Re-tessellate mesh | **Refacet** |
| Mark sharp edges | **Auto Mark Edges** *(Edit Mode)* |
| Merge UV seams | **Merge UV Seams** *(Edit Mode)* |

> 💡 Materials and Modifiers assigned in Blender are preserved after every Refresh.

---

## 🔧 What changed from the original

The original addon used the legacy `bl_info` system which is no longer supported in Blender 4.2+.

This fork adds:
- `blender_manifest.toml` — required by Blender's new Extension system
- Removed `bl_info` from `__init__.py` to prevent conflicts
- Tested and confirmed working on Blender 5.0, 5.1, and 5.2

---

## 📄 License

GPL v2 — based on the original work by [Nick Kallen](https://github.com/nkallen/plasticity-blender-addon)
