---
title: "Места назначения электронной отчетности"
description: "Можно настроить назначение для каждой конфигурации формата электронной отчетности и ее выходного компонента (папка или файл). Пользователи, имеющие соответствующие права доступа, также могут изменять настройки назначения во время выполнения. В этой статье описывается управления местом назначения электронной отчетности, поддерживаемые типы мест назначения и вопросы безопасности."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: fb2aeee1f38823e7ea96071f773e8448d65ba8ff
ms.contentlocale: ru-ru
ms.lasthandoff: 06/13/2017

---

# <a name="electronic-reporting-destinations"></a>Места назначения электронной отчетности

[!include[banner](../includes/banner.md)]


Можно настроить назначение для каждой конфигурации формата электронной отчетности и ее выходного компонента (папка или файл). Пользователи, имеющие соответствующие права доступа, также могут изменять настройки назначения во время выполнения. В этой статье описывается управления местом назначения электронной отчетности, поддерживаемые типы мест назначения и вопросы безопасности.

Конфигурации формата электронной отчетности обычно содержат по крайней мере один выходной компонент: файл. Как правило, конфигурации содержат несколько выходных компонентов файлов различных типов (например, XML, TXT или XLSX), сгруппированных в одну или несколько папок. Управление местом назначения электронной отчетности позволяет предварительно настроить поведение при выполнении каждого компонента. По умолчанию при запуске конфигурации отображается диалоговое окно, которое позволяет пользователю сохранить или открыть файл. То же поведение также используется, если вы импортируете конфигурацию электронной отчетности и не настраиваете какое-либо конкретное место назначения для нее. После создания места назначения для основного выходного компонента это место назначения переопределяет поведение по умолчанию, и папка или файл отправляется согласно настройкам места назначения.

## <a name="availability-and-general-prerequisites"></a>Доступность и общие предварительные условия
Функциональные возможности мест назначений электронной отчетности недоступны в выпуске Microsoft Dynamics AX 7.0 (февраль 2016 г.). Поэтому необходимо установить Microsoft Dynamics 365 for Operations 1611 (выпуск за ноябрь 2016 г.), чтобы использовать все функции, которые описаны в этом разделе. Можно также установить один из следующих компонентов. Однако имейте в виду, что эти альтернативные варианты обеспечивают более ограниченные возможности мест назначения электронной отчетности.

