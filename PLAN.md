# 3D Browser Minecraft Clone - Full Game Plan

## Project Overview
- **Type:** Browser-based 3D voxel game (Minecraft-style)
- **Tech:** Three.js for 3D, vanilla JS, single HTML file
- **Target:** Fun, playable, feature-complete mini game

---

## 🎮 Core Features

### World Generation
- **Terrain:** Procedural heightmap with hills, valleys, trees
- **Size:** 64x64 chunks (render distance optimized)
- **Layers:** Bedrock → Stone → Dirt → Grass
- **Features:** Trees (oak), grass patches, varied elevation

### Block Types (12 blocks)
| ID | Block | Texture Color |
|----|-------|---------------|
| 1 | Grass | Green top, brown sides |
| 2 | Dirt | Brown |
| 3 | Stone | Gray |
| 4 | Cobblestone | Dark gray |
| 5 | Oak Log | Brown bark |
| 6 | Oak Leaves | Dark green |
| 7 | Oak Planks | Light brown |
| 8 | Sand | Yellow |
| 9 | Gravel | Tan speckled |
| 10 | Glass | Transparent light blue |
| 11 | Brick | Red-brown |
| 12 | Bedrock | Dark gray (indestructible) |

### Player Mechanics
- **Movement:** WASD + Sprint (Shift) + Jump (Space)
- **Camera:** Mouse look with pointer lock
- **Physics:** Gravity, collision detection, grounded check
- **Speed:** Walk 5 blocks/sec, Sprint 8 blocks/sec
- **Jump:** 1.2 blocks high

### Block Interaction
- **Left Click:** Break block (instant)
- **Right Click:** Place block on targeted face
- **1-9 Keys:** Select block from hotbar
- **Reach Distance:** 5 blocks

### Inventory & Hotbar
- **Hotbar:** 9 slots, shows selected block
- **E Key:** Open full inventory (visual only)
- **Mouse Wheel:** Scroll through blocks

### UI Elements
- **Crosshair:** Center screen
- **Hotbar:** Bottom center, 9 slots with block icons
- **Instructions:** Initial overlay (dismiss with click)
- **Debug:** F3 for coordinates (optional)

### Visual Features
- **Sky:** Gradient blue to white
- **Lighting:** Ambient + directional (sun)
- **Shadows:** Simple shadows on blocks
- **Fog:** Distance fog for atmosphere
- **Block Outline:** Highlight when looking at block

---

## 🏗️ Technical Implementation

### Three.js Setup
- WebGL renderer with antialiasing
- Perspective camera (FOV 75)
- Raycaster for block detection

### Performance Optimizations
- Instanced mesh for same block types
- Frustum culling (automatic)
- Merge static geometry where possible

### Collision System
- AABB collision with world blocks
- Separate collision for each axis
- Prevent walking through blocks

---

## 📋 File Structure
```
minecraft-clone/
└── index.html    # All code (HTML + CSS + JS)
```

---

## ✅ Acceptance Criteria

1. ✅ Game loads without errors
2. ✅ Player can walk, jump, look around smoothly
3. ✅ Terrain generates with hills and trees
4. ✅ Can break any block (except bedrock)
5. ✅ Can place blocks on any face
6. ✅ Hotbar shows all 12 block types
7. ✅ 1-9 keys select blocks
8. ✅ Collision prevents walking through blocks
9. ✅ Performance: 30+ FPS on modern browser

---

## 🎯 Bonus Features (If Time Permits)
- Day/night cycle
- Sound effects
- More biomes
- Water physics
- Crafting table
- Simple mobs
