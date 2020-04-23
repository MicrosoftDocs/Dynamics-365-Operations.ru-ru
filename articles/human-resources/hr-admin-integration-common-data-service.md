---
title: Настройка интеграции с Common Data Service
description: Можно включать и выключать интеграцию между Common Data Service и Dynamics 365 Human Resources. Можно также просмотреть сведения о синхронизации, удалить данные отслеживания и повторно синхронизировать объект, чтобы помочь в устранении ошибок данных в этих средах.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 04280aa0908ed6dab86ef87b6c1843e4b4348e08
ms.sourcegitcommit: c9657b44adb9c1a77c7c2f6ab63a58cc848974ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198430"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="4dca8-104">Настройка интеграции с Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4dca8-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="4dca8-105">Можно включать и выключать интеграцию между Common Data Service и Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4dca8-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="4dca8-106">Можно также просмотреть сведения о синхронизации, удалить данные отслеживания и повторно синхронизировать объект, чтобы помочь в устранении ошибок данных в этих средах.</span><span class="sxs-lookup"><span data-stu-id="4dca8-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="4dca8-107">После отключения интеграции пользователи могут вносить изменения в Human Resources или Common Data Service, но эти изменения не синхронизируются между этими двумя средами.</span><span class="sxs-lookup"><span data-stu-id="4dca8-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="4dca8-108">По умолчанию интеграция между Human Resources и Common Data Service выключена.</span><span class="sxs-lookup"><span data-stu-id="4dca8-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="4dca8-109">В следующих ситуациях может потребоваться отключить интеграцию:</span><span class="sxs-lookup"><span data-stu-id="4dca8-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="4dca8-110">Данные заполняются с помощью платформы управления данными и должны быть импортированы несколько раз, чтобы перевести их в правильное состояние.</span><span class="sxs-lookup"><span data-stu-id="4dca8-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="4dca8-111">Имеются проблемы, связанные с данными в Human Resources или Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4dca8-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="4dca8-112">Если интеграция отключена, можно удалить запись в одной среде, не удаляя ее в другой.</span><span class="sxs-lookup"><span data-stu-id="4dca8-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="4dca8-113">При повторном включении интеграции запись в среде, в которой она не была удалена, синхронизируется со средой, в которой она была удалена.</span><span class="sxs-lookup"><span data-stu-id="4dca8-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="4dca8-114">Синхронизация начинается при следующем запуске пакетного задания **Синхронизация пропущенных запросов для интеграции Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="4dca8-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="4dca8-115">При отключении интеграции данных убедитесь, что в обеих средах не редактируется одна и та же запись.</span><span class="sxs-lookup"><span data-stu-id="4dca8-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="4dca8-116">При включении интеграции обратно, последняя измененная запись будет синхронизирована.</span><span class="sxs-lookup"><span data-stu-id="4dca8-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="4dca8-117">Таким образом, если изменения в записи в обеих средах не были внесены, может произойти потеря данных.</span><span class="sxs-lookup"><span data-stu-id="4dca8-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="4dca8-118">Доступ к странице интеграции Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4dca8-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="4dca8-119">В экземпляре Human Resources, для которого необходимо просмотреть или настроить параметры интеграции с Common Data Service, выберите плитку **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="4dca8-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="4dca8-120">[![Плитка администрирования системы](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="4dca8-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="4dca8-121">Выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="4dca8-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="4dca8-122">[![Вкладка ссылок](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="4dca8-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="4dca8-123">В **Интеграции** выберите **конфигурация Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="4dca8-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="4dca8-124">[![Ссылка на конфигурацию Common Data Service](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="4dca8-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="4dca8-125">Включение и выключение интеграции между Human Resources и Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4dca8-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="4dca8-126">Чтобы включить интеграцию, установите параметр **Разрешить интеграцию с Common Data Service** как **Да**.</span><span class="sxs-lookup"><span data-stu-id="4dca8-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4dca8-127">При включении интеграции данные будут синхронизированы при следующем запуске пакетного задания **Синхронизация пропущенных запросов для интеграции Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="4dca8-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="4dca8-128">Все данные должны быть доступны после завершения пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="4dca8-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="4dca8-129">Чтобы отключить интеграцию, установите для параметра значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="4dca8-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="4dca8-130">[![Включение или отключение интеграции Common Data Service](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="4dca8-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="4dca8-131">Просмотр сведений об интеграции данных</span><span class="sxs-lookup"><span data-stu-id="4dca8-131">View data integration details</span></span>

