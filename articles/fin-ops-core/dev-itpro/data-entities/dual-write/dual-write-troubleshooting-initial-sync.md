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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410089"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Устранение неполадок при начальной синхронизации

[!include [banner](../../includes/banner.md)]

Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Common Data Service. А именно, содержатся сведения об устранении неполадок, которые могут возникнуть при начальной синхронизации.

> [!IMPORTANT]
> Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD). В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Проверка наличия ошибок исходной синхронизации в приложении Finance and Operations

После включения шаблонов сопоставления статус сопоставлений должно быть **Выполняется**. Если статус **Не выполняется**, при первоначальной синхронизации произошли ошибки. Для просмотра ошибок выберите вкладку **Сведения о начальной синхронизации** на странице **Двойная запись**.

![Вкладка сведений о начальной синхронизации](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Выполнение начальной синхронизации невозможно: 400 Неправильный запрос

**Роль, требуемая для исправления ошибки:** системный администратор

При попытке запуска сопоставления и исходной синхронизации может появиться следующее сообщение об ошибке:

*Удаленный сервер вернул ошибку: (400) Неправильный запрос.), при экспорте AX произошла ошибка*

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

![Список приложений Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Ошибки ссылки на себя или циклических ссылок во время первоначальной синхронизации

Если какое-либо сопоставление имеет ссылки на себя или циклические ссылки, вы можете получить сообщение об ошибке. Ошибки делятся на следующие категории:

- [Сопоставление объекта Vendors V2 для msdyn_vendors"](#error-vendor-map)
- [Сопоставление объектов Vendors V3 для "Организации"](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Устранение ошибки в сопоставлении объектов Vendors V2 для msdyn_vendors"

Возможны следующие ошибки первоначальной синхронизации в составлении **Vendors V2** для **msdyn_vendors**, если у этих объектов есть существующие записи со значениями в полях **PrimaryContactPersonId** и **InvoiceVendorAccountNumber**. Это связано с тем, что **InvoiceVendorAccountNumber** — это полем ссылки на себя, а **PrimaryContactPersonId** — это циклическая ссылка в сопоставлении поставщиков.

*Не удалось разрешить GUID для поля: <field>. Поиск не найден: <value>. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

Вот несколько примеров:

- *Не удалось разрешить GUID для поля: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Поиск не найден: 000056. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Не удалось разрешить GUID для поля: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Поиск не найден: V24-1. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

Если имеются записи со значениями в этих полях объекта поставщика, выполните шаги, указанные в приведенном ниже разделе, чтобы успешно завершить начальную синхронизацию.

1. В приложении Finance and Operations удалите поля **PrimaryContactPersonId** и **InvoiceVendorAccountNumber** из сопоставления и сохраните изменения.

    1. Перейдите на страницу сопоставление двойной записи для **Vendors V2 (msdyn_vendors)** и перейдите на вкладку **Сопоставления объектов**. В левом фильтре выберите приложения **Finance and Operations. apps.Vendors V2**. В правом фильтре выберите **Sales.Vendor**.

    2. Выполните поиск **primarycontactperson**, чтобы найти поле источника **PrimaryContactPersonId**.
    
    3. Щелкните кнопку **Действия** и выберите **Удалить**.
    
        ![ссылка на себя или циклическая ссылка 3](media/vend_selfref3.png)
    
    4. Повторите для удаления поля **InvoiceVendorAccountNumber**.
    
        ![ссылка на себя или циклическая ссылка 4](media/vend-selfref4.png)
    
    5. Сохраните изменения сопоставления.

2. Отключение отслеживания изменений для объекта **Vendors V2**.

    1. Перейдите **Управление данными \> Объекты данных**.
    
    2. Выберите объект **Vendors V2**.
    
    3. Щелкните **Параметры** в строке меню и выберите **Отслеживание изменений**.
    
        ![ссылка на себя или циклическая ссылка 5](media/selfref_options.png)
    
    4. Щелкните **Отключить отслеживание изменений**.
    
        ![ссылка на себя или циклическая ссылка 6](media/selfref_tracking.png)

3. Выполните начальную синхронизацию сопоставления **Vendors V2 (msdyn_vendors)**. Начальная синхронизация должна успешно работать без ошибок.

4. Выполните начальную синхронизацию для составления **CDS Contacts V2 (contacts)**. Необходимо синхронизировать это сопоставление, если следует синхронизировать основное поле контакта в объекте "поставщики", так как записи контактов также должны быть первоначально синхронизованы.

5. Добавьте поля **PrimaryContactPersonId** и **InvoiceVendorAccountNumber** обратно в сопоставление **Vendors V2 (msdyn_vendors)** и сохраните сопоставление.

6. Снова выполните начальную синхронизацию сопоставления **Vendors V2 (msdyn_vendors)**. Все записи будут синхронизированы, так как отслеживание изменений отключено.

7. Включите отслеживание изменений для объекта **Vendors V2**.

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>Устранение ошибки в сопоставлениях объектов Customers V3 для "Организации"

Возможны следующие ошибки первоначальной синхронизации в составлении **Customers V3** для **"Организации"**, если у этих объектов есть существующие записи со значениями в полях **ContactPersonID** и **InvoiceAccount**. Это связано с тем, что **InvoiceAccount** — это полем ссылки на себя, а **ContactPersonID** — это циклическая ссылка в сопоставлении поставщиков.

*Не удалось разрешить GUID для поля: <field>. Поиск не найден: <value>. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

- *Не удалось разрешить GUID для поля: primarycontactid.msdyn_contactpersonid. Поиск не найден: 000056. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Не удалось разрешить GUID для поля: msdyn_billingaccount.accountnumber. Поиск не найден: 1206-1. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*

Если имеются записи со значениями в этих полях объекта клиента, выполните шаги, указанные в приведенном ниже разделе, чтобы успешно завершить начальную синхронизацию. Этот подход можно использовать для всех готовых элементов, таких как "организации" и "контакты".

1. В приложении Finance and Operations удалите поля **ContactPersonID** и **InvoiceAccount** из сопоставления **Клиенты V3 (Организации)** и сохраните сопоставление.

    1. Перейдите на страницу сопоставление двойной записи для **Клиенты V3 (Организации)** и перейдите на вкладку **Сопоставления объектов**. В левом фильтре выберите приложения **Finance and Operations app.Customers V3**. В правом фильтре выберите **Common Data Service.Account**.

    2. Выполните поиск **contactperson**, чтобы найти поле источника **ContactPersonID**.
    
    3. Щелкните кнопку **Действия** и выберите **Удалить**.
    
        ![ссылка на себя или циклическая ссылка 3](media/cust_selfref3.png)
    
    4. Повторите для удаления поля **InvoiceAccount**.
    
        ![ссылка на себя или циклическая ссылка](media/cust_selfref4.png)
    
    5. Сохраните изменения сопоставления.

2. Отключение отслеживания изменений для объекта **Customers V3**.

    1. Перейдите **Управление данными \> Объекты данных**.
    
    2. Выберите объект **Customers V3**.
    
    3. Щелкните **Параметры** в строке меню и выберите **Отслеживание изменений**.
    
        ![ссылка на себя или циклическая ссылка 5](media/selfref_options.png)
    
    4. Щелкните **Отключить отслеживание изменений**.
    
        ![ссылка на себя или циклическая ссылка 6](media/selfref_tracking.png)

3. Выполните начальную синхронизацию для составления **Клиенты V3 (Организации)**. Начальная синхронизация должна успешно работать без ошибок.

4. Выполните начальную синхронизацию для составления **CDS Contacts V2 (contacts)**. Имеется 2 сопоставления с одинаковым именем. Выберите один с описанием **Шаблон двойной записи для синхронизации между FO.CDS Vendor Contacts V2 для CDS.Contacts. Требуется новый пакет \[Dynamics365SupplyChainExtended\].** на вкладке **Сведения** сопоставления.

5. Добавьте поля **InvoiceAccount** и **ContactPersonId** обратно в сопоставление **Клиенты V3 (Организации)** и сохраните сопоставление. Теперь оба поля **InvoiceAccount** и **ContactPersonId** снова будут учтены в реальной синхронизации. На следующем шаге выполняется начальная синхронизация этих полей.

6. Снова выполните начальную синхронизацию для составления **Клиенты V3 (Организации)**. Поскольку отслеживание изменений отключено, выполнение синхронизации приведет к синхронизации данных для **InvoiceAccount** и **ContactPersonId** из приложения Finance and Operations в Common Data Service.

7. Для синхронизации данных для **InvoiceAccount** и **ContactPersonId** из Common Data Service в Finance and Operations можно использовать проект интеграции данных.

    1. В Power Apps создайте проект интеграции данных между объектами **Sales.Account** и **Finance and Operations apps.Customers V3**. Направление данных должно быть из Common Data Service в приложение Finance and Operations.  Поскольку **InvoiceAccount** является новым атрибутом в двойной записи, можно пропустить начальную синхронизацию для этого атрибута. Дополнительные сведения см. в разделе [Интеграция данных в Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        На следующем рисунке показан проект, который обновляет **CustomerAccount** и **ContactPersonId**.

        ![ссылка на себя или циклическая ссылка](media/cust_selfref6.png)

    2. Добавьте критерии компании в фильтр со стороны Common Data Service, так как в приложении Finance and Operations будут обновлены только записи, отвечающие условиям фильтра. Чтобы добавить фильтр, щелкните значок фильтра. В диалоговом окне **Изменение запроса** можно добавить запрос фильтра, например **_msdyn_company_value eq '\<guid\>'**. Если значок фильтра отсутствует, создайте запрос на поддержку, чтобы попросить у группы интеграции данных включить функцию фильтра в вашем клиенте. Если не ввести запрос фильтра для **_msdyn_company_value**, то все записи будут синхронизированы.

        ![ссылка на себя или циклическая ссылка](media/cust_selfref7.png)

        Это завершение начальной синхронизации записей.

8. Включите отслеживание изменений для объекта **Customers V3** в приложении Finance and Operations.

