# vlink

> link support in profanOS has been stopped since kernel 1.1.8b (May 2024), the use of tcc as a linker is strongly recommended

A portable linker for multiple file formats.

vlink is a portable linker, written in ANSI-C, that can read and write a wide range of object- and executable file formats. It can be used to link a specific target format from several different input file formats, or for converting, stripping and manipulating files.

The linker can be controlled by GNU-style linker scripts to generate absolute code, but it also runs very well with default rules to create relocatable executables, as required for AmigaOS or MorphOS.

Of course there might be technical restrictions that object files of different architectures cannot be merged because of incompatible relocation types, differing endianess or symbol-names with and without leading underscores. But in theory everything is possible!
Currently the following object and executable file formats are supported by vlink:

    ELF 32bit PowerPC big endian
    ELF 32bit PowerPC AmigaOS (special dynamic linking rules)
    ELF 32bit PowerPC MorphOS (relocatable executables)
    ELF 32bit PowerPC PowerUp (relocatable executables)
    ELF 32bit M68k big endian
    ELF 32bit x86 little endian
    ELF 32bit x86 AROS (relocatable executables)
    ELF 32bit ARM little endian
    ELF 64bit x86_64 little endian
    a.out Sun/010 (also Amiga/Atari 68000)
    a.out Sun/020 (also Amiga/Atari 68020+)
    a.out MiNT (embedded in Atari TOS format)
    a.out Jaguar (M68k with support for RISC relocations)
    a.out NetBSD/68k (4k and 8k pages)
    a.out NetBSD/386
    a.out PC/386
    a.out generic
    AmigaOS hunk format
    EHF, extended hunk format (WarpOS)
    Atari TOS format (writing only)
    Motorola S-Records (writing only)
    Intel-hex format (writing only)
    AMSDOS format (Amstrad/Schneider CPC)
    Commodore 8-bit PRG format
    Raw binaries (writing only)
    VOBJ, proprietary versatile object format (reading only)
