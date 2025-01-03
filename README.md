# turbopascal-textgraf
Textmode and Graphics Mode Lib for Turbo Pascal on DOS (Predecessor of the X-LIB Unit)

## Compile
Start compile.bat
Uses Turbo Pascal 6.0 installed in c:\progrs\tp\

## Usage
In your pascal code with add following usage
use textgraf

## Example Graphics Mode 13

case InitTextGraf of
     1: begin end;
end;
GrafikMode($13);
