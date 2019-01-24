## Extensions
* [Auto Close Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)
* [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
* [Bracket Pair Colorizer](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer)
* [Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)
* [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
* [Git History](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory)
* [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
* [HTML Snippets](https://marketplace.visualstudio.com/items?itemName=wgenial.html-snippets)
* [npm](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script)
* [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
* [Service Portal Snippets](https://marketplace.visualstudio.com/items?itemName=stevengregory.service-portal-snippets)
* [TODO Highlights](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight)
* [vscode-icons](https://marketplace.visualstudio.com/items?itemName=robertohuertasm.vscode-icons)

# User Settings
```json
{
    "workbench.colorTheme": "Monokai",
    "window.zoomLevel": 0,
    "editor.fontSize": 14,
    "workbench.iconTheme": "vscode-icons",
    "editor.multiCursorModifier": "ctrlCmd",
    "editor.snippetSuggestions": "top",
    "gitlens.advanced.messages": {
        "suppressShowKeyBindingsNotice": true
    },
    "editor.minimap.enabled": false,
    "vsicons.dontShowNewVersionMessage": true,
    "prettier.singleQuote": true,
    "prettier.trailingComma": "es5"
}
```

# Javascript Code Snippets (ServiceNow focused)
```json
{
	"GlideRecord": {
		"prefix": "grwhile",
		"body": [
			"var gr = new GlideRecord('$1');",
			"gr.addQuery('$2', '$3');",
			"gr.query();",
			"while(gr.next()){",
			"\t$0",
			"}"
		],
		"description": "Glide Record WhileQuery using a single param"
	},
	"GlideRecordGet": {
		"prefix": "grget",
		"body": [
			"var gr = new GlideRecord('$1');",
			"if(gr.get('$2')){",
			"\t$0",
			"\tgr.setWorkflow(false);",
			"\tgr.autoSysFields(false);",
			"\tgr.update();",
			"}"
		],
		"description": "Glide Record Query using .get() method to retrieve one record by sys_id"
	},

	"GlideRecordEncodedQuery": {
		"prefix": "grenc",
		"body": [
			"var qstring = '$1';",
			"var gr = new GlideRecord('$2');",
			"gr.addEncodedQuery(qstring);",
			"gr.query();",
			"while(gr.next()){",
			"\t$0",
			"}"
		],
		"description": "Glide Record Query using .addEncodedQuery() method"
	},

	"GlideRecordGetParams": {
		"prefix": "grget2",
		"body": [
			"var gr = new GlideRecord('$1');",
			"if(gr.get('$2', '$3')){",
			"\t$0",
			"}"
		],
		"description": "Glide Record Query using .get() method to retrieve one record by one param"
	},

	"GlideSysChoice": {
		"prefix": "syschoice",
		"body": [
			"// Param1: table, Param2: field",
			"var choiceList = new GlideSysChoice('$1', '$2');",
			"var gr = choiceList.getChoices();",
			"while (gr.next()) {",
  			"\tgs.print(gr.value + ' \t ' + gr.label);",
			"}"
		],
		"description": "Glide Record Query using .get() method to retrieve one record by one param"
	},

	"iife": {
		"prefix": "iife",
		"body": [
			"(function(){",
			"\t$0",
			"})();"
		],
		"description": "Immediately Invoked Function Expression",
	},

	"setValue": {
		"prefix": "setValue",
		"body": [
			"gr.setValue('$1', $2);"
		],
		"description": "object method to setValue",
	}
}

```
