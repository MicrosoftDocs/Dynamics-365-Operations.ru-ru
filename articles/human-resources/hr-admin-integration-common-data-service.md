---
title: Настройка интеграции с Dataverse
description: Можно включать и выключать интеграцию между Microsoft Dataverse и Dynamics 365 Human Resources. Можно также просмотреть сведения о синхронизации, удалить данные отслеживания и повторно синхронизировать таблицу, чтобы помочь в устранении ошибок данных в этих средах.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: 38c42469e62bf5457d0281540325a6c56a5f930f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114046"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="deb3e-104">Настройка интеграции с Dataverse</span><span class="sxs-lookup"><span data-stu-id="deb3e-104">Configure Dataverse integration</span></span>

<span data-ttu-id="deb3e-105">Можно включать и выключать интеграцию между Microsoft Dataverse и Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="deb3e-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="deb3e-106">Можно также просмотреть сведения о синхронизации, удалить данные отслеживания и повторно синхронизировать таблицу, чтобы помочь в устранении ошибок данных в этих средах.</span><span class="sxs-lookup"><span data-stu-id="deb3e-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="deb3e-107">Дополнительные сведения об Dataverse (ранее Common Data Service) и обновлениях терминологии см. в разделе [Что такое Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="deb3e-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="deb3e-108">После отключения интеграции пользователи могут вносить изменения в Human Resources или Dataverse, но эти изменения не синхронизируются между этими двумя средами.</span><span class="sxs-lookup"><span data-stu-id="deb3e-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="deb3e-109">По умолчанию интеграция между Human Resources и Dataverse выключена.</span><span class="sxs-lookup"><span data-stu-id="deb3e-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="deb3e-110">В следующих ситуациях может потребоваться отключить интеграцию:</span><span class="sxs-lookup"><span data-stu-id="deb3e-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="deb3e-111">Данные заполняются с помощью платформы управления данными и должны быть импортированы несколько раз, чтобы перевести их в правильное состояние.</span><span class="sxs-lookup"><span data-stu-id="deb3e-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="deb3e-112">Имеются проблемы, связанные с данными в Human Resources или Dataverse.</span><span class="sxs-lookup"><span data-stu-id="deb3e-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="deb3e-113">Если интеграция отключена, можно удалить запись в одной среде, не удаляя ее в другой.</span><span class="sxs-lookup"><span data-stu-id="deb3e-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="deb3e-114">При повторном включении интеграции запись в среде, в которой она не была удалена, синхронизируется со средой, в которой она была удалена.</span><span class="sxs-lookup"><span data-stu-id="deb3e-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="deb3e-115">Синхронизация начинается при следующем запуске пакетного задания **Синхронизация пропущенных запросов для интеграции Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="deb3e-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="deb3e-116">При отключении интеграции данных убедитесь, что в обеих средах не редактируется одна и та же запись.</span><span class="sxs-lookup"><span data-stu-id="deb3e-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="deb3e-117">При включении интеграции обратно, последняя измененная запись будет синхронизирована.</span><span class="sxs-lookup"><span data-stu-id="deb3e-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="deb3e-118">Таким образом, если изменения в записи в обеих средах не были внесены, может произойти потеря данных.</span><span class="sxs-lookup"><span data-stu-id="deb3e-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="deb3e-119">Доступ к странице интеграции Dataverse</span><span class="sxs-lookup"><span data-stu-id="deb3e-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="deb3e-120">В экземпляре Human Resources, для которого необходимо просмотреть или настроить параметры интеграции с Dataverse, выберите плитку **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="deb3e-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="deb3e-121">[![Плитка администрирования системы](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="deb3e-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="deb3e-122">Выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="deb3e-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="deb3e-123">[![Вкладка ссылок](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="deb3e-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="deb3e-124">В **Интеграции** выберите **конфигурация Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="deb3e-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="deb3e-125">[![Ссылка на конфигурацию Dataverse](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="deb3e-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="deb3e-126">Включение и выключение интеграции между Human Resources и Dataverse</span><span class="sxs-lookup"><span data-stu-id="deb3e-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="deb3e-127">Чтобы включить интеграцию, установите параметр **Разрешить интеграцию с Dataverse** как **Да** на странице **Интеграция Microsoft Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="deb3e-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="deb3e-128">При включении интеграции данные будут синхронизированы при следующем запуске пакетного задания **Синхронизация пропущенных запросов для интеграции Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="deb3e-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="deb3e-129">Все данные должны быть доступны после завершения пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="deb3e-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="deb3e-130">Чтобы отключить интеграцию, установите для параметра значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="deb3e-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="deb3e-131">[![Включение или отключение интеграции Dataverse](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="deb3e-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="deb3e-132">Настоятельно рекомендуется отключить интеграцию Dataverse при выполнении задач переноса данных.</span><span class="sxs-lookup"><span data-stu-id="deb3e-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="deb3e-133">Большие объемы передачи данных могут значительно повлиять на производительность системы.</span><span class="sxs-lookup"><span data-stu-id="deb3e-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="deb3e-134">Например, отправка 2000 работников может занять несколько часов, если интеграция включена, и менее одного часа при отключении.</span><span class="sxs-lookup"><span data-stu-id="deb3e-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="deb3e-135">Представленные в этом примере номера предназначены только для демонстрационных целей.</span><span class="sxs-lookup"><span data-stu-id="deb3e-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="deb3e-136">Точное количество времени, необходимое для импорта записей, может сильно различаться в зависимости от многих факторов.</span><span class="sxs-lookup"><span data-stu-id="deb3e-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="deb3e-137">Просмотр сведений об интеграции данных</span><span class="sxs-lookup"><span data-stu-id="deb3e-137">View data integration details</span></span>

<span data-ttu-id="deb3e-138">На экспресс-вкладке **Администрирование** на странице **Интеграция Microsoft Dataverse** можно увидеть, как взаимосвязаны строки между Human Resources и Dataverse.</span><span class="sxs-lookup"><span data-stu-id="deb3e-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="deb3e-139">Для просмотра строк таблицы выберите таблицу в поле **Таблица Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="deb3e-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="deb3e-140">В сетке отображаются все строки, связанные с выбранной таблицей.</span><span class="sxs-lookup"><span data-stu-id="deb3e-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="deb3e-141">Не все таблицы Dataverse в данный момент перечисляются.</span><span class="sxs-lookup"><span data-stu-id="deb3e-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="deb3e-142">В сетке отображаются только те таблицы, которые поддерживают использование настраиваемых полей.</span><span class="sxs-lookup"><span data-stu-id="deb3e-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="deb3e-143">Новые таблицы становятся доступными через непрерывные выпуски Human Resources.</span><span class="sxs-lookup"><span data-stu-id="deb3e-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="deb3e-144">Сетка содержит следующие поля:</span><span class="sxs-lookup"><span data-stu-id="deb3e-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="deb3e-145">**Таблица Dataverse** — имя таблицы в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="deb3e-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="deb3e-146">**Ссылка на таблицу Dataverse** — идентификатор, используемый Dataverse для идентификации записи.</span><span class="sxs-lookup"><span data-stu-id="deb3e-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="deb3e-147">Это значение аналогично значению **RecID** для Human Resources.</span><span class="sxs-lookup"><span data-stu-id="deb3e-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="deb3e-148">Идентификатор можно найти при открытии таблицы Dataverse в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="deb3e-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="deb3e-149">**Имя объекта Human Resources** — сущность Human Resources, которая последний раз синхронизировала данные с Dataverse.</span><span class="sxs-lookup"><span data-stu-id="deb3e-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="deb3e-150">Объект может иметь либо префикс Dataverse, либо другой префикс.</span><span class="sxs-lookup"><span data-stu-id="deb3e-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="deb3e-151">**Ссылка Human Resources** — значение **RecId**, связанное с записью в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="deb3e-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="deb3e-152">**Удалено из Dataverse** — значение, указывающее, была ли удалена строка из Dataverse.</span><span class="sxs-lookup"><span data-stu-id="deb3e-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="deb3e-153">Записи в Human Resources соответствуют строкам в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="deb3e-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="deb3e-154">Удаление связи записи Human Resources из строки Dataverse</span><span class="sxs-lookup"><span data-stu-id="deb3e-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="deb3e-155">При возникновении проблем с синхронизацией данных в процессе синхронизации между Human Resources и Dataverse можно разрешить их устранение путем очистки отслеживания и повторной синхронизации таблицы отслеживания.</span><span class="sxs-lookup"><span data-stu-id="deb3e-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="deb3e-156">Если удалить связь, а затем изменить или удалить строку в Dataverse, изменения не будут синхронизированы с Human Resources.</span><span class="sxs-lookup"><span data-stu-id="deb3e-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="deb3e-157">При внесении изменений в Human Resources создается новая запись отслеживания и обновляется строка в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="deb3e-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="deb3e-158">Чтобы удалить связь записи Human Resources и строки Dataverse выберите таблицу в поле **Таблица Dataverse**, затем выберите **Удалить информацию отслеживания**.</span><span class="sxs-lookup"><span data-stu-id="deb3e-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="deb3e-159">[![Очистка информации отслеживания](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="deb3e-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="deb3e-160">Чтобы выполнить полную синхронизацию таблицы после очистки отслеживания, см. следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="deb3e-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="deb3e-161">Синхронизация таблицы между Human Resources и Dataverse</span><span class="sxs-lookup"><span data-stu-id="deb3e-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="deb3e-162">Используйте эту процедуру, если:</span><span class="sxs-lookup"><span data-stu-id="deb3e-162">Use this procedure when:</span></span>

- <span data-ttu-id="deb3e-163">Изменения из Dataverse слишком долго не появляются в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="deb3e-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="deb3e-164">После очистки отслеживания необходимо обновить таблицу отслеживания.</span><span class="sxs-lookup"><span data-stu-id="deb3e-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="deb3e-165">Для выполнения полной синхронизации с таблицей между модулем Human Resources и Dataverse:</span><span class="sxs-lookup"><span data-stu-id="deb3e-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="deb3e-166">Выберите таблицу в поле **Таблица Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="deb3e-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="deb3e-167">Выберите **Синхронизировать**.</span><span class="sxs-lookup"><span data-stu-id="deb3e-167">Select **Sync now**.</span></span>

<span data-ttu-id="deb3e-168">[![Выполнение полной синхронизации](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="deb3e-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="deb3e-169">См. также</span><span class="sxs-lookup"><span data-stu-id="deb3e-169">See also</span></span>

[<span data-ttu-id="deb3e-170">Таблицы Dataverse</span><span class="sxs-lookup"><span data-stu-id="deb3e-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="deb3e-171">Настройка виртуальных таблиц Dataverse</span><span class="sxs-lookup"><span data-stu-id="deb3e-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="deb3e-172">Вопросы и ответы по виртуальным таблицам Human Resources</span><span class="sxs-lookup"><span data-stu-id="deb3e-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="deb3e-173">Что такое Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="deb3e-173">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="deb3e-174">Обновления терминологии</span><span class="sxs-lookup"><span data-stu-id="deb3e-174">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
