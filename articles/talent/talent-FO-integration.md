---
title: Вопросы и ответы по интеграции Dynamics 365 Talent с Dynamics 365 Finance
description: В этом разделе объясняется, какие данные синхронизируются в интеграции Talent и Finance.
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5bb855e6dd7ff236b7bda9e59e12ed8cc8ab9bc9
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251023"
---
# <a name="dynamics-365-talent-to-dynamics-365-finance-integration-faq"></a><span data-ttu-id="7c278-103">Вопросы и ответы по интеграции Dynamics 365 Talent с Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="7c278-103">Dynamics 365 Talent to Dynamics 365 Finance integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7c278-104">В этом разделе содержатся ответы на часто задаваемые вопросы, связанные с тем, какие данные синхронизируются в случае интеграции Dynamics 365 Talent с Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="7c278-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Talent is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="7c278-105">Синхронизируются все данные или только некоторые информационные объекты?</span><span class="sxs-lookup"><span data-stu-id="7c278-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="7c278-106">Для Core HR синхронизируется подмножество данных.</span><span class="sxs-lookup"><span data-stu-id="7c278-106">For Core HR, a subset of the data is synchronized.</span></span> <span data-ttu-id="7c278-107">Список всех сущностей см. в разделе [Интеграции из Dynamics 365 Talent в Dynamics 365 Finance](talent-financeandoperations-integration.md).</span><span class="sxs-lookup"><span data-stu-id="7c278-107">For a list of all the entities, see [Integration from Dynamics 365 Talent to Dynamics 365 Finance](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="7c278-108">Для Attract и Onboard все данные являются собственными для Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7c278-108">For Attract and Onboard, all data is native to Common Data Service.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="7c278-109">Можно ли создать новое сопоставление без использования шаблонов?</span><span class="sxs-lookup"><span data-stu-id="7c278-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="7c278-110">Шаблоны являются отправной точкой.</span><span class="sxs-lookup"><span data-stu-id="7c278-110">Templates are the starting point.</span></span> <span data-ttu-id="7c278-111">Можно создать собственный шаблон, но всегда требуется шаблон при создании проекта интеграции.</span><span class="sxs-lookup"><span data-stu-id="7c278-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="7c278-112">Дополнительные сведения об интеграторе данных (DI), шаблонах и проектах см. в разделе [Интеграция данных в Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="7c278-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance"></a><span data-ttu-id="7c278-113">Можно ли сопоставить финансовые аналитики для перемещения между Talent и Finance?</span><span class="sxs-lookup"><span data-stu-id="7c278-113">Can I map financial dimensions to transfer between Talent and Finance?</span></span>

