## VI editor commands of daily use
### Navigation:

* **Move to the end of a line**: Press `Shift + A` or `End`.
* **Move to the beginning of a line**: Press `0` (zero).
* **Move to the middle of a line**: Press `Shift + M` (works for moving to the middle of the screen vertically, but no exact mid-line navigation).
* **Go one page down**: Press `Ctrl + F`.
* **Go one page up**: Press `Ctrl + B`.
* **Move to a particular line number**: Type `:<line_number>`, e.g., `:15` (to go to line 15).

### Editing:

* **Delete a line**: Press `dd`.
* **Copy a line (yank)**: Press `yy`.
* **Paste a line**: Press `p` (paste after the cursor) or `P` (paste before the cursor).

### Line Numbers:

* **Set line numbers**: Type `:set number` or `:set nu`.
* **Turn off line numbers**: Type `:set nonumber`.

### Search:

* **Search for a word**: Press `/` followed by the word and hit Enter (e.g., `/word`).
  * **Next match**: Press `n`.
  * **Previous match**: Press `Shift + N`.

### More Commands:

* **Undo last change**: Press `u`.
* **Redo last undone change**: Press `Ctrl + R`.
* **Save changes**: Press `:w`.
* **Quit vi/vim**: Press `:q`.
* **Force quit without saving**: Press `:q!`.
* **Save and quit**: Press `:wq` or `ZZ`.
* **Replace a word**: `:%s/old_word/new_word/g` (global replacement across the entire file).
* **Jump to the last position of the file**: Press `G`.
* **Jump to the first position of the file**: Press `gg`.
* **Insert text after the cursor**: Press `a` (append).

These are some of the essential `vi` commands that will help with daily tasks.

## Advance VI editor commands

### Modes

* `i` : Insert mode (allows you to type text).
* `Esc` : Return to command mode from insert mode.

### Navigation

* `h` : Move left.
* `j` : Move down.
* `k` : Move up.
* `l` : Move right.
* `w` : Move to the beginning of the next word.
* `b` : Move to the beginning of the previous word.
* `0` : Move to the beginning of the line.
* `$` : Move to the end of the line.
* `G` : Go to the end of the file.
* `gg` : Go to the beginning of the file.
* `Ctrl+f` : Move forward one screen.
* `Ctrl+b` : Move backward one screen.

### Editing

* `x` : Delete the character under the cursor.
* `dw` : Delete from the cursor to the end of the word.
* `dd` : Delete the current line.
* `D` : Delete from the cursor to the end of the line.
* `u` : Undo last change.
* `Ctrl+r` : Redo last undone change.
* `p` : Paste text after the cursor.
* `P` : Paste text before the cursor.
* `r` : Replace the character under the cursor.
* `cw` : Change the word (delete and switch to insert mode).

### Search and Replace

* `/text` : Search forward for "text".
* `?text` : Search backward for "text".
* `n` : Repeat the last search in the same direction.
* `N` : Repeat the last search in the opposite direction.
* `:%s/old/new/g` : Replace all occurrences of "old" with "new" in the file.
* `:s/old/new/g` : Replace all occurrences of "old" with "new" in the current line.

### File Operations

* `:w` : Save the file.
* `:w filename` : Save the file with a new name.
* `:q` : Quit if no changes were made.
* `:q!` : Quit without saving.
* `:wq` or `ZZ` : Save and quit.
* `:e filename` : Open another file for editing.

### Visual Mode

* `v` : Start visual mode (highlight text by moving the cursor).
* `V` : Start linewise visual mode.
* `Ctrl+v` : Start block visual mode.

> These commands cover most day-to-day editing tasks in `vi` and should improve your workflow.

### Advanced Navigation

* `H` : Move to the top of the screen.
* `M` : Move to the middle of the screen.
* `L` : Move to the bottom of the screen.
* `Ctrl+e` : Scroll the screen down one line.
* `Ctrl+y` : Scroll the screen up one line.
* `Ctrl+d` : Scroll half a screen down.
* `Ctrl+u` : Scroll half a screen up.
* `fx` : Move to the next occurrence of the character `x` in the current line.
* `Fx` : Move to the previous occurrence of the character `x` in the current line.
* `tx` : Move right until before the character `x`.
* `Tx` : Move left until after the character `x`.
* `}` : Move to the next paragraph.
* `{` : Move to the previous paragraph.
* `%` : Jump to the matching parenthesis, bracket, or brace.

### Advanced Editing

* `>>` : Indent the current line.
* `<<` : Un-indent the current line.
* `.` : Repeat the last command.
* `J` : Join the current line with the next line.
* `cc` : Change (replace) the entire line.
* `yy` or `Y` : Yank (copy) the current line.
* `yw` : Yank (copy) from the cursor to the end of the word.
* `y$` : Yank (copy) from the cursor to the end of the line.
* `C` : Change (replace) from the cursor to the end of the line.
* `>>` : Indent current line.
* `<<` : Un-indent current line.
* `:r filename` : Read contents from another file and insert after the current line.

### Buffers and Registers

* `:reg` : List all registers (yanked/cut text is stored here).
* `"ayy` : Yank (copy) a line into register `a`.
* `"ap` : Paste the contents of register `a`.
* `"bx` : Delete into register `b`.

### Macros

* `q{letter}` : Start recording a macro into the specified letter.
* `q` : Stop recording the macro.
* `@{letter}` : Play the macro stored in the specified letter.
* `@@` : Repeat the last macro.

### Marks

* `m{letter}` : Set a mark at the cursor position (local to the file).
* `'{letter}` : Jump to the start of the line where the mark `{letter}` was set.
* `"{letter}` : Jump to the exact position of the mark `{letter}`.

### Working with Multiple Files

* `:n` : Go to the next file in the buffer list.
* `:prev` : Go to the previous file in the buffer list.
* `:bnext` : Switch to the next buffer.
* `:bprev` : Switch to the previous buffer.
* `:e filename` : Open another file for editing.
* `:bd` : Delete a buffer (close the file).
* `:sp filename` : Open a file in a new horizontal split.
* `:vsp filename` : Open a file in a new vertical split.
* `Ctrl+w` : Switch between windows (splits).

### Search and Replace (Advanced)

* `:g/pattern/d` : Delete all lines containing "pattern".
* `:g/pattern/p` : Print all lines containing "pattern".
* `:v/pattern/d` : Delete all lines not containing "pattern".
* `:%s/old/new/gc` : Replace all occurrences of "old" with "new" in the entire file, with confirmation.

### Miscellaneous

* `:set number` : Show line numbers.
* `:set nonumber` : Hide line numbers.
* `:set list` : Show hidden characters like tabs (`^I`) and end-of-lines (`$`).
* `:set nolist` : Hide hidden characters.
* `:set ignorecase` : Ignore case during search.
* `:set noignorecase` : Case-sensitive search.
* `:set hlsearch` : Highlight search results.
* `:nohlsearch` : Disable search highlighting.

### Exiting

* `:wq!` : Force save and quit (even if the file is read-only).
* `:x` : Save and quit (similar to `:wq` but more concise).
* `ZQ` : Quit without saving (alternative to `:q!`).

> These commands, especially the advanced ones like macros, marks, and working with buffers, make `vi` incredibly powerful for editing and managing multiple files.

