---
title: Устранение проблем с обновлением приложений Finance and Operations
description: В этом разделе содержатся сведения об устранении неполадок, связанных с обновлениями приложений Финансы и операции.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c7c036ef44b0470c9b3f8087e7b5b1e16dde1b34
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062833"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Устранение проблем с обновлением приложений Finance and Operations

[!include [banner](../../includes/banner.md)]





Эта тема предоставляет информацию по устранению неполадок для интеграции войной записи между приложениями Финансы и операции и Dataverse. Конкретно, в этом разделе содержатся сведения об устранении неполадок, связанных с обновлениями приложений Финансы и операции.

> [!IMPORTANT]
> Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD). В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.

## <a name="database-synchronization-errors"></a>Ошибки синхронизации баз данных

**Роль, требуемая для исправления ошибки:** системный администратор

При попытке использовать таблицу **DualWriteProjectConfiguration** для обновления приложения Финансы и операции до обновления платформы Platform update 30, может появиться сообщение об ошибке, которое напоминает следующий пример.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Чтобы устранить проблему, выполните следующие действия.

1. Выполните вход в виртуальную машину для приложения Финансы и операции.
2. Откройте Visual Studio в качестве администратора и откройте репозиторий прикладных объектов (AOT).
3. Выполните поиск **DualWriteProjectConfiguration**.
4. В AOT щелкните правой кнопкой мыши **DualWriteProjectConfiguration** и выберите **Добавить в новый проект**. Выберите **ОК**, чтобы создать новый проект, в котором используются параметры по умолчанию.
5. В обозревателе решений щелкните правой кнопкой мыши **Свойства проекта** и задайте для параметры **Синхронизация базы данных при сборке** значение **True**.
6. Выполните сборку проекта и проверьте, что сборка выполнена успешно.
7. В меню **Dynamics 365** выберите **Синхронизировать базу данных**.
8. Выберите **Синхронизировать** для выполнения полной синхронизации базы данных.
9. После успешного завершения полной синхронизации базы данных перезапустите этап синхронизации базы данных в службах Microsoft Dynamics Lifecycle Services (LCS) и используйте требуемые сценарии обновления вручную, чтобы можно было продолжить обновление.

## <a name="missing-table-columns-issue-on-maps"></a>В картах отсутствуют столбцы таблицы

**Роль, требуемая для исправления ошибки:** системный администратор

На странице **Двойная запись** может быть выведено сообщение об ошибке, подобное следующему примеру:

*Отсутствует исходное поле \<field name\> в схеме.*

![Пример сообщения об ошибке об отсутствующем исходном столбце.](media/error_missing_field.png)

Чтобы устранить проблему, сначала необходимо выполнить следующие действия, чтобы убедиться в наличии столбцов в таблице.

1. Выполните вход в виртуальную машину для приложения Финансы и операции.
2. Выберите **Рабочие области \> Управление данными**, выберите плитку **Параметры структуры**, затем на вкладке **Параметры таблицы** выберите **Обновить список таблиц**, чтобы обновить таблицы.
3. Выберите **Рабочие области \> Управление данными**, выберите вкладку **Таблицы данных** и убедитесь, что таблица указана в списке. Если таблица отсутствует в списке, выполните вход в виртуальную машину для приложения Финансы и операции и убедитесь, что таблица доступна.
4. Откройте страницу **Сопоставление таблиц** со страницы **Двойная запись** в приложении Финансы и операции.
5. Выберите **Обновить список таблиц**, чтобы автоматически заполнить столбцы в сопоставлениях таблиц.

Если проблема все еще не устранена, выполните следующие действия.

> [!IMPORTANT]
> В этих шагах выполняется процедура удаления таблицы и добавления ее снова. Чтобы избежать проблем, обязательно точно выполните описанные шаги.

1. В приложении Финансы и операции перейдите к пункту **Рабочие области \> Управление данными** и выберите плитку **Таблицы данных**.
2. Найдите таблицу, в которой отсутствует атрибут. Нажмите **Изменить целевое сопоставление** на панели инструментов.
3. В области **Сопоставить промежуточные данные с целевыми** щелкните **Создать сопоставление**.
4. Откройте страницу **Сопоставление таблиц** со страницы **Двойная запись** в приложении Финансы и операции.
5. Если атрибут не был автоматически заполнен в сопоставлении, добавьте его вручную, нажав кнопку **Добавить атрибут**, затем щелкнув **Сохранить**. 
6. Выберите сопоставление и щелкните **Выполнить**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]