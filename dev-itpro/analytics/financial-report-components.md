---
title: "Компоненты финансового отчета"
description: "В этой статье описано, как компоненты или строительные блоки определений отчетов используются в финансовой отчетности. Эти строительные блоки включают определения строк, определения столбцов и определения дерева отчетов. В статье объясняется, как организовать и заблокировать строительные блоки и как работать с группами строительных блоков."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 18 - 54 - 02
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: a423dff4d8796f454c9c4db03c8ceb2b8c3d6456
ms.lasthandoff: 03/30/2017


---

# <a name="financial-report-components"></a>Компоненты финансового отчета

В этой статье описано, как компоненты или строительные блоки определений отчетов используются в финансовой отчетности. Эти строительные блоки включают определения строк, определения столбцов и определения дерева отчетов. В статье объясняется, как организовать и заблокировать строительные блоки и как работать с группами строительных блоков. 

Суть конструктора финансовых отчетов заключается в том, чтобы разбить информацию на самые маленькие компоненты или строительные блоки, а затем объединить необходимые компоненты согласно требованиям. Таким образом, форматирование отчета отделено от финансовых данных, и можно изменить дизайн отчета без изменения финансовых данных в системе Microsoft Dynamics ERP. За счет использования этого подхода со строительными блоками вы можете комбинировать текст, суммы и расчеты для того, чтобы создать необходимые отчеты. Кроме того, эта гибкость поддерживает креативность, позволяя легко просмотреть операции различными способами. Индивидуальные строительные блоки определения отчета подобны трехмерной электронной таблице, но более мощные. Определение отчета указывает определение строки, определение столбца и необязательное определение дерева отчетности, которые должны использоваться для отчета. Оно также включает информацию о том, где хранить созданный отчет и как его форматировать. Для лучшего многократного и общего использования вы можете создать группу строительных блоков, которая является коллекцией существующих определений отчетов, определений строк, определений столбцов, определений дерева отчетности и наборов аналитик, которые связаны с компанией.

## <a name="building-blocks-of-a-report"></a>Строительные блоки отчета
| Строительный блок            | Описание                                                                                                                                                                                                                                                                              | Дополнительные сведения                                                                                                 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Определение строки            | Определение строки указывает описательные строки (например, зарплаты или продажи) в отчете. Оно также перечисляет значения или аналитики сегмента, которые содержат значения для каждой номенклатуры строки, и включает форматирование строк и расчеты.                                                    | [Определения строк](row-definitions-financial-reporting.md)                       |
| Определение столбца         | Определение столбца указывает период для использования при извлечении данных из финансовых аналитик. Оно также включает форматирование столбца и вычисления.                                                                                                                                 | [Определения столбца](column-definitions-financial-reports.md)         |
| Определение дерева отчетности | Определение дерева отчетности напоминает организационную диаграмму. Оно содержит индивидуальные единицы отчетности, которые представляют каждое поле в диаграмме. Единицы могут быть или индивидуальными подразделениями из финансовых данных или единицами более высокого уровня, которые суммируют данные от других единиц отчетности. | [Определения дерева отчетности](financial-reporting-tree-definitions.md) |
| Определение отчета         | Определение отчета использует определение строки, определение столбца, и Необязательное определение дерева отчетности для построения отчета. Оно также обеспечивает дополнительные параметры и настройки, которые можно использовать для настройки отчета.                                                                    | [Определение отчета](design-financial-report-definitions.md)                  |

Если вы ранее не создавали отчеты, то полезно использовать мастер отчета, чтобы быстро создать определение отчета, которое можно настроить позже. Если вы имеете опыт создания отчетов и хотите больше гибкости для дизайна отчета, вы можете объединить новые или существующие строительные блоки, чтобы создать новое определение отчета. Нет необходимости полностью понимать все доступные варианты определения отчета для того, чтобы создавать качественные отчеты. По мере того как вы ознакомляете с конструированием отчетов, вы можете расширить ваши определения отчета для того, чтобы пользоваться более продвинутыми функциями. После того как вы создали основной отчет, вы можете настроить определение отчета и любые строительные блоки в определении отчета.

## <a name="organize-the-building-blocks"></a>Организуйте строительные блоки
Используйте папки для того, чтобы организовать ваши строительные блоки в конструкторе отчетов. Все папки относятся к типу строительного блока, который они содержат. Например, все папки которые содержат определения строк, расположены в области **Определения строк** конструктора отчета.

### <a name="create-a-folder"></a>Создание папки

1.  В конструкторе отчета, выберите тип строительного блока, который организовать в Области перехода. Например, чтобы сортировать определение строки, щелкните **Определения строк**.
2.  В области перехода выберите существующую папку, в которой будет создана новая папка, и выполните одно из следующих действий:
    -   Щелкните правой кнопкой мыши родительскую папку и выберите пункт **Новая папка**.
    -   Выберите родительскую папку, щелкните **Файл** и выберите **Новая папка**.

