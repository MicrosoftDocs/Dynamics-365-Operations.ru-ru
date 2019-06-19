---
title: Расширение Talent с помощью PowerApps и Microsoft Flow — примеры сценариев
description: В этой теме описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 for Talent, использующих Microsoft PowerApps и Microsoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: a9ebfd1f2621b8ad65d7623c37b6851cc0b5cb54
ms.sourcegitcommit: ffc37f7c2a63bada3055f37856a30424040bc9a3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/16/2019
ms.locfileid: "1577803"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="23b74-103">Расширение Talent с помощью PowerApps и Microsoft Flow — примеры сценариев</span><span class="sxs-lookup"><span data-stu-id="23b74-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="23b74-104">В этой теме описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 for Talent, использующих Microsoft PowerApps и Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="23b74-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="23b74-105">Можно импортировать пакет решения, связанный с каждым примером, в среду PowerApps.</span><span class="sxs-lookup"><span data-stu-id="23b74-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="23b74-106">Затем можно использовать эти пакеты как руководство или как основу для реализации сценариев, которые применимы к вашей организации.</span><span class="sxs-lookup"><span data-stu-id="23b74-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23b74-107">Если вы хотите использовать шаблоны и приложения, описанные в этом разделе, "как есть", обязательно проверьте их, чтобы убедиться в том, что они охватывают все сценарии, относящиеся к вашей реализации.</span><span class="sxs-lookup"><span data-stu-id="23b74-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="23b74-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="23b74-108">Prerequisites</span></span>

- <span data-ttu-id="23b74-109">Для импорта пакетов пользователи должны иметь разрешение **Создатель среды**.</span><span class="sxs-lookup"><span data-stu-id="23b74-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="23b74-110">Для экспорта или импорта приложений пользователи должны иметь лицензию плана 2 PowerApps или пробную лицензию плана 2 PowerApps.</span><span class="sxs-lookup"><span data-stu-id="23b74-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="23b74-111">Поток — подключение формы</span><span class="sxs-lookup"><span data-stu-id="23b74-111">Flow – Form Connect</span></span>

<span data-ttu-id="23b74-112">Шаблон **Поток — подключение формы** можно использовать для чтения данных из Microsoft Forms и сохранения их в объекте Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="23b74-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="23b74-113">Этот шаблон можно расширить таким образом, чтобы его можно было использовать для других сценариев.</span><span class="sxs-lookup"><span data-stu-id="23b74-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="23b74-114">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="23b74-114">Here are some examples:</span></span>

- <span data-ttu-id="23b74-115">Запись оценок кандидатов.</span><span class="sxs-lookup"><span data-stu-id="23b74-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="23b74-116">Запись результатов из анкет для курса.</span><span class="sxs-lookup"><span data-stu-id="23b74-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="23b74-117">Компиляция библиотеки вопросов собеседования для администраторов отдела кадров (HR).</span><span class="sxs-lookup"><span data-stu-id="23b74-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="23b74-118">Запись оценки кандидатом процесса собеседования</span><span class="sxs-lookup"><span data-stu-id="23b74-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="23b74-119">В Microsoft Dynamics 365: Attract формы могут отображаться на портале кандидата, и кандидаты могут заполнять сведения.</span><span class="sxs-lookup"><span data-stu-id="23b74-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="23b74-120">Формы можно также внедрить как действия в шаблон должности.</span><span class="sxs-lookup"><span data-stu-id="23b74-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="23b74-121">Когда кандидат отправляет форму, Microsoft Flow записывает отправку формы, считывает данные и сохраняет их в объекте Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="23b74-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="23b74-122">Для загрузки шаблона **Поток — подключение формы** и структуры пользовательского объекта, перейдите к [Поток — подключение формы](https://go.microsoft.com/fwlink/?linkid=2081988) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="23b74-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="23b74-123">Инициализация и извлечение параметров, переданных в PowerApps</span><span class="sxs-lookup"><span data-stu-id="23b74-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="23b74-124">Шаблон **Инициализация и извлечение параметров, переданных в PowerApps** можно использовать в качестве отправной точки для любого сценария PowerApps, который связан с Attract.</span><span class="sxs-lookup"><span data-stu-id="23b74-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="23b74-125">Он включает все параметры по умолчанию, передаваемые приложением Attract, такие как **Заявление о приеме на работу**, **Код кандидата** и **JobID**.</span><span class="sxs-lookup"><span data-stu-id="23b74-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="23b74-126">Этот шаблон может использоваться для извлечения формы оценки кандидата, чтобы менеджер по найму мог просмотреть оценку, указанную кандидатом.</span><span class="sxs-lookup"><span data-stu-id="23b74-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="23b74-127">Приложения, которые созданы с помощью PowerApps могут быть встроены в шаблон должности в Attract.</span><span class="sxs-lookup"><span data-stu-id="23b74-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="23b74-128">Чтобы загрузить шаблон **Инициализация и извлечение параметров, переданных в PowerApps** и структуру пользовательского объекта, перейдите к шаблону [Инициализация и извлечение параметров, переданных в PowerApps](https://go.microsoft.com/fwlink/?linkid=2081991) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="23b74-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="23b74-129">Интеграция с Office 365</span><span class="sxs-lookup"><span data-stu-id="23b74-129">Integration with Office 365</span></span>

