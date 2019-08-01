### fix:

##### **attributes**: 
	...
```json
"MIValueTermsOfContract": {
"dataValueType": this.Terrasoft.DataValueType.BOOLEAN,
"value": false
},
"MITermsOfContractChecked": {
"dataValueType": this.Terrasoft.DataValueType.BOOLEAN,
},
"MITermsOfContractEnabled": {
"dataValueType": this.Terrasoft.DataValueType.BOOLEAN,
"value": false
},
"MIClientSpecificationFormTypicalChangedEnabled": {
"dataValueType": this.Terrasoft.DataValueType.BOOLEAN,
"value": false
},
"MIClientSpecificationFormTypicalChangedValue": {
"dataValueType": this.Terrasoft.DataValueType.BOOLEAN,
},
"MIValueEnabledActionWithContract": {
"dataValueType": this.Terrasoft.DataValueType.BOOLEAN,
"value": false
}
```
##### **diff**: 

```json
	{
		"operation": "insert",
		"name": "MICotractConditions1ec42647-acd8-43db-b1bf-e572d82d463e",
		...
			"click": {
				"bindTo": "actionWithContract"
			},
			"enabled": {
				"bindTo": "MITermsOfContractEnabled"
			}
		...
	},
```
```json
{
		"operation": "insert",
		"name": "MIClientSpecificationFormTypicalChangedf2b81b9e-89d8-4f7f-a867-c407f998421f",
		...
			"enabled": {
				"bindTo": "MIClientSpecificationFormTypicalChangedEnabled"
			}
		...
	},
```
```json
	{
		"operation": "insert",
		"name": "MITolerance12c661265-2e74-42b3-b034-567948b8bd17",
		...
			"enabled": "MIValueEnabledActionWithContract"
		},
		...
	},

	{
		"operation": "insert",
		"name": "MIPenaltyViolationOfPayment4c647051-22d9-4126-9d7f-90b4f4553394",
		...
			"enabled": "MIValueEnabledActionWithContract"
		},
		...
	},

		{
		"operation": "insert",
		"name": "MIStorageForServicesfb204ff7-8feb-4985-bc3c-3fdd3f130700",
		...
			"enabled": "MIValueEnabledActionWithContract"
		},
		...
	},
```
##### **methods**:
```javascript
*onEntityInitialized()* {
		...

var miStageLK = this.get("MIStageLK");
if (miStageLK.value == "acdd2ec8-574f-4c19-afa3-6a9b826043c4") this.set("MITermsOfContractEnabled", true);
if (this.get("MICotractConditions") == false) this.set("MIClientSpecificationFormTypicalChangedEnabled", true);
```
}



### Add: 
##### methods:

*specificationFilling*()

###### parameters: 
- contract - объект договор с выборочными полями.

------------

*showErrorMessage()*

###### parameters: 
- message - текст , который будет выводиться

------------

*actionWithContract()*

------------


