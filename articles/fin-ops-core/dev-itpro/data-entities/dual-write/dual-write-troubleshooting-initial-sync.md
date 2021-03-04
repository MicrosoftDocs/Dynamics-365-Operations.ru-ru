---
title: Устранение неполадок при начальной синхронизации
description: В этом разделе содержатся сведения об устранении неполадок, которые могут возникнуть при начальной синхронизации.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a7ba4fa4771324b4bcb8464649bd8ce8f32024c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683576"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Устранение неполадок при начальной синхронизации

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Dataverse. А именно, содержатся сведения об устранении неполадок, которые могут возникнуть при начальной синхронизации.

> [!IMPORTANT]
> Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD). В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Проверка наличия ошибок исходной синхронизации в приложении Finance and Operations

После включения шаблонов сопоставления статус сопоставлений должно быть **Выполняется**. Если статус **Не выполняется**, при первоначальной синхронизации произошли ошибки. Для просмотра ошибок выберите вкладку **Сведения о начальной синхронизации** на странице **Двойная запись**.

![Ошибка на вкладке сведений о начальной синхронизации](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Выполнение начальной синхронизации невозможно: 400 Неправильный запрос

**Роль, требуемая для исправления ошибки:** системный администратор

При попытке запуска сопоставления и исходной синхронизации может появиться следующее сообщение об ошибке:

*(\[Неправильный запрос\], Удаленный сервер вернул ошибку: (400) Неправильный запрос.), при экспорте AX произошла ошибка*

Ниже приведен пример полного сообщения об ошибке.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

Если эта ошибка происходит постоянно, и вы не можете выполнить начальную синхронизацию, выполните следующие действия для устранения проблемы.

1. Выполните вход в виртуальную машину для приложения Finance and Operations.
2. Откройте консоль управления Microsoft.
3. В области **Службы** убедитесь, что запущена служба структуры импорта и экспорта данных Microsoft Dynamics 365. Перезапустите ее, если она была остановлена, так как она необходима для исходной синхронизации.

## <a name="initial-synchronization-error-403-forbidden"></a>Ошибка начальной синхронизации: 403 Запрещено

Во время начальной синхронизации может появиться следующее сообщение об ошибке:

*(\[Запрещено\], Удаленный сервер вернул ошибку: (403) Запрещено.), при экспорте AX произошла ошибка*

Чтобы устранить проблему, выполните следующие действия.

1. Выполните вход в приложение Finance and Operations.
2. На странице **Приложения Azure Active Directory** удалите клиент **DtAppID** и добавьте его снова.

![Клиент DtAppID в списке приложений Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Ошибки ссылки на себя или циклических ссылок во время первоначальной синхронизации

Если какое-либо сопоставление имеет ссылки на себя или циклические ссылки, вы можете получить сообщение об ошибке. Ошибки делятся на следующие категории:

- [Ошибки в сопоставлении таблиц "Поставщики V2" с msdyn_vendors](#error-vendor-map)
- [Ошибки в сопоставлениях таблиц "Клиенты V3" с "Организации"](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Устранение ошибок в сопоставлении таблиц "Поставщики V2" с msdyn_vendors

Возможны ошибки первоначальной синхронизации для составления **Поставщики V2** с **msdyn\_vendors**, если у этих таблиц есть существующие строки, где есть значения в полях **PrimaryContactPersonId** и **InvoiceVendorAccountNumber**. Эти ошибки возникают в связи с тем, что **InvoiceVendorAccountNumber** — это поле ссылки на себя, а **PrimaryContactPersonId** — это циклическая ссылка в сопоставлении поставщиков.

Полученные сообщения об ошибках будет иметь следующую форму.

*Не удалось разрешить GUID для поля: \<field\>. Поиск не найден: \<value\>. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Далее приводятся некоторые примеры.

- *Не удалось разрешить GUID для поля: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Поиск не найден: 000056. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Не удалось разрешить GUID для поля: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Поиск не найден: V24-1. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Если какие-то строки в сущности поставщика имеют значения в полях **PrimaryContactPersonId** и **InvoiceVendorAccountNumber**, выполните следующие шаги, чтобы завершить начальную синхронизацию.

1. В приложении Finance and Operations удалите поля **PrimaryContactPersonId** и **InvoiceVendorAccountNumber** из сопоставления, затем сохраните сопоставление.

    1. На странице сопоставление двойной записи для **Поставщики V2 (msdyn\_vendors)** на вкладке **Сопоставления таблиц** в левом фильтре выберите **Приложения Finance and Operations.Поставщики V2**. В правом фильтре выберите **Sales.Vendor**.
    2. Выполните поиск **primarycontactperson**, чтобы найти поле источника **PrimaryContactPersonId**.
    3. Выберите **Действия**, затем выберите **Удалить**.

        ![Удаление поля PrimaryContactPersonId](media/vend_selfref3.png)

    4. Повторите эти шаги для удаления поля **InvoiceVendorAccountNumber**.

        ![Удаление поля InvoiceVendorAccountNumber](media/vend-selfref4.png)

    5. Сохраните изменения в сопоставлении.

2. Выключите отслеживание изменений для объекта **Поставщики V2**.

    1. В рабочей области **Управление данными** выберите плитку **Таблицы данных**.
    2. Выберите объект **Vendors V2**.
    3. На панели операций выберите **Параметры**, затем выберите **Отслеживание изменений**.

        ![Выбор параметра отслеживания изменений](media/selfref_options.png)

    4. Выберите **Отключить отслеживание изменений**.

        ![Выбор "Отключить отслеживание изменений"](media/selfref_tracking.png)

3. Выполните начальную синхронизацию для сопоставления **Поставщики V2 (msdyn\_vendors)**. Начальная синхронизация должна успешно работать без ошибок.
4. Выполните начальную синхронизацию для составления **Контакты CDS V2 (контакты)**. Необходимо синхронизировать это сопоставление, если следует синхронизировать основное поле контакта в объекте "поставщики", так как начальная синхронизация также должна быть выполнена для строк контактов.
5. Добавьте поля **PrimaryContactPersonId** и **InvoiceVendorAccountNumber** обратно в сопоставление **Поставщики V2 (msdyn\_vendors)**, затем сохраните сопоставление.
6. Выполните начальную синхронизацию еще раз для сопоставления **Поставщики V2 (msdyn\_vendors)**. Так как отслеживание изменений отключено, все строки будут синхронизированы.
7. Снова включите отслеживание изменений для объекта **Поставщики V2**.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>Устранение ошибок в сопоставлениях таблиц "Клиенты V3" с "Организации"

Возможны ошибки первоначальной синхронизации для составления **Клиенты V3** с **Организации**, если у этих таблиц есть существующие строки, где есть значения в полях **ContactPersonID** и **InvoiceAccount**. Эти ошибки возникают, так как что **InvoiceAccount** — это поле ссылки на себя, а **ContactPersonID** — это циклическая ссылка в сопоставлении поставщиков.

Полученные сообщения об ошибках будет иметь следующую форму.

*Не удалось разрешить GUID для поля: \<field\>. Поиск не найден: \<value\>. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Далее приводятся некоторые примеры.

- *Не удалось разрешить GUID для поля: primarycontactid.msdyn\_contactpersonid. Поиск не найден: 000056. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Не удалось разрешить GUID для поля: msdyn\_billingaccount.accountnumber. Поиск не найден: 1206-1. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Если какие-то строки в сущности клиента имеют значения в полях **ContactPersonID** и **InvoiceAccount**, выполните следующие шаги, чтобы завершить начальную синхронизацию. Этот подход можно использовать для всех готовых таблиц, таких как **Организации** и **Контакты**.

1. В приложении Finance and Operations удалите поля **ContactPersonID** и **InvoiceAccount** из сопоставления **Клиенты V3 (организации)**, затем сохраните сопоставление.

    1. Перейдите на страницу сопоставление двойной записи для **Клиенты V3 (организации)** и перейдите на вкладку **Сопоставления таблиц**. В левом фильтре выберите приложения **Приложение Finance and Operations.Клиенты V3**. В правом фильтре выберите **Dataverse.Account**.
    2. Выполните поиск **contactperson**, чтобы найти поле источника **ContactPersonID**.
    3. Выберите **Действия**, затем выберите **Удалить**.

        ![Удаление поля ContactPersonID](media/cust_selfref3.png)

    4. Повторите эти шаги для удаления поля **InvoiceAccount**.

        ![Удаление поля InvoiceAccount](media/cust_selfref4.png)

    5. Сохраните изменения в сопоставлении.

2. Выключите отслеживание изменений для объекта **Клиенты V3**.

    1. В рабочей области **Управление данными** выберите плитку **Таблицы данных**.
    2. Выберите объект **Customers V3**.
    3. На панели операций выберите **Параметры**, затем выберите **Отслеживание изменений**.

        ![Выбор параметра отслеживания изменений](media/selfref_options.png)

    4. Выберите **Отключить отслеживание изменений**.

        ![Выбор "Отключить отслеживание изменений"](media/selfref_tracking.png)

3. Выполните начальную синхронизацию для составления **Клиенты V3 (Организации)**. Начальная синхронизация должна успешно работать без ошибок.
4. Выполните начальную синхронизацию для составления **Контакты CDS V2 (контакты)**.

    > [!NOTE]
    > Существуют два сопоставления с одинаковым именем. Обязательно выберите сопоставление со следующим описанием на вкладке **Сведения**: **Шаблон двойной записи для синхронизации между FO.CDS Vendor Contacts V2 для CDS.Contacts. Требуется новый пакет \[Dynamics365SupplyChainExtended\].**

5. Добавьте поля **InvoiceAccount** и **ContactPersonId** обратно в сопоставление **Клиенты V3 (Организации)**, затем сохраните сопоставление. Оба поля **InvoiceAccount** и **ContactPersonId** теперь будут снова учитываться в режиме синхронизации в реальном времени. На следующем шаге вы выполните начальную синхронизацию для этих полей.
6. Снова выполните начальную синхронизацию для составления **Клиенты V3 (Организации)**. Поскольку отслеживание изменений отключено, данные для **InvoiceAccount** и **ContactPersonId** будут синхронизированы из приложения Finance and Operations в Dataverse.
7. Для синхронизации данных для **InvoiceAccount** и **ContactPersonId** из Dataverse в приложение Finance and Operations необходимо использовать проект интеграции данных.

    1. В Power Apps создайте проект интеграции данных между таблицами **Sales.Account** и **Finance and Operations apps.Customers V3**. Направление данных должно быть из Dataverse в приложение Finance and Operations. Поскольку **InvoiceAccount** является новым атрибутом в двойной записи, можно пропустить начальную синхронизацию для него. Дополнительные сведения см. в разделе [Интеграция данных в Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).

        На следующей иллюстрации показан проект, который обновляет **CustomerAccount** и **ContactPersonId**.

        ![Проект интеграции данных для обновления CustomerAccount и ContactPersonId](media/cust_selfref6.png)

    2. Добавьте критерии компании в фильтр со стороны Dataverse, так что в приложении Finance and Operations будут обновляться только строки, отвечающие условиям фильтра. Чтобы добавить фильтр, выберите кнопку фильтра. Затем, в диалоговом окне **Изменение запроса** можно добавить запрос фильтра, например **\_msdyn\_company\_value eq '\<guid\>'**. 

        > [ПРИМЕЧАНИЕ] Если кнопка фильтра отсутствует, создайте запрос на поддержку, чтобы попросить у группы интеграции данных включить функцию фильтра в вашем клиенте.

        Если не ввести запрос фильтра для **\_msdyn\_company\_value**, то все строки будут синхронизированы.

        ![Добавление запроса фильтра](media/cust_selfref7.png)

    Исходная синхронизация строк теперь завершена.

8. В приложении Finance and Operations снова включите отслеживание изменений для сущности **Клиенты V3**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]