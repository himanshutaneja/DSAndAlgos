# DSAndAlgos

This repo contains Chrome Devtools Code Snippets exported in a JSON format.

In order to import the JSON formatted snippets into Chrome, open DevTools of DevTools (Ctrl + Shift + i) and execute below lines of code in console.

```javascript
let importSnippets = [ /* paste snippets here */ ];
InspectorFrontendHost.setPreference("scriptSnippets", JSON.stringify(importSnippets));
```

In order to export the snippets out of Chrome into a JSON format, open DevTools of DevTools (Ctrl + Shift + i) and execute below lines of code in console.

```javascript
let exportSnippets
InspectorFrontendHost.getPreferences(_ => { exportSnippets = JSON.parse(_.scriptSnippets) })

copy(exportSnippets)
```
