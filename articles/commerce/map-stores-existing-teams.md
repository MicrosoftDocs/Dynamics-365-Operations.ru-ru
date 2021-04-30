---
title: Сопоставление магазинов и рабочих групп, если имеются готовые рабочие группы в Microsoft Teams
description: В этой теме описывается, как сопоставить магазины и соответствующие рабочие группы в Dynamics 365 Commerce Headquarters, если ваша организация уже создала рабочие группы в Microsoft Teams перед интеграцией Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3edd176788b24a5f5246e9b7bcb3c6fbcdca2254
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842732"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>Сопоставление магазинов и рабочих групп, если имеются готовые рабочие группы в Microsoft Teams

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

В этой теме описывается, как сопоставить магазины и соответствующие рабочие группы в Dynamics 365 Commerce Headquarters, если ваша организация уже создала рабочие группы в Microsoft Teams перед интеграцией Commerce.

Ваша организация могла создать рабочие группы для некоторых или всех магазинов до интеграции Dynamics 365 Commerce и Microsoft Teams. В этом случае чтобы установить синхронизацию задач между Commerce POS и Microsoft Teams, необходимо предоставить сопоставление магазинов и соответствующей рабочей команды в Commerce Headquarters.

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>Сопоставление магазинов и соответствующих рабочих групп в Commerce Headquarters 

Чтобы сопоставить магазины и соответствующие рабочие группы в Commerce Headquarters, выполните следующие действия.

1. Перейдите в раздел **Администрирование системы \> Рабочая область \> Управление данными**.
1. Выберите **Экспорт**. 
1. В области действий выберите **Создать**.
1. В поле **Имя группы** введите "Экспорт сопоставления Teams".
1. На экспресс-вкладке **Выбранные сущности** выберите **Добавить сущность**. Отобразится диалоговое окно **Добавление сущности**.  
1. В раскрывающемся списке **Имя сущности** выберите **Сопоставление рабочих групп между источником и рабочей группой**.
1. В раскрывающемся списке **Целевой формат данных** выберите **CSV**.
1. Выберите **Добавить**, затем выберите **Закрыть**.
1. В верхнем левом углу в области действий выберите **Экспортировать сейчас**.
1. В разделе **Статус обработки объекта** выберите **Загрузить файл**.
1. В экспортированном CSV-файле введите значения для параметров **SOURCETYPE**, **SOURCEID** и **TEAMID** следующим образом:
    - Для **SOURCETYPE** введите "RetailStore". 
    - Для **SOURCEID** введите номер магазина (например, "000135" для магазина в Сан-Франциско). Номера магазинов можно найти в разделе **Retail и Commerce \> Каналы \> Магазины**.
    - Для **TEAMID** введите соответствующий код рабочей группы из Microsoft Teams (например, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c"). Сведения о коде группы можно найти в [admin.teams.microsoft.com](https://admin.teams.microsoft.com).
1. Сохраните CSV-файл на локальном компьютере.
1. Перейдите в раздел **Администрирование системы \> Рабочая область \> Управление данными**, затем выберите **Импорт**.
1. На экспресс-вкладке **Выбранные сущности** выберите **Добавить файл**. Откроется диалоговое окно **Добавление файла**.
1. В раскрывающемся списке **Имя сущности** выберите **Сопоставление рабочих групп между источником и рабочей группой**.
1. В раскрывающемся списке **Формат исходных данных** выберите **CSV**.
1. Выберите **Отправить и добавить**, выберите CSV-файл, который ранее был сохранен, затем выберите **Открыть**.
1. В диалоговом окне **Добавить файл** выберите **Закрыть**.
1. На панели операций выберите **Сохранить**, затем выберите **Импорт**.

В следующем примере изображения показана группа **Экспорт сопоставления Teams** в Commerce с выделенными элементами **Добавить объект** и экспортированными заголовками CSV-файла.

![Группа экспорта сопоставлений Teams в Commerce с выделенными элементами добавления объектов и экспортированными заголовками CSV-файла](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> После выполнения описанных выше шагов выполните шаги из раздела [Синхронизация управления задачами между Microsoft Teams и POS-терминалом](synchronize-tasks-teams-pos.md) для синхронизации управления задачами. 

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор интеграции Dynamics 365 Commerce и Microsoft Teams](commerce-teams-integration.md)

[Включение интеграции Dynamics 365 Commerce и Microsoft Teams](enable-teams-integration.md)

[Подготовка Microsoft Teams из Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Синхронизация управления задачами между Microsoft Teams и Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Управление ролями пользователей в Microsoft Teams](manage-user-roles-teams.md)

[Вопросы и ответы по интеграции Dynamics 365 Commerce и Microsoft Teams](teams-integration-faq.md)