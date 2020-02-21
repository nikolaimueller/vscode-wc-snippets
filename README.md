# vscode-wc-snippets

Webcomponent v1 (custom element) snippets for Visual Studio Code.

## Setup in VSCode

__TODO:__ Publish snippet(s) as extension in the [Visual Studion Marketplace](https://marketplace.visualstudio.com/VSCode).

### Workaround:

__Add custom snippet(s) by hand to Visual Studio Code:__

* There are 2x snippets (files) in this repository for you:
    + ``./snippets/javascript.json``
    + ``./snippets/css.json``
    + Prepare to copy the __content__ of both snippets to the clipboard.
        - You can achive this by cloning this repository via git to some local folder, and then open the snippet files in your editor/IDE...
        - ...or, in GitHub, you can open the snippet files directly: Select the \<Code\> tab and click into the ``snippets`` folder, then click the respective snippet file and select the ``Raw`` button - now the raw content can easily be copied.
* Open Visual Studio Code
    + Open menu ``File/Preferences/User Snippets`` (de: ``Datei/Einstellungen/Benutzercodeausschnitte``)  you have three options now: 
        - Add to __Global__: Select ``New Global snippets file`` (de: ``Neue globale Codeausschnittsdatei``) then type or select ``javascript`` and ``css`` respectively.
        - Add to __User__: Just type or select ``javascript`` and ``css`` respectively.
        - Add to __Project__: Select ``New Snippets for '<your project folder>'`` then type or select ``javascript`` and ``css`` respectively.
    + A new editor tab appears ...
    + ... copy the content from the snippet files - one after the other - into the respective editor tabs.
    + Finally save the new files. *(Hint: Remember the path of the files before you close the editor tabs!)*

> I partially copied the german Visual Studio Code UI text (de:), because the german translation leads me to some confusion - I hope this will help others too ``;-)``

## Supplied Snippets

| Prefix | Descriptiony | Path |
| --- | --- | --- |
| cec | <b>c</b>ustom <b>e</b>lement <b>c</b>lass | ``./snippets/javascript.json`` |
| ces | <b>c</b>ustom <b>e</b>lement <b>s</b>tyle-sheet | ``./snippets/css.json`` |

The ideas for the both snippets are this:  
I like to separete css from js into different sourcecode files.

* So there is a snippet ``cec`` for the ``.js`` file, generating the custom element and it's class along with a html dummy-template.  
* The other snippet ``ces`` generates pseudo __css__ stuff, speciffic for custom elements and shadowDOM.


## Links

* Visual Studio Code
  + Visual Studio Code [Create your own snippet](https://code.visualstudio.com/docs/editor/userdefinedsnippets)
  + Visual Studio Code [Snippet Guide](https://code.visualstudio.com/api/language-extensions/snippet-guide)
  + Visual Studio Code [publishing extensions](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)
  + Visual Studio Code [vsce](https://github.com/microsoft/vscode-vsce) Visual Studio Code Extension Manager
  + Visual Studio Code [CLI](https://code.visualstudio.com/docs/editor/command-line)
* Other's extensions/snippets for webcomponents/custom-elements:
  + https://marketplace.visualstudio.com/items?itemName=bwielgosz.custom-elements-snippets
  + https://marketplace.visualstudio.com/items?itemName=LuceStudio.web-component-snippets, https://github.com/LuceStudio/vscode_web_component_snippets/blob/master/package.json
