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
ms.openlocfilehash: d9ee4715526e18b33ae4b7e90b081ed5868bb19c
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527940"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="e616f-104">Настройка интеграции с Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e616f-104">Configure Common Data Service integration</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e616f-105">Можно включать и выключать интеграцию между Common Data Service и Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e616f-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="e616f-106">Можно также просмотреть сведения о синхронизации, удалить данные отслеживания и повторно синхронизировать объект, чтобы помочь в устранении ошибок данных в этих средах.</span><span class="sxs-lookup"><span data-stu-id="e616f-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="e616f-107">После отключения интеграции пользователи могут вносить изменения в Human Resources или Common Data Service, но эти изменения не синхронизируются между этими двумя средами.</span><span class="sxs-lookup"><span data-stu-id="e616f-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="e616f-108">По умолчанию интеграция между Human Resources и Common Data Service выключена.</span><span class="sxs-lookup"><span data-stu-id="e616f-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="e616f-109">В следующих ситуациях может потребоваться отключить интеграцию:</span><span class="sxs-lookup"><span data-stu-id="e616f-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="e616f-110">Данные заполняются с помощью платформы управления данными и должны быть импортированы несколько раз, чтобы перевести их в правильное состояние.</span><span class="sxs-lookup"><span data-stu-id="e616f-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="e616f-111">Имеются проблемы, связанные с данными в Human Resources или Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e616f-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="e616f-112">Если интеграция отключена, можно удалить запись в одной среде, не удаляя ее в другой.</span><span class="sxs-lookup"><span data-stu-id="e616f-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="e616f-113">При повторном включении интеграции запись в среде, в которой она не была удалена, синхронизируется со средой, в которой она была удалена.</span><span class="sxs-lookup"><span data-stu-id="e616f-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="e616f-114">Синхронизация начинается при следующем запуске пакетного задания **Синхронизация пропущенных запросов для интеграции Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="e616f-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="e616f-115">При отключении интеграции данных убедитесь, что в обеих средах не редактируется одна и та же запись.</span><span class="sxs-lookup"><span data-stu-id="e616f-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="e616f-116">При включении интеграции обратно, последняя измененная запись будет синхронизирована.</span><span class="sxs-lookup"><span data-stu-id="e616f-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="e616f-117">Таким образом, если изменения в записи в обеих средах не были внесены, может произойти потеря данных.</span><span class="sxs-lookup"><span data-stu-id="e616f-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="e616f-118">Доступ к странице интеграции Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e616f-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="e616f-119">В экземпляре Human Resources, для которого необходимо просмотреть или настроить параметры интеграции с Common Data Service, выберите плитку **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="e616f-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="e616f-120">[![Плитка администрирования системы](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="e616f-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="e616f-121">Выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="e616f-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="e616f-122">[![Вкладка ссылок](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="e616f-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="e616f-123">В **Интеграции** выберите **конфигурация Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="e616f-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="e616f-124">[![Ссылка на конфигурацию Common Data Service](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="e616f-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="e616f-125">Включение и выключение интеграции между Human Resources и Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e616f-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="e616f-126">Чтобы включить интеграцию, установите параметр **Разрешить интеграцию с Common Data Service** как **Да**.</span><span class="sxs-lookup"><span data-stu-id="e616f-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e616f-127">При включении интеграции данные будут синхронизированы при следующем запуске пакетного задания **Синхронизация пропущенных запросов для интеграции Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="e616f-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="e616f-128">Все данные должны быть доступны после завершения пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="e616f-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="e616f-129">Чтобы отключить интеграцию, установите для параметра значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="e616f-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="e616f-130">[![Включение или отключение интеграции Common Data Service](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="e616f-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

> [!WARNING]
> <span data-ttu-id="e616f-131">Настоятельно рекомендуется отключить интеграцию Common Data Service при выполнении задач переноса данных.</span><span class="sxs-lookup"><span data-stu-id="e616f-131">We strongly recommend turning off Common Data Service integration while performing data migration tasks.</span></span> <span data-ttu-id="e616f-132">Большие объемы передачи данных могут значительно повлиять на производительность системы.</span><span class="sxs-lookup"><span data-stu-id="e616f-132">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="e616f-133">Например, отправка 2000 работников может занять несколько часов, если интеграция включена, и менее одного часа при отключении.</span><span class="sxs-lookup"><span data-stu-id="e616f-133">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="e616f-134">Представленные в этом примере номера предназначены только для демонстрационных целей.</span><span class="sxs-lookup"><span data-stu-id="e616f-134">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="e616f-135">Точное количество времени, необходимое для импорта записей, может сильно различаться в зависимости от многих факторов.</span><span class="sxs-lookup"><span data-stu-id="e616f-135">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="e616f-136">Просмотр сведений об интеграции данных</span><span class="sxs-lookup"><span data-stu-id="e616f-136">View data integration details</span></span>

