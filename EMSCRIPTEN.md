# Emscripten

## Build

```
emmake make
```

## Link

```
em++ -flto -O3 -fno-rtti -fno-exceptions *.o libWildMidi.a libfluidsynth.a libGL.a -o index.html -sUSE_SDL=2 -sUSE_ZLIB -sFULL_ES2 -lGL -sASYNCIFY -sASYNCIFY_IGNORE_INDIRECT -sASYNCIFY_ONLY=@funcs.txt -sENVIRONMENT=web --preload-file DATA/ --preload-file DELPHINE.INI --preload-file TRIGO.DAT --closure 1 -Wl,-u,ntohs
```