-   Версия приложения Microsoft Dynamics AX 7.0.1 (май 2016 г.)
-   [Исправление приложения](https://fix.lcs.dynamics.com/issue/results/?q=3160213) управления местом назначения электронной отчетности

Места назначения можно настроить только для конфигураций электронной отчетности, которые были импортированы, и для форматов, доступных на странице **Конфигурации электронной отчетности**.

## <a name="overview"></a>Обзор
Функциональные возможности управления местом назначения электронной отчетности доступны в разделе **Управление организацией** &gt; **Электронная отчетность**. Здесь можно переопределить поведение по умолчанию для конфигурации. Импортированные конфигурации не отображаются на этой странице, если не щелкнуть **Создать**, а затем в поле **Ссылка** не выбрать конфигурацию, для которой создаются параметры места назначения.

[![Выбор конфигурации в поле "Ссылка"](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

После создания ссылки можно создать место назначения файл для каждой папки или файла. 

[![Создание файла места назначения](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Примечание.** Можно создать одно место назначения файла для каждого выходного компонента одинакового формата, например папка или файл, выбранный в поле **Имя файла**. После этого можно включить и отключить отдельные места назначения для места назначения файла в диалоговом окне **Параметры места назначения**. Кнопка **Параметры** используется для управления всеми местами назначения для выбранного места назначения файла. В диалоговом окне **Параметры места назначения** можно управлять каждым местом назначения отдельно, выбрав для него параметр **Включено**.

[![Диалоговое окно "Параметры места назначения"](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Типы мест назначений
Поддерживаются различные типы мест назначения. Можно включить или отключить все типы одновременно. Таким образом можно либо не предпринимать никаких действий, либо отправить компонент во все настроенные места назначения. В следующих разделах описываются поддерживаемые места назначения.

### <a name="email-destination"></a>Место назначения электронной почты

Задайте для параметра **Включено** значение **Да**, чтобы отправить выходной файл по электронной почте. После включения этого параметра вы можете указать получателей сообщения электронной почты, и также изменить тему и текст сообщения электронной почты. Можно настроить постоянные тексты для темы и текста сообщения электронной почты или можно использовать формулы электронной отчетности для динамического создания текстов сообщений электронной почты. Адреса электронной почты для электронной отчетности можно настроить двумя способами. Конфигурация может быть выполнена таким же образом, как она выполняется для функции управления печатью в Finance and Operations. Адрес электронной почты можно также разрешить адрес электронной почты, используя прямую ссылку на конфигурацию электронной отчетности через формулы.

### <a name="email-address-types"></a>Типы адреса электронной почты

При нажатии кнопки **Изменить** для поля **Кому** или **Cc** открывается диалоговое окно **Кому**. Затем можно выбрать тип адреса электронной почты для использования.

[![Диалоговое окно "Кому"](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Управление печатью

При выборе типа **Эл. почта управления печатью** можно ввести фиксированные адреса электронной почты в поле **Кому**. Чтобы использовать нефиксированные адреса электронной почты, необходимо выбрать тип источника электронной почты для места назначения файла. Поддерживаются следующие значения: **Клиент**, **Поставщик**, **Перспективный клиент**, **Контакт**, **Конкурент**, **Работник**, **Кандидат**, **Потенциальный поставщик** и **Неодобренный поставщик**. После выбора типа источника электронной почты нажмите кнопку рядом с полем **Исходная учетная запись эл. почты**, чтобы открыть форму **Конструктор формул**. Эту форму можно использовать для присоединения формулы, которая представляют учетную запись выбранного субъекта в месте назначения электронной почты.

[![Настройка типа электронной почты управления печатью](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Обратите внимание, что формулы зависят от конфигурации электронной отчетности. В поле **Формула** введите характерную для конкретного документа ссылку на тип субъекта клиента или поставщика. Вместо печати можно найти узел источника данных, который представляет счет клиента или поставщика, и нажать кнопку **Добавить источник данных**, чтобы обновить формулу. Пример, при использовании конфигурации перемещения кредита ISO 20022 узел, представляющий счет поставщика, — **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. В противном случае введите любое значение строки, например **DE-001**, чтобы сохранить формулу.

[![Конструктор формул](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

В диалоговом окне **Кому** щелкните корзину рядом с полем **Исходная учетная запись эл. почты**, чтобы необратимо удалить формулу из исходной учетной записи электронной почты. Можно также открыть конструктор формул, чтобы изменить ранее сохраненную формулу. Чтобы назначить адреса электронной почты, нажмите кнопку **Изменить** для открытия диалогового окна **Назначить адреса электронной почты**.

[![Назначение адресов электронной почты для места назначения электронной почты](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Конфигурационное сообщение эл. почты

Используйте этот тип электронной почты, если конфигурация, которую вы используйте, имеет узел в источниках данных, который представляет адрес электронной почты. Можно использовать источники данных и функции в конструкторе формул, чтобы получить адрес электронной почты в правильном формате.

[![Назначение источника данных адресов электронной почты для места назначения электронной почты](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Примечание.** SMTP-сервер должен быть настроен и доступен. В Finance and Operations SMTP-сервер можно указать в разделе **Администрирование системы** &gt; **Настройка** &gt; **Электронная почта** &gt; **Параметры электронной почты**.

### <a name="archive-destination"></a>Место назначения архива

Этот параметр можно использовать для отправки выходных данных в папку Microsoft SharePoint или хранилище Microsoft Azure. Задайте для параметра **Включено** значение **Да** для отправки выходных данных в место назначения, которое определяется выбранным типом документа. Для выбора доступны только типы, в которых для группы задано значение **Файл**. Типы документов определяются в разделе **Управление организацией** &gt; **Управление документами** &gt; **Типы документов**. Конфигурация для мест назначения электронной отчетности аналогична конфигурации системы управления документами.

[![Страница типов документов](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Расположение определяет, где сохранен файл. После включения места назначения **Архив** результаты выполнения настройки можно сохранить в архиве заданий. Можно просмотреть результаты в пункте **Управление организацией** &gt; **Электронная отчетность** &gt; **Архивированные задания электронной отчетности**. **Примечание.** Можно выбрать тип документа для архива заданий в Finance and Operations, в пункте **Управление организацией** &gt; **Рабочие области** &gt; **Электронная отчетность** &gt; **Параметры электронной отчетности**.

#### <a name="sharepoint"></a>SharePoint

Можно сохранить файл в указанной папке SharePoint. Определить сервер SharePoint по умолчанию можно в разделе **Управление организацией** &gt; **Управление документами** &gt; **Параметры управления документами** на вкладке **SharePoint**. После настройки папки SharePoint ее можно выбрать как папку для сохранения выходных данных электронной отчетности для этого типа документов. 

[![Выбор папки SharePoint](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Хранилище Azure

Если в качестве расположения типа документа указан **Каталог архива**, можно сохранить файл в хранилище Azure.

### <a name="file-destination"></a>Место назначения файла

Если для параметра **Включено** задано значение **Да**, после завершения выполнения конфигурации появляется диалоговое окно открытия или сохранения.

### <a name="screen-destination"></a>Место назначения экрана

Если для параметра **Включено** задано значение **Да**, создается предварительный просмотр выходных данных. Некоторые типы файлов, такие как XML, TXT и PDF, можно просматривать непосредственно в окне браузера. Для других типов файлов, таких как Microsoft Excel или Word, используется служба Microsoft Office Online.

### <a name="power-bi-destination"></a>Место назначения Power BI

Задайте для параметра **Включено** значение **Да** для использования конфигурации электронной отчетности (ER), чтобы настроить перенос данных из вашего экземпляра Finance and Operations в службы Microsoft Power BI. Перенесенные файлы хранятся на экземпляре сервера Microsoft SharePoint Server, который должен быть настроен для этой цели. Дополнительные сведения см. в разделе [Использование конфигурации электронной отчетности для передачи данных из Finance and Operations в Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Совет.** Чтобы переопределить поведение по умолчанию (то есть диалоговое окно конфигурации), можно создать ссылку на место назначения и место назначения файла для основного выходного компонента, а затем отключить все места назначения.

## <a name="security-considerations"></a>Вопросы безопасности
Для мест назначения электронной отчетности используется два типа привилегий. Один тип управляет возможностью ведения всех мест назначения, настроенных для юридического лица (то есть, управляет доступом к странице **Места назначения электронной отчетности**). Второй тип управляет доступной для пользователей приложения возможностью переопределить параметры мест назначения, настроенные разработчиком или консультантом по функциональным возможностям электронной отчетности, во время выполнения.

| Роль (имя AOT)                     | Имя роли                                  | Полномочие (имя в AOT)                     | Название полномочия                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Разработчик электронной отчетности             | ERFormatDestinationConfigure        | Настройка места назначения форматов электронной отчетности                |
| ERFunctionalConsultant              | Консультант по функциональным возможностям электронной отчетности | ERFormatDestinationConfigure        | Настройка места назначения форматов электронной отчетности                |
| PaymAccountsPayablePaymentsClerk    | Сотрудник, обрабатывающий платежи по расчетам с поставщиками            | ERFormatDestinationRuntimeConfigure | Настройка места назначения форматов электронной отчетности во время выполнения |
| PaymAccountsReceivablePaymentsClerk | Сотрудник, обрабатывающий платежи по расчетам с клиентами         | ERFormatDestinationRuntimeConfigure | Настройка места назначения форматов электронной отчетности во время выполнения |

**Примечание.** В указанных выше полномочиях используется две привилегии. Эти привилегии имеют те же имена, что и соответствующие полномочия: **ERFormatDestinationConfigure** и **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Часто задаваемые вопросы
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Импортированные конфигурации электронной отчетности отображаются на странице "Конфигурации электронной отчетности". Но почему они не отображаются на странице "Места назначения электронной отчетности"?

Убедитесь, что вы нажали кнопку **Создать** и затем выбрали конфигурацию в поле **Ссылка**. На странице **Места назначения электронной отчетности** можно просмотреть только те конфигурации, для которых настроены места назначения.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Можно ли определить используемую учетную запись хранилища Azure и хранилище BLOB-объектов Azure?

№ п/п Используется хранилище BLOB-объектов Azure по умолчанию, которое определяется и используется для системы управления документами.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Для чего нужно место назначения "Файл" в параметрах места назначения? Для чего нужен этот параметр?

Место назначения **Файл** используется для управления диалоговым окном. Если это место назначения включено или если место назначения не определено для конфигурации, отобразится диалоговое окно открытия или сохранения после создания выходного файла.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Можете ли вы привести пример формулы, которая ссылается на счет поставщика, на который можно отправить сообщение электронной почты?

Формула зависит от конфигурации электронной отчетности. Например, при использовании конфигурации перемещения кредита ISO 20022 можно использовать **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** или **model.Payments.Creditor.Identification.SourceID** для получения связанного счета поставщика.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Одна из моих конфигураций формата содержит несколько файлов, сгруппированных в одну папку (например, папка Folder1 содержит файлы File1, File2 и File3). Как настроить места назначения, чтобы архив Folder1.zip не создавался вообще, File1 отправлялся по электронной почте, File2 отправлялся в SharePoint и File3 можно было открыть сразу же после выполнения конфигурации?

Обязательным условием является то, что ваш формат должен быть доступен в конфигурациях электронной отчетности. Если у вас есть формат, откройте страницу **Место назначения электронной отчетности** и создайте новую ссылку на данную конфигурацию. Затем необходимо наличие четырех мест назначения файлов, по одному для каждого выходного компонента. Создайте первое место назначения файла, присвойте ему имя, например **Папка** и выберите имя файла, которое представляет папку в конфигурации. Затем щелкните **Параметры** и убедитесь, что все места назначения отключены. Для этого места назначения файла папка создаваться не будет. По умолчанию из-за иерархических зависимостей между файлами и родительскими папками файлы будут вести себя таким же образом. Другими словами, они не будут никуда отправляться. Чтобы переопределить это поведение по умолчанию, необходимо создать три дополнительных места назначения файлов, по одному для каждого файла. В параметрах места назначения для каждого файла необходимо включить место назначения, в которое нужно отправить файл.

# <a name="see-also"></a>См. также

[Обзор электронной отчетности](general-electronic-reporting.md)



