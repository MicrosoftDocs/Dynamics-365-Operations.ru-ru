---
title: Расширение Talent с помощью Power Apps и Power Automate
description: В этой теме описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Talent, использующих Microsoft Power Apps и Microsoft Power Automate.
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
ms.openlocfilehash: 3bb61297e294aa3f2d06f542bebe29d7afae9c3b
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832846"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="0997e-103">Расширение Talent с помощью Power Apps и Power Automate</span><span class="sxs-lookup"><span data-stu-id="0997e-103">Extend Talent with Power Apps and Power Automate</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0997e-104">В этой теме описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Talent, использующих Microsoft Power Apps и Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="0997e-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="0997e-105">Можно импортировать пакет решения, связанный с каждым примером, в среду Power Apps.</span><span class="sxs-lookup"><span data-stu-id="0997e-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="0997e-106">Затем можно использовать эти пакеты как руководство или как основу для реализации сценариев, которые применимы к вашей организации.</span><span class="sxs-lookup"><span data-stu-id="0997e-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0997e-107">Если вы хотите использовать шаблоны и приложения, описанные в этом разделе, "как есть", обязательно проверьте их, чтобы убедиться в том, что они охватывают все сценарии, относящиеся к вашей реализации.</span><span class="sxs-lookup"><span data-stu-id="0997e-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="0997e-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="0997e-108">Prerequisites</span></span>

- <span data-ttu-id="0997e-109">Для импорта пакетов пользователи должны иметь разрешение **Создатель среды**.</span><span class="sxs-lookup"><span data-stu-id="0997e-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="0997e-110">Для экспорта или импорта приложений пользователи должны иметь лицензию плана 2 Power Apps или пробную лицензию плана 2 Power Apps.</span><span class="sxs-lookup"><span data-stu-id="0997e-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="0997e-111">Power Automate — подключение формы</span><span class="sxs-lookup"><span data-stu-id="0997e-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="0997e-112">Шаблон **Power Automate — подключение формы** можно использовать для чтения данных из Microsoft Forms и сохранения их в объекте Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0997e-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="0997e-113">Этот шаблон можно расширить таким образом, чтобы его можно было использовать для других сценариев.</span><span class="sxs-lookup"><span data-stu-id="0997e-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="0997e-114">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="0997e-114">Here are some examples:</span></span>

