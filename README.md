# turbopascal-textgraf
Textmode and Graphics Mode Lib for Turbo Pascal on DOS (Predecessor of the X-LIB Unit)

## Compile
Compile.bat uses Turbo Pascal 6.0 installed in c:\progrs\tp\
```
compile.bat
```

## Usage
In your pascal code with add following usage
```
use textgraf
```

## Example Graphics Mode 13

```
case InitTextGraf of
     1: begin end;
end;
GrafikMode($13);
```

## Methods

| Method | Description |
|--------|-------------|
| `InitTextGraf: integer` | Must be called at the very beginning of the program while still in text mode. Without this, the rest won't work. Returns 0 if everything is OK, -1 for unknown video type, and 1 for insufficient memory (requires about 12KB). |
| `SetPaletteSave(On: boolean)` | Call with `On = true` after `InitTextGraf` and in text mode. Saves the text palette and reserves memory for the graphics palette, which will then be used automatically. `On = false` disables this automation and frees the memory for the palettes (about 1.5KB). |
| `ToText` | Switches from graphics to text mode. Saves the screen content, etc. |
| `ToGraph` | Switches back to graphics mode. A graphics mode should have been exited with `ToText` beforehand to initialize all values. |
| `GrafikMode(Mode: byte)` | Sets the video mode. |
| `GetMonTyp: MonitorTyp` | Returns the monitor type. |
| `SetVGAColors(var Colors: VGAColors)` | Sets the VGA colors. |

