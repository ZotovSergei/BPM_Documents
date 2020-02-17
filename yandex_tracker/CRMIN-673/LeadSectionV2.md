##Add

###### methods:
```javascript
 callProccesMILeadClientComp: function() {
                console.log('MILeadClientComp start');
                var o = {
                    sysProcessName: "MILeadClientComp",
                    parameters: {
                    }
                }
                ProcessModuleUtilities.executeProcess(o);
            },
```
##Fix
```javascript
getSectionActions: function() {
                /*...other code*/
                actionMenuItems.addItem(this.getButtonMenuItem({
                    Caption: "Обработать базу КК",
                    Enabled: true,
                    Click: { bindTo: "callProccesMILeadClientComp" },
                    // Visible: { bindTo: "visibleMIDisqualifySuspensionLead" },
                    Visible: true,
                    // "Items": { "bindTo": "ButtonMenuItems" }
                }));
				/*...other code*/                
            },
```
