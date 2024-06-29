
These are the commands needed to compile the CP/400 application

`
CRTDSPF FILE(RUNCPM/TERMINAL) SRCFILE(RUNCPM/QDDSSRC) SRCMBR(TERMINAL)
`

`
CRTCMOD MODULE(RUNCPM/MAIN) SRCFILE(RUNCPM/QCSRC) DBGVIEW(*ALL) SYSIFCOPT(*IFSIO)
`

`
CRTPGM PGM(RUNCPM/RUNCPM) MODULE(RUNCPM/MAIN)
`

To start an instance of CP/400 you need to pass the root
path containing your CPM directory structure.

Example directory structure:
`
/CPM/ZORK1
/CPM/ZORK1/AUTOEXEC.TXT
/CPM/ZORK1/A
/CPM/ZORK1/A/0
/CPM/ZORK1/A/0/ZORK1.COM
/CPM/ZORK1/A/0/ZORK1.DAT
`

Launching Zork:
`
CALL RUNCPM/RUNCPM PARM('/CPM/ZORK1') 
`
