### [Learning Bootstrap](https://github.com/aidken/learning_bootstrap)
##### Saturday, November 28th, 2020

Want to add a nice appearance on my web app. Bootstrap should be a good choice. A sample site is [here](https://szw6q.csb.app/).


### Github Pages: Define publishing source
##### Friday, November 27th, 2020

Successfully launched my Github page, finally after a few weeks. You have to [define the publishing source](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
within your repo. My default settings wrongly pointed at `master` as the publishing source, but my branch is actually `main`.

Good. I tried to solve a problem of my Github page, and could solve it.


### Use VSCode shortcuts!
##### August 20th, 2020

I came to [Visual Code Studio](https://code.visualstudio.com/docs) from Emacs. From the beginning I used VSCode in the Emacs way, not knowing features VSCode provides. Why don't I try some?

#### Kill a line or lines
<kbd>Ctrl</kbd> + <kbd>k</kbd>
This deletes a line where cursor currently is. If multiple lines are selected, then that bunch of lines are deleted.

#### Move a line or lines up or down
<kbd>Ctrl</kbd> + <kbd>↑</kbd> or + <kbd>↓</kbd>
Move an entire line up or down. Similarly if multiple lines are selected, then that bunch of lines are moved.

#### Indent / Outdent
- Indent / Outdent <kbd>Ctrl</kbd> + <kbd>[</kbd> / <kbd>]</kbd>

#### Auto Completion (aka IntelliSense)
I changed from default <kbd>Ctrl</kbd> + <kbd>Space</kbd> to <kbd>Ctrl</kbd> + <kbd>m</kbd>.
 - Trigger Suggestion <kbd>Ctrl</kbd> + <kbd>m</kbd>
 - Trigger parameter hints <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>m</kbd>

#### Cursor position, Go back and forward
 - Go back / forward ... <kbd>Alt</kbd> + <kbd>←</kbd> / <kbd>→</kbd>
   You can go back to the part you previously edited. Useful. Even to a different file.

   Update August 20th 2020, I changed this to <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>f</kbd> / <kbd>b</kbd>

   Note: Expand / Shrink Selection ... When text is selected, hit <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>f</kbd> / <kbd>b</kbd>

#### Fold/Unfold region (such as function definition.)
 - <kbd>Ctrl</kbd> <kbd>K</kbd> + <kbd>Ctrl</kbd> <kbd>[</kbd> / <kbd>]</kbd>
   In many occasions you want to collapse a region of code for brevity. Good. I used <kbd>Ctrl</kbd> + <kbd>k</kbd> to kill a line, but I disabled it as VSCode use <kbd>Ctrl</kbd> + <kbd>k</kbd> in many shortcuts. You can use <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>k</kbd> to kill an entire line.

   Now, be careful when you use <kbd>Ctrl</kbd> + <kbd>k</kbd>. It triggers many different actions.

#### Rename variable
 - Rename ... <kbd>F2</kbd>
   If you rename once, VSCode rename it everywhere (maybe in the same file only.) Nice!

#### Definition
Often you want to know the definition of your variable or function.

 - Go to definition ... <kbd>F12</kbd>
   You can go to where something is defined. Useful when you want to edit, but this should not happen so often.

 - Peek definition ... <kbd>Alt</kbd> + <kbd>F12</kbd>
   Just look at codes of definition, but you cannot edit. Probably this is used more often.

 - Go to reference ... <kbd>Shift</kbd> + <kbd>F12</kbd>
   Show where var/func is actually called
