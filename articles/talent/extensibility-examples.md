---
title: Расширение Talent с помощью PowerApps и Microsoft Flow — примеры сценариев
description: В этой теме описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Talent, использующих Microsoft PowerApps и Microsoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
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
ms.openlocfilehash: 7bc3a18327f2d32770176eddcb7200681f0fb0da
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008067"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="da0ca-103">Расширение Talent с помощью PowerApps и Microsoft Flow — примеры сценариев</span><span class="sxs-lookup"><span data-stu-id="da0ca-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="da0ca-104">В этой теме описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Talent, использующих Microsoft PowerApps и Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="da0ca-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="da0ca-105">Можно импортировать пакет решения, связанный с каждым примером, в среду PowerApps.</span><span class="sxs-lookup"><span data-stu-id="da0ca-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="da0ca-106">Затем можно использовать эти пакеты как руководство или как основу для реализации сценариев, которые применимы к вашей организации.</span><span class="sxs-lookup"><span data-stu-id="da0ca-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da0ca-107">Если вы хотите использовать шаблоны и приложения, описанные в этом разделе, "как есть", обязательно проверьте их, чтобы убедиться в том, что они охватывают все сценарии, относящиеся к вашей реализации.</span><span class="sxs-lookup"><span data-stu-id="da0ca-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="da0ca-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="da0ca-108">Prerequisites</span></span>

- <span data-ttu-id="da0ca-109">Для импорта пакетов пользователи должны иметь разрешение **Создатель среды**.</span><span class="sxs-lookup"><span data-stu-id="da0ca-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="da0ca-110">Для экспорта или импорта приложений пользователи должны иметь лицензию плана 2 PowerApps или пробную лицензию плана 2 PowerApps.</span><span class="sxs-lookup"><span data-stu-id="da0ca-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="da0ca-111">Поток — подключение формы</span><span class="sxs-lookup"><span data-stu-id="da0ca-111">Flow – Form Connect</span></span>

<span data-ttu-id="da0ca-112">Шаблон **Поток — подключение формы** можно использовать для чтения данных из Microsoft Forms и сохранения их в объекте Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="da0ca-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="da0ca-113">Этот шаблон можно расширить таким образом, чтобы его можно было использовать для других сценариев.</span><span class="sxs-lookup"><span data-stu-id="da0ca-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="da0ca-114">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="da0ca-114">Here are some examples:</span></span>

- <span data-ttu-id="da0ca-115">Запись оценок кандидатов.</span><span class="sxs-lookup"><span data-stu-id="da0ca-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="da0ca-116">Запись результатов из анкет для курса.</span><span class="sxs-lookup"><span data-stu-id="da0ca-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="da0ca-117">Компиляция библиотеки вопросов собеседования для администраторов отдела кадров (HR).</span><span class="sxs-lookup"><span data-stu-id="da0ca-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="da0ca-118">Запись оценки кандидатом процесса собеседования</span><span class="sxs-lookup"><span data-stu-id="da0ca-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="da0ca-119">В Microsoft Dynamics 365: Attract формы могут отображаться на портале кандидата, и кандидаты могут заполнять сведения.</span><span class="sxs-lookup"><span data-stu-id="da0ca-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="da0ca-120">Формы можно также внедрить как действия в шаблон должности.</span><span class="sxs-lookup"><span data-stu-id="da0ca-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="da0ca-121">Когда кандидат отправляет форму, Microsoft Flow записывает отправку формы, считывает данные и сохраняет их в объекте Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="da0ca-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="da0ca-122">Для загрузки шаблона **Поток — подключение формы** и структуры пользовательского объекта, перейдите к [Поток — подключение формы](https://go.microsoft.com/fwlink/?linkid=2081988) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="da0ca-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="da0ca-123">Инициализация и извлечение параметров, переданных в PowerApps</span><span class="sxs-lookup"><span data-stu-id="da0ca-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="da0ca-124">Шаблон **Инициализация и извлечение параметров, переданных в PowerApps** можно использовать в качестве отправной точки для любого сценария PowerApps, который связан с Attract.</span><span class="sxs-lookup"><span data-stu-id="da0ca-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="da0ca-125">Он включает все параметры по умолчанию, передаваемые приложением Attract, такие как **Заявление о приеме на работу**, **Код кандидата** и **JobID**.</span><span class="sxs-lookup"><span data-stu-id="da0ca-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="da0ca-126">Этот шаблон может использоваться для извлечения формы оценки кандидата, чтобы менеджер по найму мог просмотреть оценку, указанную кандидатом.</span><span class="sxs-lookup"><span data-stu-id="da0ca-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="da0ca-127">Приложения, которые созданы с помощью PowerApps могут быть встроены в шаблон должности в Attract.</span><span class="sxs-lookup"><span data-stu-id="da0ca-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="da0ca-128">Чтобы загрузить шаблон **Инициализация и извлечение параметров, переданных в PowerApps** и структуру пользовательского объекта, перейдите к шаблону [Инициализация и извлечение параметров, переданных в PowerApps](https://go.microsoft.com/fwlink/?linkid=2081991) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="da0ca-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="da0ca-129">Интеграция с Office 365</span><span class="sxs-lookup"><span data-stu-id="da0ca-129">Integration with Office 365</span></span>

