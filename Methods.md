| Имя метода | Описание | Пример |
| ------------- | ------------- | ------------- |
| moduleCardPrintFormsCollectionName | получаем коллекцию всех печатных форм | var printMenuItems = this.get(this.moduleCardPrintFormsCollectionName) |
|getActions | Возвращает коллекцию действий страницы редактирования | getActions: function() {
                // Вызывается родительская реализация метода для получения
                // коллекции проинициализированных действий базовой страницы.
                var actionMenuItems = this.callParent(arguments);
                // Добавление линии-разделителя.
                actionMenuItems.addItem(this.getActionsMenuItem({
                    Type: "Terrasoft.MenuSeparator",
                    Caption: ""
                }));
                // Добавление пункта меню [Назначить встречу] в список действий страницы редактирования.
                actionMenuItems.addItem(this.getActionsMenuItem({
                    // Привязка заголовка пункта меню к локализуемой строке схемы.
                    "Caption": { bindTo: "Resources.Strings.CallProcessCaption" },
                    // Привязка метода-обработчика действия.
                    "Tag": "callCustomProcess",
                    // Привязка свойства видимости пункта меню к значению, которое возвращает метод isAccountPrimaryContactSet().
                    "Visible": { bindTo: "isAccountPrimaryContactSet" }
                }));
                return actionMenuItems;
            }, |
