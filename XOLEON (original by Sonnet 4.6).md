# Xoleon

---

### Etymology

*from **xol** (XOR + ROL, the 16-bit encryption underlying Gen V–VII Pokémon text) and **eon** (the 3DS as evolution of the DS — the ndspy successor no library built)*

---

### Current

Pokémon text decryption — Gen IV through VII
- Gen IV: full character map, 9-bit packed trainer names, control codes
- Gen V–VII: XOR/ROL key derivation, 9-bit packed text, charmap substitutions, control codes; Gen VI/VII uses identical methodology — import only

3DS container layer
- NCCH header parsing (product code, region, short title)
- RomFS filesystem traversal (directory tree, path reconstruction)
- GARC — single sub-file and full archive reads

### Planned

- **LZ11** — repackaged into xoleon; first standalone Python implementation
- **ExeFS** — code.bin access for Gen VI/VII ROM hacking
- **CGFX/BCH** — 3DS graphics; no Python library exists
- **BCSAR/BCSTM/BCWAV** — deferred until NDS audio (SDAT) is tackled in parallel
