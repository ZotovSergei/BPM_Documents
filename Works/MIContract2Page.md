### Add:

- **getRightsOnRoleAdmins**

	1. idCurrentUser - текущий пользователь
	2. idContactLaywer - поле 'Ответственный юрист КМИ'
	3. idCurrentOwner - поле 'Ответственный за договор'
	4. stageContract - стадия договора

### Fix:

**onEntityInitialized**

```javascript
	// | Ответственный за договор
	var currentOwner = this.get("Owner");
	var idCurrentOwner = currentOwner.value;

	// | Текущий пользователь
	var currentUserObject = Terrasoft.SysValue.CURRENT_USER;
	var idCurrentUser = currentUserObject.value;
	var nameCurrentUser = currentUserObject.displayValue;

	// | Объект Юрист в поле MIResponsibleLawyer - Ответственный юрист КМИ
	var currentLayer = this.get("MIResponsibleLawyer");
	var idCurrentLayer = null;
	if (currentLayer) idCurrentLayer = currentLayer.value;

	var stageContract = null;
	if (this.get("MIContractStages")) stageContract = this.get("MIContractStages").value;

	// | Регистрация
	var stageContractRegistration = "9ED8B243-AF54-4A66-BC05-9E74215B11C6".toLowerCase();

	// | Визирование
	var stagetContractVisa = "8EC5B047-E8CD-4F11-BC4F-17D1BAD42D7B".toLowerCase();

	// | Прикрепление скана с печатью
	var stagetContractScanWithPrint = "71C5555C-E65F-411A-B65D-9C99430B2401".toLowerCase();

	// | Заключен
	var stagetEnclosed = "EEE28F06-1872-4EC5-BDB4-95C3F849F226".toLowerCase();

	this.getRightsOnRoleAdmins(idCurrentUser, idCurrentLayer, idCurrentOwner, stageContract);
```
