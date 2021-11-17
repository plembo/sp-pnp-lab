# SharePoint Framework Client-side Web Part Samples and Tutorials
https://github.com/pnp/sp-dev-fx-webparts

Big collection of web parts and tutorials for SharePoint Online.

Build with node.js v10 and npm v6.14.2, gulp, yeoman and SharePoint Framework Generator on Windows. Test with SharePoint Framework Workbench.

## Script editor web part for Modern pages
https://github.com/pnp/sp-dev-fx-webparts/tree/main/samples/react-script-editor

Built in React.

```pwsh
PS> npm install
```

Trust dev cert:

```pwsh
PS> gulp trust-dev-cert
```

Fire up the local web server:

```pwsh
PS> gulp serve --nobrowser
```
Check out in SPFx Workbench on tenant:

https://[tenantname].sharepoint.com/_layouts/workbench.aspx

Try and build solution:

```pwsh
PS> gulp bundle --ship
```

If you get a stdout error, check messages. In my case I had to update the browser db:

```pwsh
PS> npx browserslist@latest --update-db
```

Package the solution:

```pwsh
PS> gulp package-solution --ship
```

Look for sppkg under sharepoint/solution, ```pnp-script-editor.sppkg```.

Install in SharePoint app catalog and then to site.

