 <div align="center">

# 🗺️ FdF — Wireframe Terrain Renderer

* A 3D wireframe terrain renderer written in C, as part of the 42 curriculum.*

[![Language](https://img.shields.io/badge/Language-C-blue.svg)](https://en.cppreference.com/w/c)
[![School](https://img.shields.io/badge/School-42_Paris-black.svg)](https://42.fr)
[![Graphics](https://img.shields.io/badge/Graphics-MiniLibX-orange.svg)](https://harm-smits.github.io/42docs/libs/minilibx)
[![Status](https://img.shields.io/badge/Status-Finished-brightgreen.svg)]()

**Author — [lcournoy](https://github.com/Lazl00)**

</div>

---

## 📖 About

**FdF** (*Fil de Fer*) is a graphics project from the 42 curriculum. The goal is to create a simplified 3D representation of a landscape using a wireframe model.

The program reads a map file containing altitude values and transforms it into a three-dimensional terrain, projected onto a 2D window.

Through this project, we explore fundamental graphics programming concepts:

- **🗺️ Map Parsing** — reading and interpreting terrain data from `.fdf` files.
- **📐 Isometric Projection** — transforming 3D coordinates into 2D screen coordinates.
- **🖼️ Graphics Rendering** — drawing terrain lines using MiniLibX.
- **⌨️ Event Handling** — handling keyboard input and window events.
- **🧠 Memory Management** — allocating, managing and freeing resources safely.

---

## 🚀 Getting Started

### Prerequisites

- A C compiler (`cc` / `gcc` / `clang`)
- `make`
- MiniLibX
- A compatible graphical environment

### Build & Run

```bash
# Clone the repository
git clone https://github.com/Lazl00/FdF.git
cd FdF

# Compile the project
make

# Run FdF with a map
./fdf maps/42.fdf
```

Replace `maps/42.fdf` with the path to any supported `.fdf` map.

---

## 🎮 Controls

| Key | Action |
|:---:|---|
| `W` / `A` / `S` / `D` | Move the terrain |
| `+` / `-` | Zoom in / out |
| `↑` / `↓` | Adjust vertical rotation |
| `←` / `→` | Adjust horizontal rotation |
| `ESC` | Close the window |

*Controls may need to be adjusted to match the actual implementation.*

---

## 🗺️ Map Format

FdF uses `.fdf` files to represent terrain elevations.

Each number corresponds to the altitude of a point on the map. Values are arranged in rows, forming a grid of coordinates.

Example:

```text
0  0  0  0  0
0  1  2  1  0
0  2  5  2  0
0  1  2  1  0
0  0  0  0  0
```

Higher values represent elevated points, while lower values represent flat terrain.

The program connects neighboring points with lines to create a wireframe representation of the landscape.

---

## 📐 Projection

The terrain is represented in three dimensions and projected onto a two-dimensional screen.

An isometric projection creates the characteristic angled view of the landscape, allowing the viewer to perceive depth and elevation without a true 3D rendering engine.

The final result is a wireframe model made of interconnected line segments.

---

## 🛠️ Makefile Commands

| Command | Description |
|---|---|
| `make` | Compile the project |
| `make clean` | Remove object files |
| `make fclean` | Remove object files and the executable |
| `make re` | Recompile the project from scratch |

---

## 🏗️ Project Structure

```text
FdF/
├── includes/
│   └── fdf.h
├── libft/
├── maps/
├── src/
│   ├── parsing/
│   ├── rendering/
│   ├── projection/
│   └── main.c
├── Makefile
└── README.md
```

*The structure above is illustrative; adapt it to match the actual repository.*

---

## 📚 Resources

- [42 FdF Project](https://42.fr/)
- [MiniLibX Documentation](https://harm-smits.github.io/42docs/libs/minilibx)
- [Isometric Projection](https://en.wikipedia.org/wiki/Isometric_projection)
- [42 Intra](https://intra.42.fr/)

---

## 🎓 42 Curriculum

*This project has been created by **lcournoy** as part of the 42 curriculum.*