3.  После отображения новой папки введите имя новой папки и нажмите клавишу "Ввод".

## <a name="lock-a-building-block"></a>Блокировка строительного блока
Вы можете создать пароль, чтобы заблокировать и защитить строительный блок. Таким образом вы можете добавить уровень безопасности к компоненту отчета без дополнительной защиты для всей системы. Пароль может помочь защитить данные строительного блока, которые важны вашему процессу отчетности в конце месяца. Пользователь с любой ролью может заблокировать строительный блок. Однако другие пользователи всегда имеют доступ только для чтения к заблокированному компоненту. Пользователи могут открыть, изменить и сохранить заблокированный компонент под новым именем. Пользователь с ролью администратора всегда может получить доступ и изменить заблокированный строительный блок.
1.  В конструкторе отчета откройте компонент отчета для блокировки, например определение строки, определение столбца, определение отчета или определение дерева отчетности.
2.  В меню **Сервис** щелкните **Защитить/снять защиту**. Вы также можете щелкнуть **Защитить/снять защиту** (значок замка) на панели инструментов.
3.  В диалоговом окне **Проект** введите и подтвердите пароль, затем нажмите кнопку **OK**. Значок замка на панели инструментов выделен, если открытый строительный блок заблокирован.

Чтобы разблокировать заблокированный строительный блок, откройте строительный блок и щелкните **Защитить/снять защиту** на панели инструментов. Либо в меню **Сервис** щелкните **Снять защиту**.

## <a name="building-block-groups"></a>Группы строительных блоков

Строительные блоки — определения строки, определения столбца, определения дерева отчетности и определения отчета, которые вы создаете для отчета. Группы строительного блока — собрания определений и наборов аналитик, которые связаны с компанией. Группы строительных блоков могут быть характерны для компании, либо несколько компаний могут совместно пользоваться одним набором строительных блоков. Если некоторые компании имеют различный план счетов, вы можете использовать отдельную группу строительных блоков для каждой компании. Либо вы можете присвоить имя всем отдельным строительным блокам, чтобы показать, с какой компанией они совместимы.
### <a name="create-a-building-block-group"></a>Создание группы строительных блоков

1.  В конструкторе отчетов в меню **Компания** щелкните **Группы строительных блоков**.
2.  В диалоговом окне **Группы строительных блоков** щелкните **Создать**.
3.  Введите уникальное имя и описание для группы строительных блоков. Каждое поле может содержать не более 256 символов (с учетом пробелов).
4.  Щелкните **OK**, чтобы создать новую группу строительных блоков.

### <a name="assign-a-building-block-group"></a>Назначение группы строительных блоков

После создания группы блоков необходимо назначить ее хотя бы одной компании. Затем можно создать определения отчета, строки, столбца и дерева отчетности и сохранить их в группе строительных блоков. Вы должны закрыть все строительные блоки, прежде чем начинать следующую процедуру.
1.  В конструкторе отчетов, в меню **Компания**, щелкните **Компании**.
2.  В диалоговом окне **Компании** выберите компанию, которой требуется назначить группу строительных блоков.
3.  Щелкните **Изменить**.
4.  В диалоговом окне **Изменить компанию** в поле **Группа строительных блоков** выберите группу строительных блоков, которую задать компании, или щелкните **Создать** для того, чтобы создать новую группу строительного блока.
5.  Щелкните **ОК** для того, чтобы назначить группу строительных блоков.
6.  Нажмите кнопку **Закрыть**, чтобы закрыть диалоговое окно **Компании**. Группа строительного блока, которую вы выбрали теперь назначена к компании. Теперь все новые определения строк, определения столбцов и т. д. будут частью группы строительных блоков, назначенной этой компании. Вы можете также импортировать файл .TDBX или отчет из другой системы.

### <a name="view-a-building-block-group"></a>Просмотр группы строительных блоков

После создания группы строительных блоков можно использовать ее для просмотра всех строительных блоков, которые ей назначены. Также можно экспортировать или импортировать группу строительных блоков и выполнить дополнительное обслуживание групп строительных блоков.
1.  В конструкторе отчетов, в меню **Компания**, щелкните **Группы строительного блока**.
2.  В диалоговом окне **Группы строительного блока**, выберите строительный блок, который осмотреть.
3.  Щелкните **Просмотр**, чтобы открыть диалоговое окно **Просмотр группы строительных блоков** и просмотреть содержимое группы строительных блоков.
4.  Нажмите кнопку **Закрыть**, чтобы закрыть диалоговые окна.

### <a name="save-a-building-block-group-under-a-new-name"></a>Сохранение группы строительных блоков под новым именем

