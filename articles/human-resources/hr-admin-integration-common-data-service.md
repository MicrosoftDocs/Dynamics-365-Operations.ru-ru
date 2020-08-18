---
title: Настройка интеграции с Common Data Service
description: Можно включать и выключать интеграцию между Common Data Service и Dynamics 365 Human Resources. Можно также просмотреть сведения о синхронизации, удалить данные отслеживания и повторно синхронизировать объект, чтобы помочь в устранении ошибок данных в этих средах.
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 8cbead2961c4576a5394080aae2fec109bce3f10
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621312"
---
# <a name="configure-common-data-service-integration"></a>Настройка интеграции с Common Data Service

Можно включать и выключать интеграцию между Common Data Service и Dynamics 365 Human Resources. Можно также просмотреть сведения о синхронизации, удалить данные отслеживания и повторно синхронизировать объект, чтобы помочь в устранении ошибок данных в этих средах.

После отключения интеграции пользователи могут вносить изменения в Human Resources или Common Data Service, но эти изменения не синхронизируются между этими двумя средами.

По умолчанию интеграция между Human Resources и Common Data Service выключена.

В следующих ситуациях может потребоваться отключить интеграцию:

- Данные заполняются с помощью платформы управления данными и должны быть импортированы несколько раз, чтобы перевести их в правильное состояние.

- Имеются проблемы, связанные с данными в Human Resources или Common Data Service. Если интеграция отключена, можно удалить запись в одной среде, не удаляя ее в другой. При повторном включении интеграции запись в среде, в которой она не была удалена, синхронизируется со средой, в которой она была удалена. Синхронизация начинается при следующем запуске пакетного задания **Синхронизация пропущенных запросов для интеграции Common Data Service**.

> [!WARNING]
> При отключении интеграции данных убедитесь, что в обеих средах не редактируется одна и та же запись. При включении интеграции обратно, последняя измененная запись будет синхронизирована. Таким образом, если изменения в записи в обеих средах не были внесены, может произойти потеря данных.

## <a name="access-the-common-data-service-integration-page"></a>Доступ к странице интеграции Common Data Service

1. В экземпляре Human Resources, для которого необходимо просмотреть или настроить параметры интеграции с Common Data Service, выберите плитку **Администрирование системы**.

    [![Плитка администрирования системы](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Выберите вкладку **Ссылки**.

    [![Вкладка ссылок](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. В **Интеграции** выберите **конфигурация Common Data Service**.

    [![Ссылка на конфигурацию Common Data Service](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>Включение и выключение интеграции между Human Resources и Common Data Service

- Чтобы включить интеграцию, установите параметр **Разрешить интеграцию с Common Data Service** как **Да**.

    > [!NOTE]
    > При включении интеграции данные будут синхронизированы при следующем запуске пакетного задания **Синхронизация пропущенных запросов для интеграции Common Data Service**. Все данные должны быть доступны после завершения пакетного задания.

- Чтобы отключить интеграцию, установите для параметра значение **Нет**.

[![Включение или отключение интеграции Common Data Service](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

> [!WARNING]
> Настоятельно рекомендуется отключить интеграцию Common Data Service при выполнении задач переноса данных. Большие объемы передачи данных могут значительно повлиять на производительность системы. Например, отправка 2000 работников может занять несколько часов, если интеграция включена, и менее одного часа при отключении. Представленные в этом примере номера предназначены только для демонстрационных целей. Точное количество времени, необходимое для импорта записей, может сильно различаться в зависимости от многих факторов.

## <a name="view-data-integration-details"></a>Просмотр сведений об интеграции данных

На экспресс-вкладке **Администрирование** на странице **Интеграция Common Data Service** можно увидеть, как взаимосвязаны записи между Human Resources и Common Data Service.

- Чтобы просмотреть записи для объекта, выберите объект в поле **Имя объекта CDS**. В сетке отображаются все записи, связанные с выбранным объектом.

[![Просмотр записей для объекта](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> Не все объекты Common Data Service в данный момент перечисляются. В сетке отображаются только те объекты, которые поддерживают использование настраиваемых полей. Новые объекты становятся доступными через непрерывные выпуски Human Resources.

Сетка содержит следующие поля:

- **Имя объекта CDS** — имя объекта в Common Data Service.
- **Ссылка на объект CDS** — идентификатор, используемый Common Data Service для идентификации записи. Это значение аналогично значению **RecID** для Human Resources. Идентификатор можно найти при открытии объекта Common Data Service в Microsoft Excel.
- **Имя объекта Human Resources** — объект, который последний раз синхронизировал данные с Common Data Service. Объект может иметь либо префикс Common Data Service, либо другой префикс.
- **Ссылка Human Resources** — значение **RecId**, связанное с записью в Human Resources.
- **Удалено из CDS** — значение, указывающее, была ли удалена запись из Common Data Service.

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>Удаление связи записи в Human Resources из Common Data Service

При возникновении проблем с синхронизацией данных в процессе синхронизации между Human Resources и Common Data Service можно разрешить их устранение путем очистки отслеживания и повторной синхронизации таблицы отслеживания. Если удалить связь, а затем изменить или удалить запись в Common Data Service, изменения не будут синхронизированы с Human Resources. При внесении изменений в Human Resources создается новая запись отслеживания и обновляется запись в Common Data Service.

- Чтобы удалить связь записи между Human Resources и Common Data Service выберите объект в поле **Имя объекта CDS**, а затем выберите **Удалить информацию отслеживания**.

[![Очистка информации отслеживания](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

Чтобы выполнить полную синхронизацию объекта после очистки отслеживания, см. следующую процедуру.

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>Синхронизация объекта между Human Resources и Common Data Service

Используйте эту процедуру, если:

- Изменения из Common Data Service слишком долго не появляются в Human Resources.

- После очистки отслеживания необходимо обновить таблицу отслеживания.

Для выполнения полной синхронизации с объектом между модулем Human Resources и Common Data Service:

1. Выберите объект в поле **Имя объекта CDS**.

2. Выберите **Синхронизировать**.

[![Выполнение полной синхронизации](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)


