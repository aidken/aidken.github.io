### pytest: how can I see print output to stdout

<!--
  cSpell:ignore pytest
-->

Saturday, October 26, 2024

Just like everyone, I place lots of print() statements in my code to see values of variables and the status of objects.

When I run a test with [pytest](https://docs.pytest.org/), output sent to stdout is by default captured, not printed, if the test is successful. If the test fails, output sent to stdout is printed. This behavior is explained [here](https://docs.pytest.org/en/latest/how-to/capture-stdout-stderr.html).

But sometimes I want to see output from my print statements on tests that did not fail. A quick way to do is command line option `--capture=no`. This disables capturing, letting output to stdout not suppressed.


### pytest: the scope of fixture

Monday, October 14, 2024

Some of my tasks are to parse reports, maybe text or Excel files, run analysis and generate other reports. For this I create Python packages that parse many different reports. I include [pytest](https://docs.pytest.org/) tests to test my package.

Typically my pytest scripts parses a report, generate a report object and then run [parametrized tests](https://docs.pytest.org/en/latest/how-to/parametrize.html). I include a [fixture](https://docs.pytest.org/en/latest/how-to/fixtures.html) that parses and returns a report object.

For a fixture like this, I should set [the scope of the fixture to module](https://docs.pytest.org/en/latest/how-to/fixtures.html#scope-sharing-fixtures-across-classes-modules-packages-or-session). This way I can save the number of runs of the fixture function.

### Template of Parcel 2 Binder at [codesandbox.io](https://codesandbox.io/)

Saturday, April 16th, 2022

I'd like to make the bundler of my codesandbox projects [Parcel 2](https://parceljs.org/).

[Here](https://bit.ly/3EkSvMN) is my template of simple Vanilla Javascript template with Parcel 2.

It's not easy for me to make a Yoeman generator. [Here](https://www.npmjs.com/package/generator-parcel-webapp) is a one with Parcel 1. Change a little bit in package.json and you can change the bundler Parcel 2.

### [Learning Bootstrap](https://github.com/aidken/learning_bootstrap)

Saturday, November 28th, 2020

Want to add a nice appearance on my web app. Bootstrap should be a good choice. A sample site is [here](https://szw6q.csb.app/).

Write an HTML, link Bootstrap, and add Bootstrap class to your HTML elements. Bootstrap CSS are applied to your elements.

### Github Pages: Define publishing source

Friday, November 27th, 2020

Successfully launched my Github page, finally after a few weeks. You have to [define the publishing source](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
within your repo. My default settings wrongly pointed at `master` as the publishing source, but my branch is actually `main`.

Good. I tried to solve a problem of my Github page, and could solve it.


### [CodeSandbox](https://codesandbox.io)

August 22nd, 2020

#### Learn Vanilla first

Tried writing TypeScript not successfully. Looks like I have to learn Vanilla first and then flavours.
Look, I wrote

```typescript
export default ['hello'];
```

and it does not work. CodeSandbox suggests I should use [Babel](https://babeljs.io/).

```typescript
export function hello(person) {
    ...
}
```

was understood.

Tried adding `./babelrc` but could not make Babel transpiler work. Back to Vanilla Javascript.

What do other people do? Flavours, transpilers, appear to be a big barrier in learning a scripting language.


#### Use curly braces when importing

Do not understand this curly braces, but when I put them it worked.

This does not work.

```typescript
import hello from './function';
```

This works.

```typescript
import { hello } from './function';
```

What is this curly braces for?

#### CodeSandbox hosts Node.js

So this means it can host Node.js app.

#### Running tests with [Jest](https://jestjs.io/)

Successfully ran tests with [Jest](https://jestjs.io/). CodeSandbox editor provides lots of suggestion, such as file path, in its editor. Nice.

#### What is [Percel](https://parceljs.org/)?

So Parcel builds components into the final product... It transpiles... doesn't it?

### Use VSCode shortcuts

August 20th, 2020

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