Вы можете сохранить существующую группу строительных блоков под новым именем. После этого вы можете изменить новую группу строительных блоков, не изменяя исходную группу строительных блоков.
1.  В конструкторе отчетов, в меню **Компания**, щелкните **Группы строительного блока**.
2.  В диалоговом окне **Группы строительных блоков** выберите группу строительных блоков для сохранения под новым именем.
3.  Нажмите кнопку **Сохранить как**.
4.  Введите новое имя и описание для группы строительных блоков.
5.  Нажмите кнопку **OК**. Новая группа строительных блоков появляется в диалоговом окне **Группы строительного блока**.

### <a name="export-a-building-block-group"></a>Экспорт группы строительных блоков

Можно экспортировать группу строительных блоков или определенные строительные блоки отчета в группу строительных блоков. Экспортированную группу строительных блоков можно использовать в качестве резервной копии. Можно также копировать экспортированные данные между группами строительных блоков или установками Dynamics 365 for Operations. Конструктор отчетов включает ссылочные стили шрифтов и наборы аналитик вместе с группой строительных блоков.
1.  В конструкторе отчетов, в меню **Компания**, щелкните **Группы строительного блока**.
2.  В диалоговом окне **Группы строительного блока** выберите группу строительного блока для экспорта и щелкните **Экспорт**.
3.  В диалоговом окне **Экспорт** выберите определения отчетов для экспорта:
    -   Для того, чтобы экспортировать все ваши определения отчета и связанные строительные блоки, щелкните **Выбрать все**.
    -   Чтобы экспортировать определенные отчеты, строки, столбцы, деревья или наборы аналитик, щелкните соответствующую вкладку и выберите элементы для экспорта. Нажмите и удерживайте клавишу CTRL, чтобы выбрать несколько элементов на вкладке. **Примечание.** При выборе отчетов для экспорта выбираются связанные строки, столбцы, деревья и наборы аналитик.

4.  По завершении выбора элементов для экспорта щелкните **Экспорт**.
5.  В диалоговом окне **Сохранить как** выберите расположение, в которую экспортировать группу строительного блока.
6.  В поле **Имя файла** введите имя файла. Конструктор отчетов автоматически добавляет расширение имени файла TDBX.
7.  Нажмите кнопку **Сохранить**. Группа строительных блоков сохраняется в указанном расположении.

### <a name="import-a-building-block-group"></a>Импорт группы строительных блоков

Можно импортировать группу строительных блоков в существующую группу строительных блоков или создать новую группу строительных блоков для данных. Все импортированные группы строительных блоков сохраняют исходные стили шрифтов и ссылки на компании и включают соответствующие наборы аналитик.
1.  В конструкторе отчетов, в меню **Компания**, щелкните **Группы строительного блока**.
2.  В диалоговом окне **Группы строительного блока** выберите группу строительного блока, в которую импортировать группу строительных блоков и щелкните **Импорт**.
3.  В диалоговом окне **Открыть** выберите группу строительного блока для импорта и щелкните **Открыть**.
4.  В диалоговом окне **Импорт** выберите определения отчетов для импорта:
    -   Чтобы импортировать все определения отчетов и поддерживающие строительные блоки, щелкните **Выбрать все**.
    -   Для того, чтобы импортировать специфические отчеты, строки, столбцы, деревья, или Наборы аналитик, выбирают отчеты, строки, столбцы, деревья, или Наборы аналитик, которые импортировать.

5.  По завершении выбора элементов для импорта щелкните **Импорт**.

### <a name="undo-a-checkout-of-a-building-block"></a>Отмените извлечение строительного блока

При открытии строительного блока другие пользователи имеют доступ только для чтения к этому строительному блоку. Иногда пользователи забывают закрыть строительный блок или завершают работу системы, не закрыв строительный блок. В результате строительный блок остается извлеченным и другие пользователи не могут открыть его. В таких ситуациях администратор финансовой отчетности может использовать диалоговое окно **Извлеченные элементы**, чтобы вернуть строительные блоки, которые пользователи оставили в извлеченном состоянии. **Примечание.** Вы должны иметь роль администратора, чтобы вернуть строительные блоки с помощью диалогового окна **Извлеченные элементы**.
1.  В конструкторе отчета, в меню **Инструменты**, щелкните **Извлеченные элементы**.
2.  В диалоговом окне **Извлеченные элементы** выберите **Показать детали от всех пользователей**. Список обновлен для показа всех строительных блоков, которые извлечены, и пользователей, которые их извлекли.
3.  Выберите строительный блок, и после этого щелкните **Отменить извлечение**.
4.  Щелкните **Да**, чтобы вернуть строительный блок.

# <a name="see-also"></a>См. также

[Финансовая отчетность в Microsoft Dynamics ERP](financial-reporting-intro.md)

