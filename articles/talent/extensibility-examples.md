---
title: Расширение Talent с помощью Power Apps и Power Automate
description: В этой статье описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Talent Attract, использующих Microsoft Power Apps и Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529642"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="ec873-103">Расширение Talent с помощью Power Apps и Power Automate</span><span class="sxs-lookup"><span data-stu-id="ec873-103">Extend Talent with Power Apps and Power Automate</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ec873-104">В этой статье описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Talent: Attract, использующих Microsoft Power Apps и Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="ec873-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="ec873-105">Можно импортировать пакет решения, связанный с каждым примером, в среду Power Apps.</span><span class="sxs-lookup"><span data-stu-id="ec873-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="ec873-106">Затем можно использовать эти пакеты как руководство или как основу для реализации сценариев, которые применимы к вашей организации.</span><span class="sxs-lookup"><span data-stu-id="ec873-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec873-107">Если вы хотите использовать шаблоны и приложения, описанные в этой статье, "как есть", обязательно проверьте их, чтобы убедиться в том, что они охватывают все сценарии, относящиеся к вашей реализации.</span><span class="sxs-lookup"><span data-stu-id="ec873-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="ec873-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="ec873-108">Prerequisites</span></span>

- <span data-ttu-id="ec873-109">Для импорта пакетов пользователи должны иметь разрешение **Создатель среды**.</span><span class="sxs-lookup"><span data-stu-id="ec873-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="ec873-110">Для экспорта или импорта приложений пользователи должны иметь лицензию плана 2 Power Apps или пробную лицензию плана 2 Power Apps.</span><span class="sxs-lookup"><span data-stu-id="ec873-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="ec873-111">Power Automate — подключение формы</span><span class="sxs-lookup"><span data-stu-id="ec873-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="ec873-112">Шаблон **Power Automate — подключение формы** можно использовать для чтения данных из Microsoft Forms и сохранения их в объекте Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ec873-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="ec873-113">Этот шаблон можно расширить таким образом, чтобы его можно было использовать для других сценариев.</span><span class="sxs-lookup"><span data-stu-id="ec873-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="ec873-114">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="ec873-114">Here are some examples:</span></span>

- <span data-ttu-id="ec873-115">Запись оценок кандидатов.</span><span class="sxs-lookup"><span data-stu-id="ec873-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="ec873-116">Запись результатов из анкет для курса.</span><span class="sxs-lookup"><span data-stu-id="ec873-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="ec873-117">Компиляция библиотеки вопросов собеседования для администраторов отдела кадров (HR).</span><span class="sxs-lookup"><span data-stu-id="ec873-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="ec873-118">Запись оценки кандидатом процесса собеседования</span><span class="sxs-lookup"><span data-stu-id="ec873-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="ec873-119">В Microsoft Dynamics 365: Attract можно использовать формы на портале кандидата, где кандидаты могут заполнять сведения.</span><span class="sxs-lookup"><span data-stu-id="ec873-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="ec873-120">Формы можно также внедрить как действия в шаблон должности.</span><span class="sxs-lookup"><span data-stu-id="ec873-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="ec873-121">Когда кандидат отправляет форму, Microsoft Power Automate записывает отправку формы, считывает данные и сохраняет их в объекте Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ec873-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="ec873-122">Для загрузки шаблона **Power Automate — подключение формы** и структуры пользовательского объекта, перейдите к [Power Automate — подключение формы](https://go.microsoft.com/fwlink/?linkid=2081988) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ec873-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="ec873-123">Power Automate — интеграция SharePoint</span><span class="sxs-lookup"><span data-stu-id="ec873-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="ec873-124">Шаблон **Power Automate — интеграция с SharePoint** может использоваться для чтения данных из списка Microsoft SharePoint, сравнения списка со значениями полей для любого объекта Common Data Service и отправить результаты сравнения в виде уведомления по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="ec873-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="ec873-125">Организация может иметь набор навыков, которые требуются срочно.</span><span class="sxs-lookup"><span data-stu-id="ec873-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="ec873-126">Эти навыки могут храниться в SharePoint в виде списка SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ec873-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="ec873-127">Когда кандидат подает заявление для любой должности, для которой перечислен набор необходимых навыков, если существует значительное соответствие между навыками кандидата и навыками, которые хранятся в SharePoint, отправляется уведомление по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="ec873-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="ec873-128">Таким образом должности, которые требуются срочно, заполняются быстрее, поскольку уведомления помогают агентам по найму связываться с кандидатами и выполнять кросс-наем кандидатов в организации.</span><span class="sxs-lookup"><span data-stu-id="ec873-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="ec873-129">Этот шаблон можно расширить таким образом, чтобы он мог использоваться для любого сценария, который включает в себя интеграцию SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ec873-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="ec873-130">Чтобы загрузить шаблон **Power Automate — интеграция SharePoint**, выберите [Power Automate — интеграция SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ec873-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="ec873-131">Приложение ссылки</span><span class="sxs-lookup"><span data-stu-id="ec873-131">Referral App</span></span>

<span data-ttu-id="ec873-132">Для добавления кандидатов в общий кадровый пул можно использовать приложение ссылки.</span><span class="sxs-lookup"><span data-stu-id="ec873-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="ec873-133">Источник ссылки может ввести значения **Имя**, **Фамилия**, **Адрес электронной почты** и **URL-адрес LinkedIn** при отправке кандидата.</span><span class="sxs-lookup"><span data-stu-id="ec873-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="ec873-134">Метаданные источника кандидата заполняются информацией об источнике ссылки.</span><span class="sxs-lookup"><span data-stu-id="ec873-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="ec873-135">Это приложение можно встроить в дистанционное обслуживание сотрудников для отправки ссылок, либо можно использовать его в качестве гиперссылки на корпоративном портале и запускать его как отдельное приложение.</span><span class="sxs-lookup"><span data-stu-id="ec873-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="ec873-136">Чтобы загрузить **Приложение ссылки**, перейдите по адресу [Решение расширения Dynamics 365 Talent: приложение ссылки](https://www.microsoft.com/download/details.aspx?id=58497) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ec873-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="ec873-137">Можно импортировать это приложение и настроить его для добавления дополнительных функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="ec873-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec873-138">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ec873-138">Additional resources</span></span>

[<span data-ttu-id="ec873-139">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="ec873-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="ec873-140">Перенос приложений между клиентами и средами</span><span class="sxs-lookup"><span data-stu-id="ec873-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