<span data-ttu-id="da0ca-130">Приложение **Интеграция с Office 365** может использоваться для извлечения сведений о рабочей группе для выполнивших вход пользователей из Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="da0ca-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="da0ca-131">Оно ссылается на работников в Talent для извлечения сведений о времени прихода и ухода и записей исключения.</span><span class="sxs-lookup"><span data-stu-id="da0ca-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="da0ca-132">Сведения о времени прихода и ухода хранятся в настраиваемых объектах Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="da0ca-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="da0ca-133">Предполагается, что эти сведения заполняются из систем других производителей путем интеграции.</span><span class="sxs-lookup"><span data-stu-id="da0ca-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="da0ca-134">Это приложение можно расширить таким образом, чтобы его можно было использовать для других сценариев.</span><span class="sxs-lookup"><span data-stu-id="da0ca-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="da0ca-135">Например, оно может использоваться для отображения сведений об отпусках рабочей группы, события календаря и любых других событиях, связанных с рабочей группой.</span><span class="sxs-lookup"><span data-stu-id="da0ca-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="da0ca-136">Чтобы загрузить приложение **Интеграция с Office 365** и структуру пользовательского объекта, перейдите к приложению [Интеграция с Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="da0ca-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="da0ca-137">Поток — уведомление по электронной почте</span><span class="sxs-lookup"><span data-stu-id="da0ca-137">Flow – Email Notification</span></span>

<span data-ttu-id="da0ca-138">Шаблон **Поток — уведомление по электронной почте** можно использовать для сценариев уведомления по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="da0ca-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="da0ca-139">Он может использоваться для выдачи сообщений по электронной почте для кандидатов, которых рабочая группа найма на работу отклоняет на любом этапе процесса набора сотрудников.</span><span class="sxs-lookup"><span data-stu-id="da0ca-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="da0ca-140">Этот шаблон может быть расширен для отслеживания изменений этапа кандидата в процессе набора персонала и для отправки уведомлений рабочей группе найма сотрудников и кандидату.</span><span class="sxs-lookup"><span data-stu-id="da0ca-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="da0ca-141">В общем случае для объектов, которые хранятся в Common Data Service, потоки можно настроить для отправки уведомлений о событиях, происходящих в Core HR, Attract или Onboard.</span><span class="sxs-lookup"><span data-stu-id="da0ca-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Onboard.</span></span>

<span data-ttu-id="da0ca-142">Чтобы загрузить шаблон **Поток — уведомление по электронной почте**, выберите [Поток — уведомление по электронной почте](https://go.microsoft.com/fwlink/?linkid=2082103) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="da0ca-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="da0ca-143">Поток — подключение и выполнение SQL</span><span class="sxs-lookup"><span data-stu-id="da0ca-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="da0ca-144">Шаблон **Поток — подключение и выполнение SQL** подключается к Microsoft SQL Server и позволяет выполнять запросы SQL.</span><span class="sxs-lookup"><span data-stu-id="da0ca-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="da0ca-145">Несмотря на то, что этот шаблон предназначен для чтения и обновления таблиц SQL, его можно расширить, чтобы его можно было использовать для других сценариев.</span><span class="sxs-lookup"><span data-stu-id="da0ca-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="da0ca-146">Например, он может использоваться для заполнения промежуточной таблицы в Common Data Service с записями из SQL Server, а также для периодической синхронизации промежуточной таблицы с помощью инкрементной принудительной отправки из SQL Server.</span><span class="sxs-lookup"><span data-stu-id="da0ca-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="da0ca-147">Для загрузки шаблона **Поток — подключение и выполнение SQL** перейдите к пункту [Поток — подключение и выполнение SQL](https://go.microsoft.com/fwlink/?linkid=2081789) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="da0ca-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="da0ca-148">Поток — интеграция с SharePoint</span><span class="sxs-lookup"><span data-stu-id="da0ca-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="da0ca-149">Шаблон **Поток — интеграция с SharePoint** шаблон может использоваться для чтения данных из списка Microsoft SharePoint, сравнения списка со значениями полей для любого объекта Common Data Service и отправить результаты сравнения в виде уведомления по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="da0ca-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="da0ca-150">Организация может иметь набор навыков, которые требуются срочно.</span><span class="sxs-lookup"><span data-stu-id="da0ca-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="da0ca-151">Эти навыки могут храниться в SharePoint в виде списка SharePoint.</span><span class="sxs-lookup"><span data-stu-id="da0ca-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="da0ca-152">Когда кандидат подает заявление для любой должности, для которой перечислен набор необходимых навыков, если существует значительное соответствие между навыками кандидата и навыками, которые хранятся в SharePoint, отправляется уведомление по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="da0ca-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="da0ca-153">Таким образом должности, которые требуются срочно, заполняются быстрее, поскольку уведомления помогают агентам по найму связываться с кандидатами и выполнять кросс-наем кандидатов в организации.</span><span class="sxs-lookup"><span data-stu-id="da0ca-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="da0ca-154">Этот шаблон можно расширить таким образом, чтобы он мог использоваться для любого сценария, который включает в себя интеграцию SharePoint.</span><span class="sxs-lookup"><span data-stu-id="da0ca-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="da0ca-155">Чтобы загрузить шаблон **Поток — интеграция SharePoint**, выберите [Поток — интеграция SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="da0ca-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="da0ca-156">Приложение ссылки</span><span class="sxs-lookup"><span data-stu-id="da0ca-156">Referral App</span></span>
<span data-ttu-id="da0ca-157">Для добавления кандидатов в общий кадровый пул можно использовать приложение ссылки.</span><span class="sxs-lookup"><span data-stu-id="da0ca-157">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="da0ca-158">Источник ссылки может ввести значения **Имя**, **Фамилия**, **Адрес электронной почты** и **URL-адрес Linkedln** при отправке кандидата.</span><span class="sxs-lookup"><span data-stu-id="da0ca-158">The referrer can enter **Firstname**, **Lastname**, **Email**, and **Linkedln URL** when submitting a candidate.</span></span> <span data-ttu-id="da0ca-159">Метаданные источника кандидата заполняются информацией об источнике ссылки.</span><span class="sxs-lookup"><span data-stu-id="da0ca-159">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="da0ca-160">Это приложение можно встроить в дистанционное обслуживание сотрудников (ESS) для отправки ссылок, либо можно использовать его в качестве гиперссылки на корпоративном портале и запускать его как отдельное приложение.</span><span class="sxs-lookup"><span data-stu-id="da0ca-160">You can embed this app in Employee self-service (ESS) for submitting referrals, or you can be use it as a hyperlink in the Corporate Portal and run as a stand-alone app.</span></span>

<span data-ttu-id="da0ca-161">Чтобы загрузить **Приложение ссылки**, перейдите по адресу [Решение расширения Dynamics 365 Talent: приложение ссылки](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="da0ca-161">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) on the Microsoft Download Center.</span></span> <span data-ttu-id="da0ca-162">Можно импортировать это приложение и настроить его для добавления дополнительных функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="da0ca-162">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da0ca-163">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="da0ca-163">Additional resources</span></span>

[<span data-ttu-id="da0ca-164">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="da0ca-164">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="da0ca-165">Перенос приложений между клиентами и средами</span><span class="sxs-lookup"><span data-stu-id="da0ca-165">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
