| Имя метода | Описание | Пример |
| ------------- | ------------- | ------------- |
| moduleCardPrintFormsCollectionName | получаем коллекцию всех печатных форм | var printMenuItems = this.get(this.moduleCardPrintFormsCollectionName) |
|getActions | Возвращает коллекцию действий страницы редактирования | getActions: function() {var actionMenuItems = this.callParent(arguments);};return actionMenuItems;} |