<span data-ttu-id="4dca8-132">На экспресс-вкладке **Администрирование** на странице **Интеграция Common Data Service** можно увидеть, как взаимосвязаны записи между Human Resources и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4dca8-132">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="4dca8-133">Чтобы просмотреть записи для объекта, выберите объект в поле **Имя объекта CDS**.</span><span class="sxs-lookup"><span data-stu-id="4dca8-133">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="4dca8-134">В сетке отображаются все записи, связанные с выбранным объектом.</span><span class="sxs-lookup"><span data-stu-id="4dca8-134">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="4dca8-135">[![Просмотр записей для объекта](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="4dca8-135">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="4dca8-136">Не все объекты Common Data Service в данный момент перечисляются.</span><span class="sxs-lookup"><span data-stu-id="4dca8-136">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="4dca8-137">В сетке отображаются только те объекты, которые поддерживают использование настраиваемых полей.</span><span class="sxs-lookup"><span data-stu-id="4dca8-137">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="4dca8-138">Новые объекты становятся доступными через непрерывные выпуски Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4dca8-138">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="4dca8-139">Сетка содержит следующие поля:</span><span class="sxs-lookup"><span data-stu-id="4dca8-139">The grid includes the following fields:</span></span>

- <span data-ttu-id="4dca8-140">**Имя объекта CDS** — имя объекта в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4dca8-140">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="4dca8-141">**Ссылка на объект CDS** — идентификатор, используемый Common Data Service для идентификации записи.</span><span class="sxs-lookup"><span data-stu-id="4dca8-141">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="4dca8-142">Это значение аналогично значению **RecID** для Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4dca8-142">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="4dca8-143">Идентификатор можно найти при открытии объекта Common Data Service в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4dca8-143">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="4dca8-144">**Имя объекта Human Resources** — объект, который последний раз синхронизировал данные с Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4dca8-144">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="4dca8-145">Объект может иметь либо префикс Common Data Service, либо другой префикс.</span><span class="sxs-lookup"><span data-stu-id="4dca8-145">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="4dca8-146">**Ссылка Human Resources** — значение **RecId**, связанное с записью в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4dca8-146">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="4dca8-147">**Удалено из CDS** — значение, указывающее, была ли удалена запись из Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4dca8-147">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="4dca8-148">Удаление связи записи в Human Resources из Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4dca8-148">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="4dca8-149">При возникновении проблем с синхронизацией данных в процессе синхронизации между Human Resources и Common Data Service можно разрешить их устранение путем очистки отслеживания и повторной синхронизации таблицы отслеживания.</span><span class="sxs-lookup"><span data-stu-id="4dca8-149">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="4dca8-150">Если удалить связь, а затем изменить или удалить запись в Common Data Service, изменения не будут синхронизированы с Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4dca8-150">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="4dca8-151">При внесении изменений в Human Resources создается новая запись отслеживания и обновляется запись в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4dca8-151">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="4dca8-152">Чтобы удалить связь записи между Human Resources и Common Data Service выберите объект в поле **Имя объекта CDS**, а затем выберите **Удалить информацию отслеживания**.</span><span class="sxs-lookup"><span data-stu-id="4dca8-152">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="4dca8-153">[![Очистка информации отслеживания](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="4dca8-153">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="4dca8-154">Чтобы выполнить полную синхронизацию объекта после очистки отслеживания, см. следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="4dca8-154">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="4dca8-155">Синхронизация объекта между Human Resources и Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4dca8-155">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="4dca8-156">Используйте эту процедуру, если:</span><span class="sxs-lookup"><span data-stu-id="4dca8-156">Use this procedure when:</span></span>

- <span data-ttu-id="4dca8-157">Изменения из Common Data Service слишком долго не появляются в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4dca8-157">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="4dca8-158">После очистки отслеживания необходимо обновить таблицу отслеживания.</span><span class="sxs-lookup"><span data-stu-id="4dca8-158">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="4dca8-159">Для выполнения полной синхронизации с объектом между модулем Human Resources и Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="4dca8-159">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="4dca8-160">Выберите объект в поле **Имя объекта CDS**.</span><span class="sxs-lookup"><span data-stu-id="4dca8-160">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="4dca8-161">Выберите **Синхронизировать**.</span><span class="sxs-lookup"><span data-stu-id="4dca8-161">Select **Sync now**.</span></span>

<span data-ttu-id="4dca8-162">[![Выполнение полной синхронизации](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="4dca8-162">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


