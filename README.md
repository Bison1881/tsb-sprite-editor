# TSB Sprite Editor

A browser-based CHR tile viewer and palette editor for **Tecmo Super Bowl (NES, 1991)**.

Built as a companion to the [TSB Player Attribute Editor](https://github.com/Bison1881/tsb-editor).

---

## Features

- **CHR Tile Sheet** — view all 8,192 tiles from the CHR ROM at a glance
- **Pixel Editor** — click any tile to edit it pixel by pixel using the active palette
- **Palette Editor** — edit home uniform, away uniform, scoreboard, and field/menu colour tables per team
- **NES Master Palette** — pick from all 64 NES colours
- **Export ROM** — save your changes directly to a `.nes` file

## Usage

1. Open the editor at [https://bison1881.github.io/tsb-sprite-editor/](https://bison1881.github.io/tsb-sprite-editor/)
2. Load your `Tecmo Super Bowl (USA).nes` ROM file
3. Select a team and colour table from the left panel
4. Click a palette slot to select it, then pick a colour from the NES master palette
5. Click any tile in the sheet to open it in the pixel editor
6. Draw with the palette slot colours
7. Click **Export ROM** to save your edited ROM

## ROM Compatibility

| Field | Value |
|---|---|
| File | `Tecmo Super Bowl (USA).nes` |
| CRC-32 | `fc5e400f` |
| Size | 393,232 bytes |
| Mapper | 4 (MMC3) |

## Technical Notes

- CHR ROM starts at file offset `0x40010` (128KB, 8,192 tiles)
- Palette tables are in PRG ROM at known fixed offsets (home `0x23D5C`, away `0x23DCC`, scoreboard `0x343B8`, field `0x1A010`)
- Each palette entry is 4 bytes — one NES colour index per slot
- Tile data is 2bpp, two 8-byte bitplanes per tile

## Related Projects

- [TSB Player Attribute Editor](https://github.com/Bison1881/tsb-editor) — edit player names, stats, and jerseys
- [KGJ MLB Editor](https://github.com/Bison1881/kgj-mlb-editor) — Ken Griffey Jr. Presents Major League Baseball (SNES)

## License

MIT — see [LICENSE](LICENSE)