- <span data-ttu-id="0997e-115">Запись оценок кандидатов.</span><span class="sxs-lookup"><span data-stu-id="0997e-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="0997e-116">Запись результатов из анкет для курса.</span><span class="sxs-lookup"><span data-stu-id="0997e-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="0997e-117">Компиляция библиотеки вопросов собеседования для администраторов отдела кадров (HR).</span><span class="sxs-lookup"><span data-stu-id="0997e-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="0997e-118">Запись оценки кандидатом процесса собеседования</span><span class="sxs-lookup"><span data-stu-id="0997e-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="0997e-119">В Microsoft Dynamics 365: Attract формы могут отображаться на портале кандидата, и кандидаты могут заполнять сведения.</span><span class="sxs-lookup"><span data-stu-id="0997e-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="0997e-120">Формы можно также внедрить как действия в шаблон должности.</span><span class="sxs-lookup"><span data-stu-id="0997e-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="0997e-121">Когда кандидат отправляет форму, Microsoft Power Automate записывает отправку формы, считывает данные и сохраняет их в объекте Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0997e-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="0997e-122">Для загрузки шаблона **Power Automate — подключение формы** и структуры пользовательского объекта, перейдите к [Power Automate — подключение формы](https://go.microsoft.com/fwlink/?linkid=2081988) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0997e-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a><span data-ttu-id="0997e-123">Инициализация и извлечение параметров, переданных в Power Apps</span><span class="sxs-lookup"><span data-stu-id="0997e-123">Initiate and Extract Parameters Passed to Power Apps</span></span>

<span data-ttu-id="0997e-124">Шаблон **Инициализация и извлечение параметров, переданных в Power Apps** можно использовать в качестве отправной точки для любого сценария Power Apps, который связан с Attract.</span><span class="sxs-lookup"><span data-stu-id="0997e-124">The **Initiate and Extract Parameters Passed to Power Apps** template can be used as a starting point for any Power Apps scenario that is specific to Attract.</span></span> <span data-ttu-id="0997e-125">Он включает все параметры по умолчанию, передаваемые приложением Attract, такие как **Заявление о приеме на работу**, **Код кандидата** и **JobID**.</span><span class="sxs-lookup"><span data-stu-id="0997e-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="0997e-126">Этот шаблон может использоваться для извлечения формы оценки кандидата, чтобы менеджер по найму мог просмотреть оценку, указанную кандидатом.</span><span class="sxs-lookup"><span data-stu-id="0997e-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="0997e-127">Приложения, которые созданы с помощью Power Apps могут быть встроены в шаблон должности в Attract.</span><span class="sxs-lookup"><span data-stu-id="0997e-127">Apps that are created by using Power Apps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="0997e-128">Чтобы загрузить шаблон **Инициализация и извлечение параметров, переданных в Power Apps** и структуру пользовательского объекта, перейдите к шаблону [Инициализация и извлечение параметров, переданных в Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0997e-128">To download the **Initiate and Extract Parameters Passed to Power Apps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="0997e-129">Интеграция с Office 365</span><span class="sxs-lookup"><span data-stu-id="0997e-129">Integration with Office 365</span></span>

<span data-ttu-id="0997e-130">Приложение **Интеграция с Office 365** может использоваться для извлечения сведений о рабочей группе для выполнивших вход пользователей из Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="0997e-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="0997e-131">Оно ссылается на работников в Talent для извлечения сведений о времени прихода и ухода и записей исключения.</span><span class="sxs-lookup"><span data-stu-id="0997e-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="0997e-132">Сведения о времени прихода и ухода хранятся в настраиваемых объектах Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0997e-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="0997e-133">Предполагается, что эти сведения заполняются из систем других производителей путем интеграции.</span><span class="sxs-lookup"><span data-stu-id="0997e-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="0997e-134">Это приложение можно расширить таким образом, чтобы его можно было использовать для других сценариев.</span><span class="sxs-lookup"><span data-stu-id="0997e-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="0997e-135">Например, оно может использоваться для отображения сведений об отпусках рабочей группы, события календаря и любых других событиях, связанных с рабочей группой.</span><span class="sxs-lookup"><span data-stu-id="0997e-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="0997e-136">Чтобы загрузить приложение **Интеграция с Office 365** и структуру пользовательского объекта, перейдите к приложению [Интеграция с Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0997e-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--email-notification"></a><span data-ttu-id="0997e-137">Power Automate — уведомление по электронной почте</span><span class="sxs-lookup"><span data-stu-id="0997e-137">Power Automate – Email Notification</span></span>

<span data-ttu-id="0997e-138">Шаблон **Power Automate — уведомление по электронной почте** можно использовать для сценариев уведомления по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="0997e-138">The **Power Automate – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="0997e-139">Он может использоваться для выдачи сообщений по электронной почте для кандидатов, которых рабочая группа найма на работу отклоняет на любом этапе процесса набора сотрудников.</span><span class="sxs-lookup"><span data-stu-id="0997e-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="0997e-140">Этот шаблон может быть расширен для отслеживания изменений этапа кандидата в процессе набора персонала и для отправки уведомлений рабочей группе найма сотрудников и кандидату.</span><span class="sxs-lookup"><span data-stu-id="0997e-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="0997e-141">В общем случае для объектов, которые хранятся в Common Data Service, потоки можно настроить для отправки уведомлений о событиях, происходящих в Core HR, Attract или Onboard.</span><span class="sxs-lookup"><span data-stu-id="0997e-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Onboard.</span></span>

<span data-ttu-id="0997e-142">Чтобы загрузить шаблон **Power Automate — уведомление по электронной почте**, выберите [Power Automate — уведомление по электронной почте](https://go.microsoft.com/fwlink/?linkid=2082103) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0997e-142">To download the **Power Automate – Email Notification** template, go to [Power Automate – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="0997e-143">Power Automate — подключение и выполнение SQL</span><span class="sxs-lookup"><span data-stu-id="0997e-143">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="0997e-144">Шаблон **Power Automate — подключение и выполнение SQL** подключается к Microsoft SQL Server и позволяет выполнять запросы SQL.</span><span class="sxs-lookup"><span data-stu-id="0997e-144">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="0997e-145">Несмотря на то, что этот шаблон предназначен для чтения и обновления таблиц SQL, его можно расширить, чтобы его можно было использовать для других сценариев.</span><span class="sxs-lookup"><span data-stu-id="0997e-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="0997e-146">Например, он может использоваться для заполнения промежуточной таблицы в Common Data Service с записями из SQL Server, а также для периодической синхронизации промежуточной таблицы с помощью инкрементной принудительной отправки из SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0997e-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="0997e-147">Для загрузки шаблона **Power Automate — подключение и выполнение SQL** перейдите к пункту [Power Automate — подключение и выполнение SQL](https://go.microsoft.com/fwlink/?linkid=2081789) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0997e-147">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="0997e-148">Power Automate — интеграция SharePoint</span><span class="sxs-lookup"><span data-stu-id="0997e-148">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="0997e-149">Шаблон **Power Automate — интеграция с SharePoint** может использоваться для чтения данных из списка Microsoft SharePoint, сравнения списка со значениями полей для любого объекта Common Data Service и отправить результаты сравнения в виде уведомления по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="0997e-149">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="0997e-150">Организация может иметь набор навыков, которые требуются срочно.</span><span class="sxs-lookup"><span data-stu-id="0997e-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="0997e-151">Эти навыки могут храниться в SharePoint в виде списка SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0997e-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="0997e-152">Когда кандидат подает заявление для любой должности, для которой перечислен набор необходимых навыков, если существует значительное соответствие между навыками кандидата и навыками, которые хранятся в SharePoint, отправляется уведомление по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="0997e-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="0997e-153">Таким образом должности, которые требуются срочно, заполняются быстрее, поскольку уведомления помогают агентам по найму связываться с кандидатами и выполнять кросс-наем кандидатов в организации.</span><span class="sxs-lookup"><span data-stu-id="0997e-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="0997e-154">Этот шаблон можно расширить таким образом, чтобы он мог использоваться для любого сценария, который включает в себя интеграцию SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0997e-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="0997e-155">Чтобы загрузить шаблон **Power Automate — интеграция SharePoint**, выберите [Power Automate — интеграция SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0997e-155">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="0997e-156">Приложение ссылки</span><span class="sxs-lookup"><span data-stu-id="0997e-156">Referral App</span></span>
<span data-ttu-id="0997e-157">Для добавления кандидатов в общий кадровый пул можно использовать приложение ссылки.</span><span class="sxs-lookup"><span data-stu-id="0997e-157">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="0997e-158">Источник ссылки может ввести значения **Имя**, **Фамилия**, **Адрес электронной почты** и **URL-адрес Linkedln** при отправке кандидата.</span><span class="sxs-lookup"><span data-stu-id="0997e-158">The referrer can enter **Firstname**, **Lastname**, **Email**, and **Linkedln URL** when submitting a candidate.</span></span> <span data-ttu-id="0997e-159">Метаданные источника кандидата заполняются информацией об источнике ссылки.</span><span class="sxs-lookup"><span data-stu-id="0997e-159">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="0997e-160">Это приложение можно встроить в дистанционное обслуживание сотрудников (ESS) для отправки ссылок, либо можно использовать его в качестве гиперссылки на корпоративном портале и запускать его как отдельное приложение.</span><span class="sxs-lookup"><span data-stu-id="0997e-160">You can embed this app in Employee self-service (ESS) for submitting referrals, or you can be use it as a hyperlink in the Corporate Portal and run as a stand-alone app.</span></span>

<span data-ttu-id="0997e-161">Чтобы загрузить **Приложение ссылки**, перейдите по адресу [Решение расширения Dynamics 365 Talent: приложение ссылки](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0997e-161">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) on the Microsoft Download Center.</span></span> <span data-ttu-id="0997e-162">Можно импортировать это приложение и настроить его для добавления дополнительных функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="0997e-162">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0997e-163">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0997e-163">Additional resources</span></span>

[<span data-ttu-id="0997e-164">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="0997e-164">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="0997e-165">Перенос приложений между клиентами и средами</span><span class="sxs-lookup"><span data-stu-id="0997e-165">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
