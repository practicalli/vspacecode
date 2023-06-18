# Clojure Workflow

The REPL workflow is an effective way to develop Clojure projects.


## Create Project

[:globe_with_meridians: Creating projects using a template](https://practical.li/clojure/clojure-cli/projects/templates/){target=_blank} is a quick way to get started.  A template will create the project structure, add libraries and even include example code.

??? INFO "Practicalli Project Templates"
    [:fontawesome-brands-github: practicalli/project-templates](https://github.com/practicalli/project-templates){target=_blank} provide production level templates that include Practicalli [:globe_with_meridians: REPL Reloaded Workflow](https://practical.li/clojure/clojure-cli/repl-reloaded/){target=_blank} tools, Docker & Compose configurations, Makefile tasks for a consistent command line UI and GitHub workflows to manage quality of code and configuration.

    - `practicalli/minimal` - production level project with minimal code examples
    - `practicalli/application` - production level project template with Mulog, Docker, Make, MegaLinter, etc.
    - `practicalli/service` - production level web services template with Integrant, Http-kit, Reitit, Mulog, Docker, Make, MegaLinter, etc.


Use deps-new to create a project, specifying a template and a name for the project.

Open a terminal window and change to a suitable folder and create a project using `:project/create` alias from [:globe_with_meridians: Practicalli Clojure CLI Config](https://practical.li/clojure/clojure-cli/practicalli-config/){target=_blank}

```bash
clojure -T:project/create
```

The `-T` execution option runs the tool with Clojure.exec which uses keywords to specify the options for creating the project.

> `:project/create` alias uses `:template practicalli/minimal` `:name practicalli/playground` arguments by defauls, which can e overridden on the command line
>
> The name of the project is of the form `domain/app-lib-name`. Use a company name or Git Service account name as the `domain`.


## Open Project

Run the command `code .` from the root of a Clojure project or run VSCode and use the VSpaceCode key bindings to open a project.

++spc++ ++"f"++ ++"f"++ and open the Folder that contains a Clojure project. Select the top level of the folder, e.g. `playground` and click **OK**

![VSpaceCode Clojure CLI Project](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-deps-light.png?raw=true#only-light)
![VSpaceCode Clojure CLI Project](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-deps-dark.png?raw=true#only-dark)


## Start a REPL

Either start a terminal UI repl and connect to it from Calva, or use Calva jack-in to start a repl and automatically connect.

??? INFO "Start REPL via VSCode terminal"
    **Ctrl+`** toggles open the [VSCode Integrated terminal](https://code.visualstudio.com/docs/editor/integrated-terminal){target=_blank}.  Or open your operating system terminal.

    In the terminal, change to the folder than contains your project, e.g. `cd projects/clojure/playground`

    [Configure the VS Code internal terminal to use the GitBash shell](https://code.visualstudio.com/docs/editor/integrated-terminal#_configuration){target=_blank}.

=== "Terminal UI"
    Change into the directory and test the project runs by starting a REPL with [:globe_with_meridians: Terminal REPL](https://practical.li/clojure/clojure-cli/repl/){target=_blank}

    !!! EXAMPLE "Start rich terminal UI REPL"
        ```bash
        cd playground && clojure -M:repl/rebel
        ```

    A repl prompt should appear

    ![Clojure REPL rebel readline](https://github.com/practicalli/graphic-design/blob/live/clojure/rebel/clojure-repl-rebel-prompt-light.png?raw=true#only-light)
    ![Clojure REPL rebel readline](https://github.com/practicalli/graphic-design/blob/live/clojure/rebel/clojure-repl-rebel-prompt-dark.png?raw=true#only-dark)

    Type code expressions at the repl prompt and press RETURN to evaluate them.

    !!! EXAMPLE "Evaluate code at REPL prompt"
        ```clojure
        (+ 1 2 3 4 5)
        ```

    Switch to VSpaceCode with the Clojure `playground` project open.

    ++comma++ ++"'"++ to connect to the REPL process started in the terminal UI

    ![VSpaceCode connect to running REPL](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-connect-light.png?raw=true#only-light)
    ![VSpaceCode connect to running REPL](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-connect-dark.png?raw=true#only-dark)

    Select the tool to use to start the repl

    ![VSpaceCode Clojure Jack-in build tool](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-jack-in-type-deps-light.png?raw=true#only-light)
    ![VSpaceCode Clojure Jack-in build tool](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-jack-in-type-deps-dark.png?raw=true#only-dark)

    Confirm the **host** and **port** of the REPL, this should be automatically detected. These details were shown when the REPL was run in the terminal.

    ![VSpaceCode connect to running REPL - specify hostname and port](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-connect-host-port-light.png?raw=true#only-light)
    ![VSpaceCode connect to running REPL - specify hostname and port](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-connect-host-port-dark.png?raw=true#only-dark)

    Wait a few moments for the REPL to start.


=== "Calva jack-in"
    Open the `playground` project in VS Code.

    `, "` to jack-in to a Clojure REPL for the project.  This starts an external REPL process and connects to it.

    Select `deps.edn` for Clojure CLI when prompted for the project type

    ![VSpaceCode Start REPL via jack-in](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-jack-in-light.png?raw=true#only-light)
    ![VSpaceCode Start REPL via jack-in](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-jack-in-dark.png?raw=true#only-dark)

    Select the tool to use to start the repl

    ![VSpaceCode Clojure Jack-in build tool](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-jack-in-type-deps-light.png?raw=true#only-light)
    ![VSpaceCode Clojure Jack-in build tool](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-jack-in-type-deps-dark.png?raw=true#only-dark)

    Wait a few moments for the REPL to start.


Once the REPL is connected, the `REPL` name with a lightning bolt icon is displayed in the status bar.

![VSpaceCode REPL connected](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-repl-connected-light.png?raw=true#only-light)
![VSpaceCode REPL connected](https://github.com/practicalli/graphic-design/blob/live/editors/vspacecode/vspacecode-clojure-project-repl-connected-dark.png?raw=true#only-dark)

??? HINT "Troubleshooting"
    If the REPL did not start, the nREPL link in the bottom blue bar will show the word "Disconnected".

    ![VS Code - Calva - Start REPL - nREPL button](/images/vscode-calva-clojure-repl-connect-nrepl-button.png)

    Open the Output tab to see the progress of the REPL starting.

    ![VS Code - Calva - Start REPL - nREPL button](/images/vscode-calva-clojure-repl-connect-output.png)

    Try running a REPL in a terminal and connecting to it.


## Evaluating Clojure code

`, e f` to evaluate a top-level expression and see the results inline.  Or `, e s` to select a specific expression and `, e e` to evaluate it.

`, e l` to clear all the evaluated results.

| Keybinding | Description                                          |
|------------|------------------------------------------------------|
| `, e ;`    | Evaluate the current expression and paste as comment |
| `, e :`    | Evaluate the current expression and paste as comment |
| `, e e`    | Show the result of the current expression            |
| `, e f`    | Show the result of the top level expression          |
| `, e l`    | Clear all the evaluated results                      |
| `, e n`    | Evaluate all code in the current file/namespace      |
| `, e w`    | Replace the expression with its result               |


## Running tests

`, e n` to evaluate all the unit test code in the current window

`, t a` to run all the unit tests in the project

`, t f` to run just the failing tests

| Keybinding | Description                             |
|------------|-----------------------------------------|
| `, t a`    | Run all tests in the project            |
| `, t f`    | Run all tests for the current namespace |
| `, t n`    | Run all tests for the current namespace |
| `, t t`    | Run all tests for the current namespace |

!!! HINT "Test results shown in REPL"
    The REPL window is used to display the results of running unit tests


## Commenting / uncommenting code

`SPC c l` toggles a comment on the current line.

Use the **Add Line Comment** command to place `;;` at the start of a line, which comments it out.


## Linting

`, c n` and `, c N` cycle through clj-kondo linting warnings


## Increase / decrease font size

`Ctrl +` and `Ctrl -` will increase and decrease the size of the whole editor.

`SPC SPC` and type the command `Preference: Open Settings (JSON)` to open the `settings.json` configuration file.  Update the value for `editor.fontSize` and save the file.  The font should update immediately in the VS Code UI.

Other useful options that can be added to the `settings.json` configuration

```json title="settings.json"
   "workbench.colorTheme": "Solarized Light",
    "editor.fontSize": 14,
    "editor.fontFamily": "'Fira Code', 'Ubuntu Mono', 'Droid Sans Mono', 'monospace', monospace, 'Droid Sans Fallback'",
    "window.zoomLevel": 1,
    "calva.paredit.defaultKeyMap": "strict"
```


## Structural editing - Paredit

`, k` is the structural editing menu.

Structural editing ensures code can be written and edited without breaking the structure of Clojure.  Structural editing ensures you dont have uneven parentheses, `()`, `[]`, `{}`, etc.

The [Calva visual Guide to Paredit](https://calva.io/paredit/) includes lots of examples of using Structural editing.

| Keybinding | Description                                        |
|------------|----------------------------------------------------|
| `, k .`    | Toggle paredit strict mode                         |
| `, k b`    | Barf forwards                                      |
| `, k c`    | Convolute expression                               |
| `, k h`    | Jump backwards                                     |
| `, k j`    | Jump forward down an expression                    |
| `, k k`    | Jump backwards down an expression                  |
| `, k l`    | Jump forward an expression                         |
| `, k r`    | Raise an expression (over-write parent expression) |
| `, k s`    | Slurp forward                                      |
| `, k t`    | Transpose expression                               |
| `, k w (`  | Wrap with ()                                       |
| `, k w [`  | Wrap with []                                       |
| `, k w {`  | Wrap with {}                                       |
| `, k w "`  | Wrap with ""                                       |
| `, k w p`  | rewrap with ()                                     |
| `, k w s`  | rewWrap with []                                    |
| `, k w c`  | rewWrap with {}                                    |
| `, k w q`  | rewWrap with ""                                    |
