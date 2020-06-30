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
* Open Visual Studio Code, repeat the following steps for each snippet:
    + Open menu ``File/Preferences/User Snippets`` (de: ``Datei/Einstellungen/Benutzercodeausschnitte``)  you have three options now: 
        - Add to __Global__: Select ``New Global snippets file`` (de: ``Neue globale Codeausschnittsdatei``) then type or select ``javascript`` or ``css`` respectively.
        - Add to __User__: Just type or select ``javascript`` or ``css`` respectively.
        - Add to __Project__: Select ``New Snippets for '<your project folder>'`` then type or select ``javascript`` or ``css`` respectively.
    + A new editor tab appears for each snippet file ...
    + ... copy the content from the snippet file, from this git repository, into the respective new editor tab.
    + Finally save the new file. *(Hint: Remember the path of the file before you close the editor tabs!)*

> I partially copied the german Visual Studio Code UI text (de:), because the german translation leads me to some confusion - I hope this will help others too ``;-)``

## Supplied Snippets

| Prefix | Descriptiony | Path |
| ---  | --- | --- |
| cec  | <b>c</b>ustom <b>e</b>lement <b>c</b>lass | ``./snippets/javascript.json`` |
| ces  | <b>c</b>ustom <b>e</b>lement <b>s</b>tyle-sheet | ``./snippets/css.json`` |
| ceci | <b>c</b>ustom <b>e</b>lement <b>c</b>lass <b>i</b>nline | ``./snippets/javascript.json`` |

1.) The ideas for the snippets __`cec`__ and __`ces`__ are this:  
I like to separete css from js into different sourcecode files.

* So there is a snippet ``cec`` for the ``.js`` file, generating the custom element and it's class along with a html-template and some dummy-content.  
* The other snippet ``ces`` generates pseudo __css__ stuff, speciffic for custom elements and shadowDOM.
* The generated class contains code to load the CSS file automatically.

2.) The snippet __`ceci`__ is applicable for a __monolithic HTML__ file, where all components are kept inline in one `<script>` block. In this case the __css file__ (mentioned above) becomes obsolete, thus styles are 'relocated' into the template string of the component.  
Following the "monolithic" approach, one can build a HTML file, which can be started directly from the filesystem into the browser - without the need for a web-server.

> For good reasons, modern browsers deny do load further (css, js, ...) files if you loaded the origin HTML file from the filesystem directly (see: [Same-origin policy](https://developer.mozilla.org/de/docs/Web/Security/Same-origin_policy)).

## Usage Example

*Hint: Web components are a combination of web technologies - most of all `custom elements` and a `javascript class` which implements the custom element and turns it into a component. I use the words component, web component and custom element as synonymes here.*

__Play the example__

* Prerequisite: Install the snippets - follow the installation at [Setup in VSCode](#Setup-in-VSCode)
* Clone this git repository to some local folder on your machine:  
`git clone https://github.com/nikolaimueller/vscode-wc-snippets.git`
* Navigate into the new folder:  
`cd vscode-wc-snippets`
* Open Visual Studio Code in the new folder: `code . &`  *(that command works on Windows as well as on Linux! The `.` means: 'open in current working directory' and `&` executes the process (code) independently/parellel from the command shell.)*
* Now you need a "ad hock" webserver - *ps: I like [LiveServer](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)* - and start browsing the file `DemoComponent.html`.
* Open your browsers development tools and look into the console - you will see that, at this moment, there is no `DummyComponent.js` file.
* In Visual Studio Code create a new file named `DemoComponent.js` - the new file opens in an new editor.
* In the new editor type `cec` (snippet prefix) and press `Enter` - a lot of sorce code will be apear in the editor...
* ...the cursor is placed "some where" inside that new code, just type the __tag name__ of your new custom element - for example `demo-component` - safe it, now the content of the new web component should be visible in the browser.
* __Congratulations - that's your new `DemoComponent` implementation!__
* But wait a moment, we are not ready - we need some `CSS` for the new component - create another file `DemoComponent.css` and in the new editor type `ces`, then hit `Enter` key and safe the file.
* __Bingo! Your component has a red border now - well done!__

__Some ideas about naming conventions:__

* It's common, best practice for long time now, to name the source code file which contains classes like the class name they contain. And class names allways starts with a upper-case letter (ie.: class `DomeComponent` --> `DomeComponent.js`).
* At least my component implementations need more than one file - as a result I create a subfolder for each component and put my `'*.js'`, `'*.css'`, `'*.md'`, etc. into that subfolder. And I like to repeat the class name of the component for the folder name too (a good alternative could be the component's tag name).
* Syntactivally browsers demand to name custom elements all lower-case with at least one dash somewhere in the middle of the tag name.
    + It's a good idea to let the custom element's name follow the class name, like so: &lt;`demo-component`&gt; ... `DemoComponent`
    + For 3rd party components it's reasonable to start the name with a short prefix, a shorthand for the component library (ie.: `my-route-view` ... `MyRouteView`)
    + while components local to the project could have a name ending with postfixed `Component` - like so: ``md-viewer-component`` ... ``MdViewerComponent``
    + My habbit is to have a `components` subfolder below the project root-folder, and put all components for the actual project there.

*These are just some ideas for naming and structuring source code - the details are not so important, but __having__ some __coding convention__ and to __follow it__ - that __is important!__*

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