<span data-ttu-id="23b74-130">Приложение **Интеграция с Office 365** может использоваться для извлечения сведений о рабочей группе для выполнивших вход пользователей из Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="23b74-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="23b74-131">Оно ссылается на работников в Talent для извлечения сведений о времени прихода и ухода и записей исключения.</span><span class="sxs-lookup"><span data-stu-id="23b74-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="23b74-132">Сведения о времени прихода и ухода хранятся в настраиваемых объектах Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="23b74-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="23b74-133">Предполагается, что эти сведения заполняются из систем других производителей путем интеграции.</span><span class="sxs-lookup"><span data-stu-id="23b74-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="23b74-134">Это приложение можно расширить таким образом, чтобы его можно было использовать для других сценариев.</span><span class="sxs-lookup"><span data-stu-id="23b74-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="23b74-135">Например, оно может использоваться для отображения сведений об отпусках рабочей группы, события календаря и любых других событиях, связанных с рабочей группой.</span><span class="sxs-lookup"><span data-stu-id="23b74-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="23b74-136">Чтобы загрузить приложение **Интеграция с Office 365** и структуру пользовательского объекта, перейдите к приложению [Интеграция с Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="23b74-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="23b74-137">Поток — уведомление по электронной почте</span><span class="sxs-lookup"><span data-stu-id="23b74-137">Flow – Email Notification</span></span>

<span data-ttu-id="23b74-138">Шаблон **Поток — уведомление по электронной почте** можно использовать для сценариев уведомления по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="23b74-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="23b74-139">Он может использоваться для выдачи сообщений по электронной почте для кандидатов, которых рабочая группа найма на работу отклоняет на любом этапе процесса набора сотрудников.</span><span class="sxs-lookup"><span data-stu-id="23b74-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="23b74-140">Этот шаблон может быть расширен для отслеживания изменений этапа кандидата в процессе набора персонала и для отправки уведомлений рабочей группе найма сотрудников и кандидату.</span><span class="sxs-lookup"><span data-stu-id="23b74-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="23b74-141">В общем случае для объектов, которые хранятся в Common Data Service, потоки можно настроить для отправки уведомлений о событиях, происходящих в Core HR, Attract или Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="23b74-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="23b74-142">Чтобы загрузить шаблон **Поток — уведомление по электронной почте**, выберите [Поток — уведомление по электронной почте](https://go.microsoft.com/fwlink/?linkid=2082103) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="23b74-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="23b74-143">Поток — подключение и выполнение SQL</span><span class="sxs-lookup"><span data-stu-id="23b74-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="23b74-144">Шаблон **Поток — подключение и выполнение SQL** подключается к Microsoft SQL Server и позволяет выполнять запросы SQL.</span><span class="sxs-lookup"><span data-stu-id="23b74-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="23b74-145">Несмотря на то, что этот шаблон предназначен для чтения и обновления таблиц SQL, его можно расширить, чтобы его можно было использовать для других сценариев.</span><span class="sxs-lookup"><span data-stu-id="23b74-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="23b74-146">Например, он может использоваться для заполнения промежуточной таблицы в Common Data Service с записями из SQL Server, а также для периодической синхронизации промежуточной таблицы с помощью инкрементной принудительной отправки из SQL Server.</span><span class="sxs-lookup"><span data-stu-id="23b74-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="23b74-147">Для загрузки шаблона **Поток — подключение и выполнение SQL** перейдите к пункту [Поток — подключение и выполнение SQL](https://go.microsoft.com/fwlink/?linkid=2081789) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="23b74-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="23b74-148">Поток — интеграция с SharePoint</span><span class="sxs-lookup"><span data-stu-id="23b74-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="23b74-149">Шаблон **Поток — интеграция с SharePoint** шаблон может использоваться для чтения данных из списка Microsoft SharePoint, сравнения списка со значениями полей для любого объекта Common Data Service и отправить результаты сравнения в виде уведомления по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="23b74-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="23b74-150">Организация может иметь набор навыков, которые требуются срочно.</span><span class="sxs-lookup"><span data-stu-id="23b74-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="23b74-151">Эти навыки могут храниться в SharePoint в виде списка SharePoint.</span><span class="sxs-lookup"><span data-stu-id="23b74-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="23b74-152">Когда кандидат подает заявление для любой должности, для которой перечислен набор необходимых навыков, если существует значительное соответствие между навыками кандидата и навыками, которые хранятся в SharePoint, отправляется уведомление по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="23b74-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="23b74-153">Таким образом должности, которые требуются срочно, заполняются быстрее, поскольку уведомления помогают агентам по найму связываться с кандидатами и выполнять кросс-наем кандидатов в организации.</span><span class="sxs-lookup"><span data-stu-id="23b74-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="23b74-154">Этот шаблон можно расширить таким образом, чтобы он мог использоваться для любого сценария, который включает в себя интеграцию SharePoint.</span><span class="sxs-lookup"><span data-stu-id="23b74-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="23b74-155">Чтобы загрузить шаблон **Поток — интеграция SharePoint**, выберите [Поток — интеграция SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="23b74-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="admin-console-to-manage-talent-pools"></a><span data-ttu-id="23b74-156">Консоль администрирования для управления кадровыми пулами</span><span class="sxs-lookup"><span data-stu-id="23b74-156">Admin console to manage talent pools</span></span>

<span data-ttu-id="23b74-157">Когда включена интеграция с LinkedIn, Attract автоматически создает кадровый пул LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="23b74-157">When you enable integration with LinkedIn, Attract automatically createas a LinkedIn talent pool.</span></span> <span data-ttu-id="23b74-158">Когда наниматель обменивается сообщениями InMail с кандидатом через LinkedIn, Attract создает профиль для кандидата, и кандидат становится участником кадрового пула LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="23b74-158">When a recruiter exchanges InMail with a recruit through LinkedIn, Attract creates a profile for the recruit, and the recruit becomes a member of the LinkedIn talent pool.</span></span> <span data-ttu-id="23b74-159">Это приложение PowerApps полезно для реорганизации кандидатов в кадровых пулах на основе навыка.</span><span class="sxs-lookup"><span data-stu-id="23b74-159">This PowerApps app is useful for reorganizing candidates in talent pools based on skill.</span></span>

<span data-ttu-id="23b74-160">Выполните это приложение PowerApps в качестве консоли администрирования для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="23b74-160">Run this PowerApps app as an admin console to perform the following tasks:</span></span>

- <span data-ttu-id="23b74-161">Просмотр списка кандидатов в кадровом пуле</span><span class="sxs-lookup"><span data-stu-id="23b74-161">List candidates in a talent pool</span></span>
- <span data-ttu-id="23b74-162">Добавление кандидатов в кадровый пул и удаление кандидатов из пула</span><span class="sxs-lookup"><span data-stu-id="23b74-162">Add and remove candidates from a talent pool</span></span>
- <span data-ttu-id="23b74-163">Перемещение кандидатов из одного кадрового пула в другой</span><span class="sxs-lookup"><span data-stu-id="23b74-163">Move candidates from one talent pool to another</span></span>
- <span data-ttu-id="23b74-164">Определение того, являются ли кандидаты уже частью кадрового пула, перед их перемещением</span><span class="sxs-lookup"><span data-stu-id="23b74-164">Determine whether candidates are already part of a talent pool before moving them</span></span>
- <span data-ttu-id="23b74-165">Проверка навыков кандидатов перед их перемещением в другие кадровые пулы</span><span class="sxs-lookup"><span data-stu-id="23b74-165">Check the skills of candidates before moving them to other talent pools</span></span>

<span data-ttu-id="23b74-166">В этом приложении PowerApps используются отношения "многие ко многим", поэтому его можно использовать в качестве шаблона для других сценариев, в которых необходимо извлечь записи, имеющие отношения "многие ко многим".</span><span class="sxs-lookup"><span data-stu-id="23b74-166">This PowerApps app uses many-to-many relationships, so you can use it as a template for other scenarios where you need to extract records that have many-to-many relationships.</span></span>

<span data-ttu-id="23b74-167">Чтобы загрузить шаблон **Консоль администрирования для управления кадровыми пулами**, перейдите в [Консоль администрирования для управления кадровыми пулами](https://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="23b74-167">To download the **Admin console to manage talent pools** template,  go to [Admin console to manage talent pools](https://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23b74-168">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="23b74-168">Additional resources</span></span>

[<span data-ttu-id="23b74-169">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="23b74-169">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="23b74-170">Перенос приложений между клиентами и средами</span><span class="sxs-lookup"><span data-stu-id="23b74-170">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