<span data-ttu-id="e616f-137">На экспресс-вкладке **Администрирование** на странице **Интеграция Common Data Service** можно увидеть, как взаимосвязаны записи между Human Resources и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e616f-137">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="e616f-138">Чтобы просмотреть записи для объекта, выберите объект в поле **Имя объекта CDS**.</span><span class="sxs-lookup"><span data-stu-id="e616f-138">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="e616f-139">В сетке отображаются все записи, связанные с выбранным объектом.</span><span class="sxs-lookup"><span data-stu-id="e616f-139">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="e616f-140">[![Просмотр записей для объекта](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="e616f-140">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="e616f-141">Не все объекты Common Data Service в данный момент перечисляются.</span><span class="sxs-lookup"><span data-stu-id="e616f-141">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="e616f-142">В сетке отображаются только те объекты, которые поддерживают использование настраиваемых полей.</span><span class="sxs-lookup"><span data-stu-id="e616f-142">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="e616f-143">Новые объекты становятся доступными через непрерывные выпуски Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e616f-143">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="e616f-144">Сетка содержит следующие поля:</span><span class="sxs-lookup"><span data-stu-id="e616f-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="e616f-145">**Имя объекта CDS** — имя объекта в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e616f-145">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="e616f-146">**Ссылка на объект CDS** — идентификатор, используемый Common Data Service для идентификации записи.</span><span class="sxs-lookup"><span data-stu-id="e616f-146">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="e616f-147">Это значение аналогично значению **RecID** для Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e616f-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="e616f-148">Идентификатор можно найти при открытии объекта Common Data Service в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="e616f-148">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="e616f-149">**Имя объекта Human Resources** — объект, который последний раз синхронизировал данные с Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e616f-149">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="e616f-150">Объект может иметь либо префикс Common Data Service, либо другой префикс.</span><span class="sxs-lookup"><span data-stu-id="e616f-150">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="e616f-151">**Ссылка Human Resources** — значение **RecId**, связанное с записью в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e616f-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="e616f-152">**Удалено из CDS** — значение, указывающее, была ли удалена запись из Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e616f-152">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="e616f-153">Удаление связи записи в Human Resources из Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e616f-153">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="e616f-154">При возникновении проблем с синхронизацией данных в процессе синхронизации между Human Resources и Common Data Service можно разрешить их устранение путем очистки отслеживания и повторной синхронизации таблицы отслеживания.</span><span class="sxs-lookup"><span data-stu-id="e616f-154">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="e616f-155">Если удалить связь, а затем изменить или удалить запись в Common Data Service, изменения не будут синхронизированы с Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e616f-155">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="e616f-156">При внесении изменений в Human Resources создается новая запись отслеживания и обновляется запись в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e616f-156">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="e616f-157">Чтобы удалить связь записи между Human Resources и Common Data Service выберите объект в поле **Имя объекта CDS**, а затем выберите **Удалить информацию отслеживания**.</span><span class="sxs-lookup"><span data-stu-id="e616f-157">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="e616f-158">[![Очистка информации отслеживания](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="e616f-158">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="e616f-159">Чтобы выполнить полную синхронизацию объекта после очистки отслеживания, см. следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="e616f-159">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="e616f-160">Синхронизация объекта между Human Resources и Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e616f-160">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="e616f-161">Используйте эту процедуру, если:</span><span class="sxs-lookup"><span data-stu-id="e616f-161">Use this procedure when:</span></span>

- <span data-ttu-id="e616f-162">Изменения из Common Data Service слишком долго не появляются в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e616f-162">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="e616f-163">После очистки отслеживания необходимо обновить таблицу отслеживания.</span><span class="sxs-lookup"><span data-stu-id="e616f-163">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="e616f-164">Для выполнения полной синхронизации с объектом между модулем Human Resources и Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="e616f-164">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="e616f-165">Выберите объект в поле **Имя объекта CDS**.</span><span class="sxs-lookup"><span data-stu-id="e616f-165">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="e616f-166">Выберите **Синхронизировать**.</span><span class="sxs-lookup"><span data-stu-id="e616f-166">Select **Sync now**.</span></span>

<span data-ttu-id="e616f-167">[![Выполнение полной синхронизации](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="e616f-167">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


