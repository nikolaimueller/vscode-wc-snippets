# vscode-wc-snippets

Webcomponent v1 (custom element) snippets for Visual Studio Code.

## Setup in VSCode

TODO: $$$

Copy the generated snippets folder to a new folder under your ``.vscode/extensions`` folder and restart VS Code.

## Supplied Snippets

| prefix | Descriptiony |
| --- | --- |
| cec | __c__ustom __e__lement __c__lass |
| ces | __c__ustom __e__lement __s__tyle-sheet |

The idea for the both snippets are this:
I like to separete css from js into different sourcecode files.

* So there is a snippet ``cec`` for the ``.js`` file, generating the custom element and it's class along with a html dummy-template.  
* The other snippet ``ces`` generates pseudo __css__ stuff, speciffic for custom elements and shadowDOM.


## Links

* Visual Studio Code
  + Visual Studio Code [Create your own snippet](https://code.visualstudio.com/docs/editor/userdefinedsnippets)
  + Visual Studio Code [Snippet Guide](https://code.visualstudio.com/api/language-extensions/snippet-guide)
* Other's extensions/snippets for webcomponents/custom-elements:
  + https://marketplace.visualstudio.com/items?itemName=bwielgosz.custom-elements-snippets