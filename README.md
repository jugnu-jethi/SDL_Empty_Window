SDL2 Setup

Install mingw64 @https://sourceforge.net/projects/mingw-w64/
 - select arch: x86_64; thread: posix; exception: seh
 
Install build-tools @https://github.com/gnu-mcu-eclipse/windows-build-tools/releases
 - for utilities like rm and such


Edit windows environment and ADD:
 - "C:\Program Files\GNU MCU Eclipse\Build Tools\2.11-20180428-1604\bin"
 - "C:\Program Files\mingw-w64\x86_64-8.1.0-posix-seh-rt_v6-rev0\mingw64\bin"
 - "C:\Users\Jugnu\Downloads\SDL2-devel-2.0.8-mingw\SDL2-2.0.8\x86_64-w64-mingw32\bin"
 
In Eclipse, under C/C++ Build -> Settings:
 - Under GCC C++ Compiler -> Includes, add Include path (-l) 
    -- "C:\Users\Jugnu\Downloads\SDL2-devel-2.0.8-mingw\SDL2-2.0.8\x86_64-w64-mingw32\include\SDL2"
 - Under MinGW Linker -> Libraries, add Libraries (-l)
    -- mingw32
	-- SDL2Main
	-- SDL2
- Under MinGW Linker -> Libraries, add to Library search path (-L)
    -- "C:\Users\Jugnu\Downloads\SDL2-devel-2.0.8-mingw\SDL2-2.0.8\x86_64-w64-mingw32\lib"