# Assembly-Programs
This projects stores all the assignments of Computer Organization and Assembly Language I have covered so far being a student of Bacholers in Computer Science at FAST NUCES Lahore 
# COAL – Assembly Language Programs

Name: Aaliyan Aziz 
Roll No: L250718

## Description
Assignment3/Q2.asm is a 16-bit 8088 program that builds a text viewport
directly in video memory (0xB800):

- bordered double-line window (rows 3–21, cols 8–72) with a centred title banner (0x1E)
- multi-line document streamed into the window with LODSB/STOSW
- scroll_window_up scrolls only the window interior (MOVSW + row strides, STOSW to blank)
- find_and_highlight finds a keyword with REPE CMPSB and rewrites only the attribute bytes
- status bar on row 23 with the match count printed by an iterative stack-based printNum

All procedures take stack parameters, use [bp+n] / [bp-n], keep locals on the stack,
save/restore registers and clean up with ret n.

## Tools
- NASM
- DOSBox

## Assemble and run

nasm Assignment3/Q2.asm -o Q2.com
dosbox
Z:\> mount c path\to\folder
Z:\> c:
C:\> Q2.com

Press a key to step through: initial view → scrolled view → highlighted view + status bar.

## Folder structure

COAL/
├── README.md
└── Assignment3/
    └── Q2.asm


## Output screenshots
![Step 1](step%201.png)
![Step 2](step%202.png)

