---
title: Устранение неполадок, связанных с обновлениями приложений Finance and Operations
description: В этом разделе содержатся сведения об устранении неполадок, связанных с обновлениями приложений Finance and Operations.
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
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172885"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a>Устранение неполадок, связанных с обновлениями приложений Finance and Operations

[!include [banner](../../includes/banner.md)]



Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Common Data Service. Конкретно, в этом разделе содержатся сведения об устранении неполадок, связанных с обновлениями приложений Finance and Operations.

> [!IMPORTANT]
> Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD). В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.

## <a name="database-synchronization-errors"></a>Ошибки синхронизации баз данных

**Роль, требуемая для исправления ошибки:** системный администратор

При попытке использовать объект **DualWriteProjectConfiguration** для обновления приложения Finance and Operations до обновления платформы Platform update 30, может появиться сообщение об ошибке, которое напоминает следующий пример.

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Чтобы устранить проблему, выполните следующие действия.

1. Выполните вход в виртуальную машину для приложения Finance and Operations.
2. Откройте Visual Studio в качестве администратора и откройте репозиторий прикладных объектов (AOT).
3. Выполните поиск **DualWriteProjectConfiguration**.
4. В AOT щелкните правой кнопкой мыши **DualWriteProjectConfiguration** и выберите **Добавить в новый проект**. Выберите **ОК**, чтобы создать новый проект, в котором используются параметры по умолчанию.
5. В обозревателе решений щелкните правой кнопкой мыши **Свойства проекта** и задайте для параметры **Синхронизация базы данных при сборке** значение **True**.
6. Выполните сборку проекта и проверьте, что сборка выполнена успешно.
7. В меню **Dynamics 365** выберите **Синхронизировать базу данных**.
8. Выберите **Синхронизировать** для выполнения полной синхронизации базы данных.
9. После успешного завершения полной синхронизации базы данных перезапустите этап синхронизации базы данных в службах Microsoft Dynamics Lifecycle Services (LCS) и используйте требуемые сценарии обновления вручную, чтобы можно было продолжить обновление.

## <a name="missing-entity-fields-issue-on-maps"></a>Проблема с отсутствующими полями объекта на картах

**Роль, требуемая для исправления ошибки:** системный администратор

На странице **Двойная запись** может быть выведено сообщение об ошибке, подобное следующему примеру:

*Отсутствует исходное поле \<имя поля\> в схеме.*

![Пример сообщения об ошибке об отсутствующем исходном поле](media/error_missing_field.png)

Чтобы устранить проблему, сначала необходимо выполнить следующие действия, чтобы убедиться в наличии полей в объекте.

1. Выполните вход в виртуальную машину для приложения Finance and Operations.
2. Выберите **Рабочие области \> Управление данными**, выберите плитку **Параметры структуры**, затем на вкладке **Параметры объекта** выберите **Обновить список объектов**, чтобы обновить объекты.
3. Выберите **Рабочие области \> Управление данными**, выберите вкладку **Объекты данных** и убедитесь, что объект указан в списке. Если объект отсутствует в списке, выполните вход в виртуальную машину для приложения Finance and Operations и убедитесь, что объект доступен.
4. Откройте страницу **Сопоставление объектов** со страницы **Двойная запись** в приложении Finance and Operations.
5. Выберите **Обновить список объектов**, чтобы автоматически заполнить поля в сопоставлениях объектов.

Если проблема все еще не устранена, выполните следующие действия.

> [!IMPORTANT]
> В этих шагах выполняется процедура удаления объекта и добавления его снова. Чтобы избежать проблем, обязательно точно выполните описанные шаги.

1. В приложении Finance and Operations перейдите к пункту **Рабочие области \> Управление данными** и выберите плитку **Объекты данных**.
2. Найдите объект, в котором отсутствует поле. Запишите целевой объект, промежуточную таблицу, имя объекта и другие значения столбцов.
3. Если какая-либо из групп обработки зависит от этого объекта, перед удалением объекта выполните соответствующие действия для групп обработки.
4. Удалите объект, в котором отсутствует поле.
5. Выберите **Создать** и снова добавьте объект. Укажите значения, которые были записаны на шаге 2.
6. Откройте страницу **Сопоставление объектов** со страницы **Двойная запись** в приложении Finance and Operations.
7. Выберите **Обновить список объектов**, чтобы автоматически заполнить поля в сопоставлениях объектов.
