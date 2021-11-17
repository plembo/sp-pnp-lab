# SharePoint PnP Starter Kit
https://github.com/pnp/sp-starter-kit

A "comprehensive solution designed for SharePoint Online and SHarePoint 2019 which provides numerous SharePoint Framework (SPFx) web parts, extensions, and other components, as well as PnP PowerShell driven provisioning..."

May build on Linux, but run on Windows to use tools like the SharePoint Framework Workbench.

To date, requires PnP PowerShell v1.7.0  (under PowerShell v7) and node.js v10. PS v5 on Windows will not work, neither will node.js beyond v10. Also requires gulp (```npm install -g gulp-cli```), yeoman (```npm install -g yo```) and SharePoint generator (```npm install @microsoft/generator-sharepoint```).

### Prerequisites
```pwsh
PS> Install-Module PnP.PowerShell -Scope CurrentUser
PS> npm install -g gulp-cli yo @microsoft/generator-sharepoint
```

### Install PnP Starter Kit
Clone the Starter Kit repo:

```pwsh
PS> git clone https://github.com/pnp/sp-starter-kit.git
```

Authorize script execution:

```pwsh
PS> Register-PnPManagementShellAccess
```

Then connect with:

```pwsh
PS> Connect-PnPOnline -Url https://[tenantname].sharepoint.com -Interactive
```
To install the whole Starter Kit in one go, cd to starter-kit/provisioning and run the following command:

```pwsh
PS> Invoke-PnPTenantTemplate -Path starterkit.pnp
```

To install only the SPFx components without the site designs, scripts or content:

https://github.com/pnp/sp-starter-kit/blob/master/provisioning/readme-spfx-only.md

```pwsh
PS> Invoke-PnPTenantTemplate -Path starterkit-spfx-only.pnp
```