<span data-ttu-id="7c278-114">Финансовые аналитики в настоящее время не находятся в Common Data Service для приложений и, в результате, не являются частью шаблона по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7c278-114">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="7c278-115">Эта сущность запланирована, но в настоящее время не известно, когда она будет выпущена.</span><span class="sxs-lookup"><span data-stu-id="7c278-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="7c278-116">Для данных, которые расположены в Finance, но не существуют в Talent, свяжите две системы вместе с помощью **Настроить ссылки** в Talent.</span><span class="sxs-lookup"><span data-stu-id="7c278-116">For data that resides in Finance but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="7c278-117">Дополнительные сведения о настройке связей между Talent и Finance см. в разделе [Что нового и что изменилось в Dynamics 365 Talent: Core HR (31 октября 2018 г.)](whats-new-talent-october-31.md).</span><span class="sxs-lookup"><span data-stu-id="7c278-117">For more information about how to configure links between Talent and Finance, see [What's new or changed in Dynamics 365 Talent: Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![Сопоставление финансовых аналитик](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="7c278-119">Иногда при импорте сотрудников они перемещаются в неактивных работников в Finance.</span><span class="sxs-lookup"><span data-stu-id="7c278-119">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="7c278-120">Почему?</span><span class="sxs-lookup"><span data-stu-id="7c278-120">Why?</span></span>

<span data-ttu-id="7c278-121">Данная ошибка может возникать, если у сотрудников нет активной записи сведений о приеме на работу в Talent.</span><span class="sxs-lookup"><span data-stu-id="7c278-121">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="7c278-122">Чтобы решить эту проблему, откройте **Управление персоналом \> Сотрудники \> История занятости \> Диспетчер дат**и убедитесь, что имеется активная запись данных о приеме на работу.</span><span class="sxs-lookup"><span data-stu-id="7c278-122">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="7c278-123">Если я выбрал сопоставить только подмножество полей, изменений, будут ли изменения, внесенные в несопоставленные поля, вызывать синхронизацию?</span><span class="sxs-lookup"><span data-stu-id="7c278-123">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="7c278-124">Синхронизация данных производится в соответствии с графиком выполнения.</span><span class="sxs-lookup"><span data-stu-id="7c278-124">Data sync follows the execution schedule.</span></span> <span data-ttu-id="7c278-125">Интеграция выберет запись, если любое поле в записи было изменено, независимо от того, является ли это поле частью сопоставления интеграции.</span><span class="sxs-lookup"><span data-stu-id="7c278-125">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="7c278-126">Как отправить только изменения активных рабочих, но не завершенные записи?</span><span class="sxs-lookup"><span data-stu-id="7c278-126">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="7c278-127">С помощью функции "Расширенный запрос" можно фильтровать и формировать исходные данные перед передачей их в место назначения.</span><span class="sxs-lookup"><span data-stu-id="7c278-127">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Расширенный запрос активных работников](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="7c278-129">Можно ли указать поля, которые передаются в Finance, для конкретной сущности?</span><span class="sxs-lookup"><span data-stu-id="7c278-129">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="7c278-130">Поля можно добавлять или удалять из задачи интеграции.</span><span class="sxs-lookup"><span data-stu-id="7c278-130">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="7c278-131">Не все поля данных, которые существуют в сущности Common Data Service будет заполняться из Core HR.</span><span class="sxs-lookup"><span data-stu-id="7c278-131">Not all data fields that exist on the Common Data Service entity will be populated from Core HR.</span></span>
<span data-ttu-id="7c278-132">Дополнительные данные могут заполняться через PowerApps.</span><span class="sxs-lookup"><span data-stu-id="7c278-132">Additional data can be populated via PowerApps.</span></span>

![Добавление полей в задачу интеграции и удаление полей из задачи интеграции](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="7c278-134">Я настроил интеграцию как пакетное задание, но Talent потерял подключение к системе назначения.</span><span class="sxs-lookup"><span data-stu-id="7c278-134">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="7c278-135">Как можно отправить этот же набор изменений в систему назначения?</span><span class="sxs-lookup"><span data-stu-id="7c278-135">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="7c278-136">Специальная настройка для обработки исключений не требуется.</span><span class="sxs-lookup"><span data-stu-id="7c278-136">No special setup is required for exception handling.</span></span> <span data-ttu-id="7c278-137">Интегратор данных автоматически перехватывает ошибки, которые произошли в источнике или пункте назначения, сообщает о них и позволяет выполнить повторные попытки вручную.</span><span class="sxs-lookup"><span data-stu-id="7c278-137">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="7c278-138">Однако это не обеспечивает ручной коррекции данных.</span><span class="sxs-lookup"><span data-stu-id="7c278-138">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="7c278-139">Если требуются обновления данных, это должно быть выполнено как в источнике, так и в месте назначения.</span><span class="sxs-lookup"><span data-stu-id="7c278-139">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="7c278-140">Как можно настроить двунаправленную интеграцию?</span><span class="sxs-lookup"><span data-stu-id="7c278-140">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="7c278-141">Нет, в настоящее время интеграция работает в одну сторону (из Talent в Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="7c278-141">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="7c278-142">Тем не менее, существует шаблон по умолчанию для отправки данных из Talent в Finance.</span><span class="sxs-lookup"><span data-stu-id="7c278-142">However, there is a default template available to send data from Talent to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="7c278-143">Можно ли разрешить удаление записи как часть моей интеграции?</span><span class="sxs-lookup"><span data-stu-id="7c278-143">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="7c278-144">Нет, интегратор данных не будут регистрировать удаленные записи для переноса данных.</span><span class="sxs-lookup"><span data-stu-id="7c278-144">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="7c278-145">Только создание данных и обновления (UPSERT) входят в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="7c278-145">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="7c278-146">Можно ли повторно выполнить поврежденное выполнение?</span><span class="sxs-lookup"><span data-stu-id="7c278-146">Can I rerun the errored execution?</span></span> <span data-ttu-id="7c278-147">Если да, будет ли отправлен полный файл или только изменения?</span><span class="sxs-lookup"><span data-stu-id="7c278-147">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="7c278-148">Первый запуск интегратора данных всегда является полным запуском.</span><span class="sxs-lookup"><span data-stu-id="7c278-148">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="7c278-149">Последующие запуски основаны на отслеживании изменений.</span><span class="sxs-lookup"><span data-stu-id="7c278-149">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="7c278-150">В случае выполнения с ошибками извлекаются записи в области выполнения и отправляются самые последние изменения из Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7c278-150">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="7c278-151">При сохранении проекта появилось сообщение об ошибке: "Проект имеет ошибки сопоставления".</span><span class="sxs-lookup"><span data-stu-id="7c278-151">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="7c278-152">Что делать?</span><span class="sxs-lookup"><span data-stu-id="7c278-152">What do I do?</span></span>

<span data-ttu-id="7c278-153">Проверьте настройку интеграционных ключей, внесите все требуемые изменения в настройку, затем обновите сущности в проекте.</span><span class="sxs-lookup"><span data-stu-id="7c278-153">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="7c278-154">При использовании шаблона по умолчанию интеграционные ключи будут импортированы автоматически.</span><span class="sxs-lookup"><span data-stu-id="7c278-154">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="7c278-155">Эта проблема может возникнуть при добавлении новой задачи к существующему шаблону.</span><span class="sxs-lookup"><span data-stu-id="7c278-155">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="7c278-156">Если имеется N юридических лиц, в которых сотрудники имеют занятость, нужно ли создать сопоставление для каждого из них?</span><span class="sxs-lookup"><span data-stu-id="7c278-156">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="7c278-157">Да, для каждого юридического лица в Finance необходим отдельный проект интеграции в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="7c278-157">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="7c278-158">Требуется перенести данные, которые не являются частью шаблона по умолчанию, предоставленного корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7c278-158">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="7c278-159">Можно сделать это?</span><span class="sxs-lookup"><span data-stu-id="7c278-159">Can I do this?</span></span>

<span data-ttu-id="7c278-160">Да, поля можно добавить в существующий шаблон или удалить их из него.</span><span class="sxs-lookup"><span data-stu-id="7c278-160">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="7c278-161">Можно изменить шаблон для включения дополнительных данных из других сущностей Common Data Service для приложений.</span><span class="sxs-lookup"><span data-stu-id="7c278-161">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="7c278-162">Сущность должна находиться в Common Data Service для приложений, чтобы ее можно было включить в шаблон.</span><span class="sxs-lookup"><span data-stu-id="7c278-162">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="7c278-163">Я только что создал новые среды Finance и Talent и получил ошибку "Значение данных нарушает ограничения целостности".</span><span class="sxs-lookup"><span data-stu-id="7c278-163">I just created new Finance and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="7c278-164">Почему?</span><span class="sxs-lookup"><span data-stu-id="7c278-164">Why?</span></span>

<span data-ttu-id="7c278-165">Причины этой ошибки могут быть следующими:</span><span class="sxs-lookup"><span data-stu-id="7c278-165">Reasons for this error can include:</span></span>

- <span data-ttu-id="7c278-166">Передача данных привела к извлечению дублирующихся записей в источнике (Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="7c278-166">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="7c278-167">Перемещение данных содержит значения NULL для полей, которые необходимы в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7c278-167">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="7c278-168">Проверьте данные в Common Data Service и обеспечьте соответствие требованиям Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7c278-168">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="7c278-169">Если имеются ошибки выполнения и код сотрудника не синхронизируется, как найти старое задание, которое содержит сбойную запись сотрудника?</span><span class="sxs-lookup"><span data-stu-id="7c278-169">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="7c278-170">Интегратор данных создаст несколько проектов в Finance.</span><span class="sxs-lookup"><span data-stu-id="7c278-170">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="7c278-171">Связь между задачей интегратора данных и проектом Finance будет один к одному.</span><span class="sxs-lookup"><span data-stu-id="7c278-171">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="7c278-172">Отследите время из журнала выполнения интегратора данных и найдите проект индекс -1 в Finance.</span><span class="sxs-lookup"><span data-stu-id="7c278-172">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="7c278-173">Если номер задачи равен 9 в интеграторе данных, индекс в Finance — 8.</span><span class="sxs-lookup"><span data-stu-id="7c278-173">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="7c278-174">Запишите индекс задачи из интегратора данных (в этом примере это "9").</span><span class="sxs-lookup"><span data-stu-id="7c278-174">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![Запись индекса задачи из интегратора данных](media/CaptureTaskIndex.png)

2. <span data-ttu-id="7c278-176">Отследите время выполнения проекта.</span><span class="sxs-lookup"><span data-stu-id="7c278-176">Track the execution time of the project.</span></span>

![Отслеживание времени выполнения проекта](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="7c278-178">В Finance укажите индекс — 1.</span><span class="sxs-lookup"><span data-stu-id="7c278-178">In Finance, identify index - 1.</span></span> <span data-ttu-id="7c278-179">В этом примере проект с суффиксом "8" и временем выполнения проекта с индексом "0" совпадает со времени выполнения на этапе 2.</span><span class="sxs-lookup"><span data-stu-id="7c278-179">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![Определение индекса](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-i-dont-see-my-talent-data-in-finance-what-do-i-do"></a><span data-ttu-id="7c278-181">После интеграции Talent и Finance я не вижу свои данные Talent в Finance.</span><span class="sxs-lookup"><span data-stu-id="7c278-181">After integrating Talent and Finance, I don’t see my Talent data in Finance.</span></span> <span data-ttu-id="7c278-182">Что делать?</span><span class="sxs-lookup"><span data-stu-id="7c278-182">What do I do?</span></span>

<span data-ttu-id="7c278-183">Интеграция с Finance осуществляется в два этапа.</span><span class="sxs-lookup"><span data-stu-id="7c278-183">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="7c278-184">Во-первых убедитесь, что данные Talent обновлены и доступны в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7c278-184">First, verify that the Talent data is updated and available in Common Data Service.</span></span> <span data-ttu-id="7c278-185">Это синхронизация почти в реальном времени, и ее можно проверить в PowerApps, просмотрев данные в информационных объектах.</span><span class="sxs-lookup"><span data-stu-id="7c278-185">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![Данные в Common Data Service](media/DataInCDS.png)

<span data-ttu-id="7c278-187">Если данные не отображаются должным образом в Common Data Service, убедитесь, что сущность поддерживается в интеграции.</span><span class="sxs-lookup"><span data-stu-id="7c278-187">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="7c278-188">Чтобы включить дополнительные данные в Common Data Service, изменение будет требоваться со стороны корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7c278-188">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="7c278-189">Если сущность поддерживается и данные доступны в Common Data Service, проверьте правильность сопоставления в интеграторе данных.</span><span class="sxs-lookup"><span data-stu-id="7c278-189">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="7c278-190">Если сопоставление интегратора выглядит правильным, затем проверьте успешность выполнения заданий управления данными.</span><span class="sxs-lookup"><span data-stu-id="7c278-190">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="7c278-191">Ошибки могут возникать при выполнении пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="7c278-191">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="7c278-192">Дополнительные сведения об управлении данными см. в разделе [Управление данными](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7c278-192">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="7c278-193">Адреса моих сотрудников неправильные после импорта в Finance.</span><span class="sxs-lookup"><span data-stu-id="7c278-193">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="7c278-194">Что делать?</span><span class="sxs-lookup"><span data-stu-id="7c278-194">What should I do?</span></span>

<span data-ttu-id="7c278-195">Номерная серия для параметра **Код местоположения** использует одинаковый шаблон в Talent и Finance.</span><span class="sxs-lookup"><span data-stu-id="7c278-195">The number sequence for **Location ID** uses the same pattern in both Talent and Finance.</span></span> <span data-ttu-id="7c278-196">Номерная серия должна быть уникальной на обеих сторонах, поэтому нет конфликтов адресов при интеграции данных из Common Data Service в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7c278-196">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="7c278-197">Во время реализации Talent убедитесь, что номерные серии не одинаковы в Talent и Finance.</span><span class="sxs-lookup"><span data-stu-id="7c278-197">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance.</span></span> <span data-ttu-id="7c278-198">Проверьте, что все номерные серии не идентичны там, где данные могут поддерживаться в обеих системах.</span><span class="sxs-lookup"><span data-stu-id="7c278-198">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="7c278-199">При создании моего набора подключения я не вижу подключение в раскрывающемся списке подключения.</span><span class="sxs-lookup"><span data-stu-id="7c278-199">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="7c278-200">Что делать?</span><span class="sxs-lookup"><span data-stu-id="7c278-200">What do I do?</span></span>

<span data-ttu-id="7c278-201">Убедитесь, что при создании подключений выбраны Dynamics 365 Finance и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7c278-201">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="7c278-202">При синхронизации занятости возникают ошибки «CompanyInfo_FK не существует» или «Значение "31.12.2154 23:59:59" в поле "Дата окончания занятости" не найдено в связанной таблице "Занятость"». Что делать?</span><span class="sxs-lookup"><span data-stu-id="7c278-202">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="7c278-203">Убедитесь, что сопоставляются правильные юридические лица.</span><span class="sxs-lookup"><span data-stu-id="7c278-203">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="7c278-204">Синхронизация юридических лиц не является частью шаблона по умолчанию, поэтому ожидается, что каждое юридическое лицо, которое присутствует в Talent и Common Data Service, также присутствует в Finance.</span><span class="sxs-lookup"><span data-stu-id="7c278-204">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="7c278-205">Кроме того, убедитесь, что выбраны правильные юридические лица для связанного набора соединений.</span><span class="sxs-lookup"><span data-stu-id="7c278-205">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="7c278-206">После настройки проекта сопоставление полей для Finance выглядит пустым.</span><span class="sxs-lookup"><span data-stu-id="7c278-206">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="7c278-207">Что делать?</span><span class="sxs-lookup"><span data-stu-id="7c278-207">What should I do?</span></span>

<span data-ttu-id="7c278-208">Обновите информационные объекты в Finance, перейдя в **Управление данными \> Параметры структуры \> Параметры объекта \> Обновить список объектов**.</span><span class="sxs-lookup"><span data-stu-id="7c278-208">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="7c278-209">Данная процедура займет несколько минут, затем вы должны увидеть эти сопоставления.</span><span class="sxs-lookup"><span data-stu-id="7c278-209">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="7c278-210">Эта проблема возникает при создании новых проектов.</span><span class="sxs-lookup"><span data-stu-id="7c278-210">This issue occurs when new projects are created.</span></span>

![Отсутствует сопоставление полей](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="7c278-212">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7c278-212">Additional resources</span></span>

- <span data-ttu-id="7c278-213">Интегратор данных (DI):</span><span class="sxs-lookup"><span data-stu-id="7c278-213">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="7c278-214">Интеграция данных в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7c278-214">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="7c278-215">Управление ошибками и устранение неполадок интегратора данных</span><span class="sxs-lookup"><span data-stu-id="7c278-215">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="7c278-216">Ответ на запросы DSR для созданных системой журналов в PowerApps, Microsoft Flow и Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7c278-216">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="7c278-217">Управление данными:</span><span class="sxs-lookup"><span data-stu-id="7c278-217">Data Management:</span></span>

  - [<span data-ttu-id="7c278-218">Управление данными</span><span class="sxs-lookup"><span data-stu-id="7c278-218">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
