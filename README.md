# wix_installer_issue_7925

Wix v4.0.3
This repo was created to simulate [https://github.com/wixtoolset/issues/issues/7925](https://github.com/wixtoolset/issues/issues/7925) issue of the wix.
Requirements: 
- VS 2022
- VS 2022 Extension `HeatWave for VS2022` v1.0.2

Error:
```
Severity	Code	Description	Project	File	Line	Suppression State	Details
Error	WIX0200	The Package element contains an unhandled extension element 'WixUI'. Please ensure that the extension for elements in the 'http://wixtoolset.org/schemas/v4/wxs/ui' namespace has been provided.	MyApp1	C:\dev\git-hub\wix_installer_issue_7925\wix_installer_issue_7925\Installers\MyApp1\Package.wxs	18		
```

# To successfully build MSI

In `Package.wxs` comment out those two lines: 
```
     <UIRef Id="WixUI_Common" />
    <ui:WixUI Id="MyUICommon" />
```

