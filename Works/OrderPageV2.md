### Add:

- **removeSubscribeButton**

	1. actionMenuItems - коллекция наименований возможных действий при нажатии кнопки "Действия"
> Descriprion
Ищет совпадение в списке  с нужным элементом,который необходимо убрать из списка,если находит запоминает его индекс. И удаляет по данному индексу из коллекции.


### Fix:

- **getActions**

```javascript
	// | Вызов функции
	this.removeSubscribeButton(actionMenuItems);
```
