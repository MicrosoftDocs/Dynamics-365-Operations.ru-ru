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
ms.openlocfilehash: 5a711c1057b87bd792755ef91a84d1c28879c590
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908503"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="f1494-103">Сопоставление магазинов и рабочих групп, если имеются готовые рабочие группы в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f1494-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1494-104">В этой теме описывается, как сопоставить магазины и соответствующие рабочие группы в Dynamics 365 Commerce Headquarters, если ваша организация уже создала рабочие группы в Microsoft Teams перед интеграцией Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1494-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="f1494-105">Ваша организация могла создать рабочие группы для некоторых или всех магазинов до интеграции Dynamics 365 Commerce и Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f1494-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="f1494-106">В этом случае чтобы установить синхронизацию задач между Commerce POS и Microsoft Teams, необходимо предоставить сопоставление магазинов и соответствующей рабочей команды в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="f1494-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="f1494-107">Сопоставление магазинов и соответствующих рабочих групп в Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="f1494-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="f1494-108">Чтобы сопоставить магазины и соответствующие рабочие группы в Commerce Headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f1494-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f1494-109">Перейдите в раздел **Администрирование системы \> Рабочая область \> Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="f1494-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="f1494-110">Выберите **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="f1494-110">Select **Export**.</span></span> 
1. <span data-ttu-id="f1494-111">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f1494-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f1494-112">В поле **Имя группы** введите "Экспорт сопоставления Teams".</span><span class="sxs-lookup"><span data-stu-id="f1494-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="f1494-113">На экспресс-вкладке **Выбранные сущности** выберите **Добавить сущность**.</span><span class="sxs-lookup"><span data-stu-id="f1494-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="f1494-114">Отобразится диалоговое окно **Добавление сущности**.</span><span class="sxs-lookup"><span data-stu-id="f1494-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="f1494-115">В раскрывающемся списке **Имя сущности** выберите **Сопоставление рабочих групп между источником и рабочей группой**.</span><span class="sxs-lookup"><span data-stu-id="f1494-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="f1494-116">В раскрывающемся списке **Целевой формат данных** выберите **CSV**.</span><span class="sxs-lookup"><span data-stu-id="f1494-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="f1494-117">Выберите **Добавить**, затем выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="f1494-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="f1494-118">В верхнем левом углу в области действий выберите **Экспортировать сейчас**.</span><span class="sxs-lookup"><span data-stu-id="f1494-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="f1494-119">В разделе **Статус обработки объекта** выберите **Загрузить файл**.</span><span class="sxs-lookup"><span data-stu-id="f1494-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="f1494-120">В экспортированном CSV-файле введите значения для параметров **SOURCETYPE**, **SOURCEID** и **TEAMID** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f1494-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="f1494-121">Для **SOURCETYPE** введите "RetailStore".</span><span class="sxs-lookup"><span data-stu-id="f1494-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="f1494-122">Для **SOURCEID** введите номер магазина (например, "000135" для магазина в Сан-Франциско).</span><span class="sxs-lookup"><span data-stu-id="f1494-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="f1494-123">Номера магазинов можно найти в разделе **Retail и Commerce \> Каналы \> Магазины**.</span><span class="sxs-lookup"><span data-stu-id="f1494-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="f1494-124">Для **TEAMID** введите соответствующий код рабочей группы из Microsoft Teams (например, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span><span class="sxs-lookup"><span data-stu-id="f1494-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="f1494-125">Сведения о коде группы можно найти в [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="f1494-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="f1494-126">Сохраните CSV-файл на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="f1494-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="f1494-127">Перейдите в раздел **Администрирование системы \> Рабочая область \> Управление данными**, затем выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="f1494-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="f1494-128">На экспресс-вкладке **Выбранные сущности** выберите **Добавить файл**.</span><span class="sxs-lookup"><span data-stu-id="f1494-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="f1494-129">Откроется диалоговое окно **Добавление файла**.</span><span class="sxs-lookup"><span data-stu-id="f1494-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="f1494-130">В раскрывающемся списке **Имя сущности** выберите **Сопоставление рабочих групп между источником и рабочей группой**.</span><span class="sxs-lookup"><span data-stu-id="f1494-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="f1494-131">В раскрывающемся списке **Формат исходных данных** выберите **CSV**.</span><span class="sxs-lookup"><span data-stu-id="f1494-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="f1494-132">Выберите **Отправить и добавить**, выберите CSV-файл, который ранее был сохранен, затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="f1494-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="f1494-133">В диалоговом окне **Добавить файл** выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="f1494-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="f1494-134">На панели операций выберите **Сохранить**, затем выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="f1494-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="f1494-135">В следующем примере изображения показана группа **Экспорт сопоставления Teams** в Commerce с выделенными элементами **Добавить объект** и экспортированными заголовками CSV-файла.</span><span class="sxs-lookup"><span data-stu-id="f1494-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Группа экспорта сопоставлений Teams в Commerce с выделенными элементами добавления объектов и экспортированными заголовками CSV-файла](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="f1494-137">После выполнения описанных выше шагов выполните шаги из раздела [Синхронизация управления задачами между Microsoft Teams и POS-терминалом](synchronize-tasks-teams-pos.md) для синхронизации управления задачами.</span><span class="sxs-lookup"><span data-stu-id="f1494-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="f1494-138">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f1494-138">Additional resources</span></span>

[<span data-ttu-id="f1494-139">Обзор интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f1494-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="f1494-140">Включение интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f1494-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="f1494-141">Подготовка Microsoft Teams из Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f1494-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="f1494-142">Синхронизация управления задачами между Microsoft Teams и Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="f1494-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="f1494-143">Управление ролями пользователей в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f1494-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="f1494-144">Вопросы и ответы по интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f1494-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
