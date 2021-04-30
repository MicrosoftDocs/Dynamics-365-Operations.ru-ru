---
title: Настройка интеграции с Dataverse
description: Можно включать и выключать интеграцию между Microsoft Dataverse и Dynamics 365 Human Resources. Можно также просмотреть сведения о синхронизации, удалить данные отслеживания и повторно синхронизировать таблицу, чтобы помочь в устранении ошибок данных в этих средах.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf406a954f5bb8b49627b58a901d0721cdad407b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890036"
---
# <a name="configure-dataverse-integration"></a>Настройка интеграции с Dataverse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Можно включать и выключать интеграцию между Microsoft Dataverse и Dynamics 365 Human Resources. Можно также просмотреть сведения о синхронизации, удалить данные отслеживания и повторно синхронизировать таблицу, чтобы помочь в устранении ошибок данных в этих средах.

> [!NOTE]
> Дополнительные сведения об Dataverse (ранее Common Data Service) и обновлениях терминологии см. в разделе [Что такое Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

После отключения интеграции пользователи могут вносить изменения в Human Resources или Dataverse, но эти изменения не синхронизируются между этими двумя средами.

По умолчанию интеграция между Human Resources и Dataverse выключена.

В следующих ситуациях может потребоваться отключить интеграцию:

- Данные заполняются с помощью платформы управления данными и должны быть импортированы несколько раз, чтобы перевести их в правильное состояние.

- Имеются проблемы, связанные с данными в Human Resources или Dataverse. Если интеграция отключена, можно удалить запись в одной среде, не удаляя ее в другой. При повторном включении интеграции запись в среде, в которой она не была удалена, синхронизируется со средой, в которой она была удалена. Синхронизация начинается при следующем запуске пакетного задания **Синхронизация пропущенных запросов для интеграции Dataverse**.

> [!WARNING]
> При отключении интеграции данных убедитесь, что в обеих средах не редактируется одна и та же запись. При включении интеграции обратно, последняя измененная запись будет синхронизирована. Таким образом, если изменения в записи в обеих средах не были внесены, может произойти потеря данных.

## <a name="access-the-dataverse-integration-page"></a>Доступ к странице интеграции Dataverse

1. В экземпляре Human Resources, для которого необходимо просмотреть или настроить параметры интеграции с Dataverse, выберите плитку **Администрирование системы**.

    [![Плитка администрирования системы](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Выберите вкладку **Ссылки**.

    [![Вкладка ссылок](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. В **Интеграции** выберите **конфигурация Dataverse**.

    [![Ссылка на конфигурацию Dataverse](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>Включение и выключение интеграции между Human Resources и Dataverse

- Чтобы включить интеграцию, установите параметр **Разрешить интеграцию с Dataverse** как **Да** на странице **Интеграция Microsoft Dataverse**.

    > [!NOTE]
    > При включении интеграции данные будут синхронизированы при следующем запуске пакетного задания **Синхронизация пропущенных запросов для интеграции Dataverse**. Все данные должны быть доступны после завершения пакетного задания.

- Чтобы отключить интеграцию, установите для параметра значение **Нет**.

[![Включение или отключение интеграции Dataverse](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> Настоятельно рекомендуется отключить интеграцию Dataverse при выполнении задач переноса данных. Большие объемы передачи данных могут значительно повлиять на производительность системы. Например, отправка 2000 работников может занять несколько часов, если интеграция включена, и менее одного часа при отключении. Представленные в этом примере номера предназначены только для демонстрационных целей. Точное количество времени, необходимое для импорта записей, может сильно различаться в зависимости от многих факторов.

## <a name="view-data-integration-details"></a>Просмотр сведений об интеграции данных

На экспресс-вкладке **Администрирование** на странице **Интеграция Microsoft Dataverse** можно увидеть, как взаимосвязаны строки между Human Resources и Dataverse.

- Для просмотра строк таблицы выберите таблицу в поле **Таблица Dataverse**. В сетке отображаются все строки, связанные с выбранной таблицей.

> [!NOTE]
> Не все таблицы Dataverse в данный момент перечисляются. В сетке отображаются только те таблицы, которые поддерживают использование настраиваемых полей. Новые таблицы становятся доступными через непрерывные выпуски Human Resources.

Сетка содержит следующие поля:

- **Таблица Dataverse** — имя таблицы в Dataverse.
- **Ссылка на таблицу Dataverse** — идентификатор, используемый Dataverse для идентификации записи. Это значение аналогично значению **RecID** для Human Resources. Идентификатор можно найти при открытии таблицы Dataverse в Microsoft Excel.
- **Имя объекта Human Resources** — сущность Human Resources, которая последний раз синхронизировала данные с Dataverse. Объект может иметь либо префикс Dataverse, либо другой префикс.
- **Ссылка Human Resources** — значение **RecId**, связанное с записью в Human Resources.
- **Удалено из Dataverse** — значение, указывающее, была ли удалена строка из Dataverse.

> [!NOTE]
> Записи в Human Resources соответствуют строкам в Dataverse.

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>Удаление связи записи Human Resources из строки Dataverse

При возникновении проблем с синхронизацией данных в процессе синхронизации между Human Resources и Dataverse можно разрешить их устранение путем очистки отслеживания и повторной синхронизации таблицы отслеживания. Если удалить связь, а затем изменить или удалить строку в Dataverse, изменения не будут синхронизированы с Human Resources. При внесении изменений в Human Resources создается новая запись отслеживания и обновляется строка в Dataverse.

- Чтобы удалить связь записи Human Resources и строки Dataverse выберите таблицу в поле **Таблица Dataverse**, затем выберите **Удалить информацию отслеживания**.

[![Очистка информации отслеживания](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

Чтобы выполнить полную синхронизацию таблицы после очистки отслеживания, см. следующую процедуру.

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>Синхронизация таблицы между Human Resources и Dataverse

Используйте эту процедуру, если:

- Изменения из Dataverse слишком долго не появляются в Human Resources.

- После очистки отслеживания необходимо обновить таблицу отслеживания.

Для выполнения полной синхронизации с таблицей между модулем Human Resources и Dataverse:

1. Выберите таблицу в поле **Таблица Dataverse**.

2. Выберите **Синхронизировать**.

[![Выполнение полной синхронизации](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>См. также

[Таблицы Dataverse](hr-developer-entities.md)<br>
[Настройка виртуальных таблиц Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Вопросы и ответы по виртуальным таблицам Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Что такое Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Обновления терминологии](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]