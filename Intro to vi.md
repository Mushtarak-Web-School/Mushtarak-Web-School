# Intro to vi

write in the terminal ``vi hello.txt`` and you are about to create a new file hello.txt
vi is a code editor, with powerful functionalities.


- ``i`` insert before cursor to the file.
- ``a`` append after cursor to the file.
- ``s`` substitiute or replace file content.

press ``i`` to enter vi insert mode.
press ``esc`` to back to command mode

### commands:
- ``yy`` copy line.
- ``dd`` cut line.
- ``p`` past.
- ``dw`` delete word.
- ``u`` undo.
- ``y$`` copy to the end of line.
- ``x`` cut title.
- ``y^`` copy to the begining of line.

if you press ``:`` you will enter the last line mode:

- ``:w`` write changes to the file.
- ``:wq`` write changes to the file and quit.
- ``:q`` quit.
- ``:set number`` show line number.
- ``:/wordpattern`` search for word.
- ``:1,$ s/e/E/g`` change globally (e) to (E).
- ``:1,$ s/o[nr]/oo/g change globally any (o) followed by (n) or (r) with (oo).
- ``:%`` search in the whole file.
- ``:% s/^CA[1-9]\{4\}/CAXXXX/`` change the four numbers after ``CA`` with ``XXXX``.
- ``:% s/^CA[0-9]\{3\}\>/CAXXX/`` TODO:
- ``:% s/^CA[0-9]\{3\}\ua0/CAXXX/``TODO:
