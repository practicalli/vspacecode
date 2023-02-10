# VSCode quick start

The VSCode quick start covers Calva essentials for Clojure development, including Calva and VSpaceCode key bindings.

Open a Clojure project and star a REPL from Calva or connect to a command line repl.  Calva is then ready for writing Clojure code and evaluating results instantly.

The [Calva User Guide](https://calva.io/) provides a detailed guide to the features of Calva, although the key bindings for VSpaceCode are not included in that guide.


## Open a Clojure project

Run the command `code .` from the root of a Clojure project or run VSCode and use the VSpaceCode key bindings to open a project.

++spc++ ++"f"++ ++"f"++ and open the Folder that contains a Clojure project. Select the top level of the folder, e.g. `playground` and click **OK**


## Launch REPL from Calva

Calva can start a REPL process using Clojure CLI or Leiningen.

For Clojure CLI, aliases from the project `deps.edn` can be selected to modify the REPL startup.

??? HINT "Use Command Line REPL for Clojure CLI and user aliases"
    Calva does not read aliases from the Clojure CLI user configuration, i.e. `$XDG_CONFIG_HOME/clojure/deps.edn` or `$HOME/.clojure/deps.edn`

    Start a REPL via the command line to include aliases from the user configuration, e.g.
    ```
    clojure -M:dev/reloaded:repl/rebel
    ```

++comma++ ++double-quote++ to jack-in to a Clojure REPL for the project.  This starts an external REPL process and connects to it.

> Alternative, use ++comma++ ++single-quote++ to connect to an external REPL process that has already started.

Select either `deps.edn` for Clojure CLI or `Leiningen` when prompted for the project type

![VS Code - Calva - Start REPL - nREPL button](https://raw.githubusercontent.com/practicalli/graphic-design/live/vspacecode/screenshots/vspacecode-clojure-repl-jack-in-leiningen.png)

Wait a few moments for the REPL to start.

A new REPL window will open when the Clojure REPL is ready

![VS Code - Calva - Start REPL - nREPL button](/images/vspacecode-calva-jack-in-repl-output.png)

The VSCode Status Bar shows when the Clojure REPL is connected

![VSpaceCode Status Bar showing REPL connected](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vspacecode-clojure-status-bar-repl-connected-light.png#only-light)
![VSpaceCode Status Bar showing REPL connected](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vspacecode-clojure-status-bar-repl-connected-dark.png#only-dark)


### Troubleshooting

If the REPL did not start, the nREPL link in the bottom blue bar will show the word "Disconnected".

![VS Code - Calva - Start REPL - nREPL button](/images/vscode-calva-clojure-repl-connect-nrepl-button.png)

Open the Output tab to see the progress of the REPL starting.  Ask your coach for help if you see output other than that below.

![VS Code - Calva - Start REPL - nREPL button](/images/vscode-calva-clojure-repl-connect-output.png)

Try running a REPL in the command line and connecting to it (details at bottom of this page).


## Start command line REPL

++ctrl+grave++ toggles open the [VSCode Integrated terminal](https://code.visualstudio.com/docs/editor/integrated-terminal), or use the operating system terminal.

??? INFO "Windows GitBash users"
    [Configure the VS Code internal terminal to use the GitBash shell](https://code.visualstudio.com/docs/editor/integrated-terminal#_configuration).


??? HINT "Practicalli recommends Kitty Terminal"
    [Kitty Terminal](https://practical.li/engineering-playbook/command-line/kitty-terminal/) is a fast, feature-rich GPU based terminal emulator.

In the terminal, change to the folder than contains your project, e.g. `cd projects/clojure/playground`

=== "Clojure CLI"
    Start a REPL process via Clojure CLI tools, using the [Practicalli Clojure CLI Config](/images/vscode-calva-clojure-repl-connect-nrepl-button.png) aliases which also starts an nREPL server that an editor can connect to.

    ```
    clojure -M:repl/basic
    ```

    If you also wish to have an interactive terminal REPL, include rebel readline when starting the REPL

    ```
    clojure -M:repl/rebel
    ```

=== "Leiningen"
    To use Leiningen, type the command `lein repl` in the terminal.

    ![VS Code Terminal - Clojure REPL running](/images/vscode-calva-terminal-repl-running.png)


### Connecting to external REPL

++ctrl+single-quote++ to connect to an external REPL process from Calva / VSpaceCode.

For the project type select either **deps.edn** for Clojure CLI or Leiningen when prompted



Confirm the **host** and **port** of the REPL, this should be automatically detected. Host and port details were shown in the output when running the REPL in the terminal.

![Calva - connect to running REPL](/images/vscode-calva-connect-host-and-port.png)

Wait a few moments for the REPL to start.

A new REPL window will open when the Clojure REPL is ready

![VS Code - Calva - Start REPL - nREPL button](/images/vspacecode-calva-connect-repl-output.png.png)


In the bottom left of the VS Code window, check the status of the **nrepl** connection.  If you are connected, then the *disconnected* status should disappear

In the bottom left of the VS Code window, check the status of the **nrepl** connection.  If you are connected, then the *disconnected* status should disappear

![Calva - nrepl disconnected](/images/vscode-calva-nrepl-disconnected.png)


## Evaluate Code

Once you have a running REPL, use these commands to help you develop the code.

++comma++ ++"e"++ ++"f"++ to evaluate a top-level expression and see the results inline.  Or ++comma++ ++"e"++ ++"s"++ to select a specific expression and ++comma++ ++"e"++ ++"e"++ to evaluate it.

++comma++ ++"e"++ ++"l"++ to clear all the evaluated results.

| Keybinding                       | Description                                          |
|----------------------------------|------------------------------------------------------|
| ++comma++ ++"e"++ ++semi-colon++ | Evaluate the current expression and paste as comment |
| ++comma++ ++"e"++ ++colon++      | Evaluate the current expression and paste as comment |
| ++comma++ ++"e"++ ++"e"++        | Show the result of the current expression            |
| ++comma++ ++"e"++ ++"f"++        | Show the result of the top level expression          |
| ++comma++ ++"e"++ ++"l"++        | Clear all the evaluated results                      |
| ++comma++ ++"e"++ ++"n"++        | Evaluate all code in the current file/namespace      |
| ++comma++ ++"e"++ ++"s"++        | Select current expression                            |
| ++comma++ ++"e"++ ++"w"++        | Replace the expression with its result               |


!!! HINT "REPL history"
    The REPL window maintains a history of the code typed in and can be navigated by pressing `Alt+Up` and `Alt+Down`.


## Running tests

Unit tests can be run from Calva

++comma++ ++"e"++ ++"n"++ to evaluate all the unit test code in the current window

++comma++ ++"t"++ ++"a"++ to run all the unit tests in the project

++comma++ ++"t"++ ++"f"++ to run just the failing tests

| Keybinding                | Description                             |
|---------------------------|-----------------------------------------|
| ++comma++ ++"t"++ ++"a"++ | Run all tests in the project            |
| ++comma++ ++"t"++ ++"f"++ | Run failing tests                       |
| ++comma++ ++"t"++ ++"n"++ | Run all tests for the current namespace |
| ++comma++ ++"t"++ ++"t"++ | Run current test                        |


!!! HINT "Test results shown in REPL"
    The REPL window is used to display the results of running unit tests


## Commenting / uncommenting code

Use  `;;` at the start of a line, which comments it out.

!!! HINT "VSpaceCode comment key binding"
    `SPC c l` toggles a comment on the current line.

!!! WARNING "Line comments keybindings ?"
    The **Add Line Comment** command to place line comment command is broken in Calva, it only produces a single semi-colon
    TODO: is this configurable in Calva.


## Increase / decrease font size

`Ctrl +` and `Ctrl -` will increase and decrease the size of the whole editor.

`Ctrl Shift P` and type the command `Preference: Open Settings (JSON)` to open the `settings.json` configuration file.  Update the value for `editor.fontSize` and save the file.  The font should update immediately in the VS Code UI.

Other useful options that can be added to the `settings.json` configuration

```
   "workbench.colorTheme": "Solarized Light",
    "editor.fontSize": 14,
    "editor.fontFamily": "'Fira Code', 'Ubuntu Mono', 'Droid Sans Mono', 'monospace', monospace, 'Droid Sans Fallback'",
    "window.zoomLevel": 1,
    "calva.paredit.defaultKeyMap": "strict"
```


## Structured editing - Paredit

Once you get the basics of Clojure development, you can try structural editing which is a way to edit your code without breaking the structure of Clojure.  Structural editing ensures you dont have uneven parentheses, `()`, `[]`, `{}`, etc.

The [Calva visual Guide to Paredit](https://calva.io/paredit/) includes lots of examples of using Structural editing.


### Linting

`, c n` and `, c N` cycle through clj-kondo linting warnings


### Increase / decrease font size

`Ctrl +` and `Ctrl -` will increase and decrease the size of the whole editor.

`SPC SPC` and type the command `Preference: Open Settings (JSON)` to open the `settings.json` configuration file.  Update the value for `editor.fontSize` and save the file.  The font should update immediately in the VS Code UI.

Other useful options that can be added to the `settings.json` configuration

```
   "workbench.colorTheme": "Solarized Light",
    "editor.fontSize": 14,
    "editor.fontFamily": "'Fira Code', 'Ubuntu Mono', 'Droid Sans Mono', 'monospace', monospace, 'Droid Sans Fallback'",
    "window.zoomLevel": 1,
    "calva.paredit.defaultKeyMap": "strict"
```


### Structural editing - Paredit

++comma++ ++"k"++ is the structural editing menu.

Structural editing ensures code can be written and edited without breaking the structure of Clojure.  Structural editing ensures you dont have uneven parentheses, `()`, `[]`, `{}`, etc.

The [Calva visual Guide to Paredit](https://calva.io/paredit/) includes lots of examples of using Structural editing.

| Keybinding                                 | Description                                        |
|--------------------------------------------|----------------------------------------------------|
| ++comma++ ++"k"++ ++period++               | Toggle paredit strict mode                         |
| ++comma++ ++"k"++ ++"b"++                  | Barf forwards                                      |
| ++comma++ ++"k"++ ++"c"++                  | Convolute expression                               |
| ++comma++ ++"k"++ ++"h"++                  | Jump backwards                                     |
| ++comma++ ++"k"++ ++"j"++                  | Jump forward down an expression                    |
| ++comma++ ++"k"++ ++"k"++                  | Jump backwards down an expression                  |
| ++comma++ ++"k"++ ++"l"++                  | Jump forward an expression                         |
| ++comma++ ++"k"++ ++"r"++                  | Raise an expression (over-write parent expression) |
| ++comma++ ++"k"++ ++"s"++                  | Slurp forward                                      |
| ++comma++ ++"k"++ ++"t"++                  | Transpose expression                               |
| ++comma++ ++"k"++ ++"w"++ ++"("++          | Wrap with ()                                       |
| ++comma++ ++"k"++ ++"w"++ ++bracket-left++ | Wrap with []                                       |
| ++comma++ ++"k"++ ++"w"++ ++brace-left++   | Wrap with {}                                       |
| ++comma++ ++"k"++ ++"w"++ ++double-quote++ | Wrap with ""                                       |
| ++comma++ ++"k"++ ++"w"++ ++"p"++          | rewrap with ()                                     |
| ++comma++ ++"k"++ ++"w"++ ++"s"++          | rewWrap with []                                    |
| ++comma++ ++"k"++ ++"w"++ ++"c"++          | rewWrap with {}                                    |
| ++comma++ ++"k"++ ++"w"++ ++"q"++          | rewWrap with ""                                    |
