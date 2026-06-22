# Sci-Fi FPS Game

Sebuah game First-Person Shooter (FPS) dengan tema sci-fi yang dibangun menggunakan Unity Engine.

## Fitur Saat Ini

### ✅ Implementasi
- **Player Movement**: Pergerakan pemain menggunakan WASD atau arrow keys
- **Camera Control**: Kontrol kamera dengan mouse (mouse look)
- **Jump Mechanics**: Sistem lompatan dengan Space bar
- **Ground Detection**: Deteksi permukaan untuk jump yang akurat

## Kontrol Pemain

| Input | Aksi |
|-------|------|
| W / Arrow Up | Maju |
| A / Arrow Left | Ke Kiri |
| S / Arrow Down | Mundur |
| D / Arrow Right | Ke Kanan |
| Space | Lompat |
| Mouse | Lihat sekeliling |
| ESC | Unlock/Lock Cursor |

## Setup Proyek

### Struktur Folder
```
Assets/
├── Scripts/
│   ├── Player/
│   │   ├── PlayerController.cs
│   │   └── CameraController.cs
│   └── Managers/
│       └── GameManager.cs
├── Scenes/
├── Prefabs/
└── Models/
```

### Konfigurasi Scene

1. Buat scene baru bernama "Main"
2. Buat hierarki sebagai berikut:
   ```
   - Player (dengan Rigidbody)
     - Camera (dengan CameraController script)
   - Ground (Plane dengan BoxCollider)
   - GameManager (dengan GameManager script)
   ```

3. Setup Player GameObject:
   - Tambahkan Rigidbody component
   - Tambahkan Capsule Collider component
   - Attach PlayerController script
   - Set Ground Layer ke "Ground"

4. Setup Camera:
   - Child dari Player
   - Attach CameraController script
   - Position (0, 0.6, 0)

5. Setup Ground:
   - Plane scaled (10, 1, 10)
   - Set layer ke "Ground"

## Parameter yang Dapat Disesuaikan

### PlayerController
- **Move Speed**: Kecepatan pergerakan pemain (default: 5)
- **Jump Force**: Kekuatan lompatan (default: 5)
- **Ground Drag**: Hambatan saat di ground (default: 5)
- **Air Drag**: Hambatan saat di udara (default: 2)

### CameraController
- **Mouse Sensitivity**: Sensitivitas mouse (default: 2)
- **Max Look Angle**: Batas sudut pandang (default: 90)

## TODO - Fitur Selanjutnya

- [ ] Weapon System (senjata switching)
- [ ] Shooting Mechanics
- [ ] Enemy AI
- [ ] Health System
- [ ] UI (Ammo, Health, Score)
- [ ] Sound Effects
- [ ] Level Design

## Developer

ExcelRazian15-Blip
