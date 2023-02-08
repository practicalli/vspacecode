# VSCode

Install VS Code with the VSpaceCode and Calva Extensions

!!! INFO "VSCode version 1.75 used in this guide"

![VSCode Install page](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-install-page-linux.png)


## Install VSCode

=== "Debian/Ubuntu"
    [Download the `.deb` file from VSCode website](https://code.visualstudio.com/){target=_blank .md-button}

    === "Command Line"
        Change to the directory the `.deb` file was downloaded to

        ```shell
        sudo dpkg --install  code_1.75.0-1675266613_amd64.deb
        ```
        Enter the login account password when prompted

    === "Software Center"
        Open (double click) the file.  The Ubuntu software studio will open.  Click the Install button.

        ![VSCode Install via Ubuntu software center](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-install-ubuntu-software.png)

        Enter your password when prompted to install the software.

        Close the Ubuntu Software app once the install has finished.

    To run VSCode, press the `Super` key and type `code`, or open a terminal and type the command `code`.

    [Reference: VSCode on Linux](https://code.visualstudio.com/docs/setup/linux){target=_blank .md-button}

=== "MacOSX"

    [Download the `.zip` file](https://code.visualstudio.com/)

    Double-click on the downloaded archive to expand the contents.

    Drag `Visual Studio Code.app` to the `Applications` folder, making it available in the Launchpad.

    Add VS Code to your Dock by right-clicking on the icon and choosing `Options, Keep in Dock`.

    [Reference: VSCode on MacOSX](https://code.visualstudio.com/docs/setup/mac)

    Launch VSCode from the Dock, or in a command line terminal, type `code`.

=== "Windows"
    [Download the Windows Installer](https://code.visualstudio.com/)

    Run the installer which should have a name similar to `VSCodeUserSetup-{version}.exe`.

    VS Code is installed under `C:\users\{username}\AppData\Local\Programs\Microsoft VS Code`.


## VSCode Welcome wizard

When VSCode is first run the Welcome wizard will display.

![VSCode Wizard](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-welcome-getting-started-wizard-light.png#only-light)
![VSCode Wizard](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-welcome-getting-started-wizard-dark.png#only-dark)

Use the wizard to set the default theme

![VSCode Wizard - select theme](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-welcome-getting-started-wizard-select-color-theme-light.png#only-light)
![VSCode Wizard - select theme](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-welcome-getting-started-wizard-select-color-theme-dark.png#only-dark)

Select **Mark Done** link to close the wizard.


!!! HINT "Practicalli uses the Solarized Light and Dark themes"
    ++ctrl+"k"++ ++ctrl+"T"++ toggles the theme used for VSCode


## Calva Extension

The Calva extension supports Clojure and ClojureScript development

=== "Quick Open"
    ++ctrl+"p"++ to launch VS Code Quick Open, paste the extension install command and press enter.
    ```shell
    ext install betterthantomorrow.calva
    ```

=== "Extensions tab"
    Select the Extensions icon in the left hand navigation.

    Type `calva` into the search box to list the relevant extension

    Click the `Install` button next to the `VSpaceCode` extension.

    ![VSCode Calva Extensions list](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-extension-calva-light.png#only-light)
    ![VSCode Calva Extensions list](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-extension-calva-dark.png#only-dark)


After a few moments the extension will be installed.

!!! INFO "Extension install does not require restarting VSCode"


## VSpaceCode extension

=== "Quick Open"

    Launch VS Code Quick Open (Ctrl+P), paste the following command, and press enter.

    ```shell
    ext install VSpaceCode.vspacecode
    ```

=== "Extensions tab"
    Select the Extensions icon in the left hand navigation.

    Type `vspacecode` into the search box to list the relevant extension

    Click the `Install` button next to the `VSpaceCode` extension.

    ![VSCode Calva Extensions list](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-extension-vspacecode-light.png#only-light)
    ![VSCode Calva Extensions list](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-extension-vspacecode-dark.png#only-dark)

    > The _VSpaceCode Expanded_ extension is not used in this guide


After a few momments the extension will show as installed, along with several other extensions that VSpaceCode uses.

![VSCode Calva Extensions list](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-extension-installed-light.png#only-light)
![VSCode Calva Extensions list](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-extension-installed-dark.png#only-dark)


### Configuration Wizard

Once the VSpaceCode extension has finished installing, the **Getting Started with VSpaceCode** page is displayed with a configuration wizard that updates the User `settings.json` and `keybindings.json` files.

Select **Configure for you** button in the _Setting up_ section of the page.

![VSCode VSpaceCode extension - Getting Started with VSpaceCode](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-extension-vspacecode-get-started-wizard-light.png#only-light)
![VSCode VSpaceCode extension - Getting Started with VSpaceCode](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-extension-vspacecode-get-started-wizard-dark.png#only-dark)

Select **Mark Done** to close the wizard

??? "Troubleshoot Wizard"
    If the `.config/Code/User/settings.json` and `.config/Code/User/keybindings.json` files are empty then an older version of VSpaceCode may still be configured in the VSCode settings.

    Start the configuration wizard using ++ctrl+"p"++ for the quick open prompt and enter `vspacecode`

    Select _Getting Started with VSpaceCode_

    ![VSCode VSpaceCode extension - Getting Started with VSpaceCode](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-extension-vspacecode-get-started.png)

    If the wizard still does not run, quit VSCode and remove `$HOME/.vscode` and `$HOME/.config/Code` directories to ensure a clean starting point (backing up the User settings.json and keybindings.json if any useful configurations were added on top of the VSpaceCode configuration).
   
    All extensions must be installed again.
    
    If the wizard keeps failing, use the Manual configuration approach
    

??? INFO "Manual Configuration"
    Follow the [manual configuration commands](https://vspacecode.github.io/docs/#manual-configuration-optional) if the automatic setup failed or was not followed.

    `Ctrl+Shift+p` to open the VS Code command menu, type `vspacecode` to narrow the command list and select `VSpaceCode: Configure Default Settings and Keybindings`.

    ![VSpaceCode configure default settings and key bindings](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vspacecode-command-configure-default-settings-keybindings-light.png#only-light)
    ![VSpaceCode configure default settings and key bindings](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vspacecode-command-configure-default-settings-keybindings-dark.png#only-dark)

    Save the changes by opening the `settings.json` and `keybindings.json`.
   
    ++ctrl+shift+"p"++ and searching `Preference: Open Settings (JSON)` and `Preference: Open Keyboard Shortcuts (JSON)` in turn. ++ctrl+"s"++ to save the highlighted file.


### Remap Calva Esc key

Calva extension adds `Esc` as a keyboard shortcut for clearing evaluation results.  This binding breaks vim-style editing in VSpaceCode, so the Calva keyboard shortcut should be remapped.

++ctrl+shift+"p"++ to open the VSCode command menu, type `keyboard` to narrow the command list and select `Preferences: Open keyboard shortcuts (JSON)`.

Edit the `.config/Code/User/keybindings.json` file and add the following configuration to remove `Esc` from the `calva.clearInlineResults` command and create a new keyboard shortcut for that command using `Shift Esc`

Add this code before the final closing bracket, `}`, in the file.

```json title=".config/Code/User/keybindings.json"
  {
    "key": "escape",
    "command": "-calva.clearInlineResults"
  },
  {
    "key": "shift+escape",
    "command": "calva.clearInlineResults",
    "when": "editorTextFocus && !editorHasMultipleSelections && !editorReadOnly && !hasOtherSuggestions && !suggestWidgetVisible && editorLangId == 'clojure'"
  }
```

<!--
## Add the Calva specific keyboard shortcuts

> Required for VSpaceCode version 0.8.5 or earlier. Later version will include the [Clojure keybindings for the Calva extension pull request](https://github.com/VSpaceCode/VSpaceCode/pull/154).

`SPC f f` and select the `~/.vscode/extensions/vspacecode.vspacecode-0.8.5/package.json` file.

`/` followed by `Major` to find the location to add the clojure keyboard shortcuts

Open the [Clojure keybindings pull request](https://github.com/VSpaceCode/VSpaceCode/pull/154) and copy the code from the package.json change to your local package.json file.

`SPC f s` to save the file and the keyboard shortcuts will be available when opening a Clojure file.

-->


## Confirm installation

To confirm that VSpaceCode is working by opening an editor window.


Select the Explorer Icon in the left hand menu, then select *Open Folder...*  

![VSpaceCode navigation bar - explorer](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vspacecode-navigation-explorer-light.png#only-light){loading=lazy}
![VSpaceCode navigation bar - explorer](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vspacecode-navigation-explorer-dark.png#only-dark){loading=lazy}


Open a Clojure project to confirm the Calva and VSpaceCode extension are working (or any text file to test VSpaceCode).

++spc++ should open the VSpaceCode menu in the top center of VSCode.

![VSpaceCode space menu](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vspacecode-menu-space-light.png#only-light)
![VSpaceCode space menu](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vspacecode-menu-space-dark.png#only-dark)


Calva should show a welcome message

![VSpacecode - Calva welcome message](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-calva-welcome-message-after-opening-clojure-project-light.png#only-light)
![VSpacecode - Calva welcome message](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/vscode-calva-welcome-message-after-opening-clojure-project-dark.png#only-dark)
