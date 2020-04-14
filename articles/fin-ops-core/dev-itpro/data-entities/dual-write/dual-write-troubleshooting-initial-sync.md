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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172722"
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

## <a name="self-reference-failures-during-initial-synchronization"></a>Ошибки ссылки на себя во время первоначальной синхронизации

Если какое-либо сопоставление имеет ссылки на себя, вы можете получить сообщение об ошибке, подобное следующему примеру:

*В Vendors V2 следующая ошибка: код записи: новая запись, ErrorMessage: Невозможно разрешить guid для поля: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Значение подстановки не найдено: CN-001. Попробуйте эти URL-адреса для проверки, существуют ли ссылочные данные: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*

Этот тип ошибки происходит во время первоначальной синхронизации сопоставлений, которые содержат ссылки на себя. В предыдущем примере счет накладной в поле ссылается на объект поставщика.

Чтобы устранить эту проблему, возможно, потребуется выполнить сопоставление два раза до успешного выполнения первоначальной синхронизации.

