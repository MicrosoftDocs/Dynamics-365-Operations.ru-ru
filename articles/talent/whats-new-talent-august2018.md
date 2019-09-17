---
title: Что нового и что изменилось в Dynamics 365 for Talent Core HR (август 2018 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 08/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-08-27
ms.dyn365.ops.version: Talent August 2018 update
ms.openlocfilehash: 3327939137486038b9002029c7c9e8d65dfa2f64
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742617"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-august-2018"></a><span data-ttu-id="c6c32-103">Что нового и что изменилось в Dynamics 365 for Talent Core HR (август 2018 г.)</span><span class="sxs-lookup"><span data-stu-id="c6c32-103">What's new or changed in Dynamics 365 for Talent Core HR (August 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c6c32-104">**Сборка 8.1.104**</span><span class="sxs-lookup"><span data-stu-id="c6c32-104">**Build 8.1.104**</span></span>

<span data-ttu-id="c6c32-105">В этой теме описываются новые и измененные компоненты в Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="c6c32-105">This topic describes features that are either new or changed in Dynamics 365 for Talent Core HR.</span></span>

## <a name="view-expiring-records-in-manager-self-service"></a><span data-ttu-id="c6c32-106">Просмотр записей с истекающим сроком действия на портале самообслуживания менеджеров</span><span class="sxs-lookup"><span data-stu-id="c6c32-106">View expiring records in Manager self service</span></span>

<span data-ttu-id="c6c32-107">На портале самообслуживания менеджеров теперь можно просматривать записи с истекающим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="c6c32-107">You can now view expiring records in Manager self-service.</span></span> <span data-ttu-id="c6c32-108">Предусмотрены новые параметры для настройки того, какая информация будет доступна для просмотра менеджерами.</span><span class="sxs-lookup"><span data-stu-id="c6c32-108">New options are allow you to configure what information will be available for managers to view.</span></span> <span data-ttu-id="c6c32-109">К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="c6c32-109">These include:</span></span>

-   <span data-ttu-id="c6c32-110">Сертификаты</span><span class="sxs-lookup"><span data-stu-id="c6c32-110">Certificates</span></span>

-   <span data-ttu-id="c6c32-111">Идентификационные номера</span><span class="sxs-lookup"><span data-stu-id="c6c32-111">Identification numbers</span></span>

-   <span data-ttu-id="c6c32-112">Периоды надзора</span><span class="sxs-lookup"><span data-stu-id="c6c32-112">Probation periods</span></span>

-   <span data-ttu-id="c6c32-113">Отборы</span><span class="sxs-lookup"><span data-stu-id="c6c32-113">Screenings</span></span>

-   <span data-ttu-id="c6c32-114">Тесты</span><span class="sxs-lookup"><span data-stu-id="c6c32-114">Tests</span></span>

<span data-ttu-id="c6c32-115">Эта функция также дает возможность указать диапазон дней, в пределах которого следует искать записи с истекающим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="c6c32-115">This feature also gives you the ability to specify the range of days in which to look for expiring records.</span></span>

## <a name="configurable-transfer-actions"></a><span data-ttu-id="c6c32-116">Конфигурируемые действия перемещения</span><span class="sxs-lookup"><span data-stu-id="c6c32-116">Configurable transfer actions</span></span>

<span data-ttu-id="c6c32-117">Можно сконфигурировать по ролям параметры, доступные при вводе запроса на перемещение.</span><span class="sxs-lookup"><span data-stu-id="c6c32-117">You can configure by role the options that will be available during the entry of a transfer request.</span></span> <span data-ttu-id="c6c32-118">Это обеспечивает дополнительную гибкость для различных ролей в организации.</span><span class="sxs-lookup"><span data-stu-id="c6c32-118">This feature provides additional flexibility across the roles in an organization.</span></span>

<span data-ttu-id="c6c32-119">Например, руководители, которые запрашивают перемещения сотрудников, могут не иметь доступа, чтобы предложить или ввести суммы компенсации или выбрать списки задач, которые будут связаны с запросом на перемещение.</span><span class="sxs-lookup"><span data-stu-id="c6c32-119">For example, managers requesting employee transfers may not have access to suggest or enter compensation amounts or select the task lists that will be associated with the transfer request.</span></span> <span data-ttu-id="c6c32-120">В этом случае руководители могут создавать и отправлять запросы на перемещения, но вводить компенсации или назначать списки задач им не разрешено.</span><span class="sxs-lookup"><span data-stu-id="c6c32-120">In this case, managers can create and submit transfer requests but are not allowed to enter compensation or task list assignments.</span></span> <span data-ttu-id="c6c32-121">В этой же конфигурации HR-специалисты смогут назначить новые значения компенсации, а также назначить дополнительные контрольные списки для заполнения в результате выполнения перемещения.</span><span class="sxs-lookup"><span data-stu-id="c6c32-121">In this same configuration, HR will be able to assign the new compensation values as well as assign any additional checklists to be completed as a result of the transfer completing.</span></span>

<span data-ttu-id="c6c32-122">По умолчанию новые параметры конфигурации заданы так, чтобы не изменять возможности, имевшиеся до этого обновления.</span><span class="sxs-lookup"><span data-stu-id="c6c32-122">By default, the new configuration options are set to not change the capabilities prior to this update.</span></span>

## <a name="leave-and-absence"></a><span data-ttu-id="c6c32-123">Отпуск и отсутствие</span><span class="sxs-lookup"><span data-stu-id="c6c32-123">Leave and absence</span></span>

<span data-ttu-id="c6c32-124">В компоненте "Отпуск и отсутствие" теперь есть дополнительные поля дат.</span><span class="sxs-lookup"><span data-stu-id="c6c32-124">There are now additional Date fields available in Leave and Absence.</span></span>

<span data-ttu-id="c6c32-125">С их помощью можно задавать основание периода начисления на уровне плана так, чтобы использовать конкретные даты, связанные с самим сотрудником.</span><span class="sxs-lookup"><span data-stu-id="c6c32-125">With this feature you can set the accrual period basis at the plan level to use specific employee dates.</span></span> <span data-ttu-id="c6c32-126">Это позволяет использовать в процессе начисления отпусков даты, отличные от начальной даты плана.</span><span class="sxs-lookup"><span data-stu-id="c6c32-126">This allows for dates other than the plan start date to be used during the leave accrual process.</span></span> <span data-ttu-id="c6c32-127">Параметры дат, связанных с сотрудниками, включают в себя следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c6c32-127">Options for employee specific dates include the following values:</span></span>

-   <span data-ttu-id="c6c32-128">Произвольная (было доступно до этого обновления)</span><span class="sxs-lookup"><span data-stu-id="c6c32-128">Custom (available prior to this update)</span></span>

-   <span data-ttu-id="c6c32-129">Дата годовщины</span><span class="sxs-lookup"><span data-stu-id="c6c32-129">Anniversary date</span></span>

-   <span data-ttu-id="c6c32-130">Дата первоначального приема на работу</span><span class="sxs-lookup"><span data-stu-id="c6c32-130">Original hire date</span></span>

-   <span data-ttu-id="c6c32-131">Дата начала стажа</span><span class="sxs-lookup"><span data-stu-id="c6c32-131">Seniority date</span></span>

-   <span data-ttu-id="c6c32-132">Скорректированная дата приема работника на работу</span><span class="sxs-lookup"><span data-stu-id="c6c32-132">Worker’s adjusted start date</span></span>

-   <span data-ttu-id="c6c32-133">Дата приема работника на работу</span><span class="sxs-lookup"><span data-stu-id="c6c32-133">Worker’s start date</span></span>

<span data-ttu-id="c6c32-134">Будучи настроенным для использования одной из дат, связанных с конкретным сотрудником, процесс регистрации будут использовать указанную дату для расчета периодов начислений.</span><span class="sxs-lookup"><span data-stu-id="c6c32-134">When configured to use one of the employee specific dates, the enrollment process will use the specified date to calculate the accrual periods.</span></span> <span data-ttu-id="c6c32-135">Основание периода начисления также отображается в регистрации сотрудника в плане, чтобы вы понимали, что именно используется в процессе начисления.</span><span class="sxs-lookup"><span data-stu-id="c6c32-135">The accrual period basis is also displayed on the employee’s plan enrollment to help you understand what’s being used during the accrual process.</span></span>

## <a name="microsoft-word-integration"></a><span data-ttu-id="c6c32-136">Интеграция с Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="c6c32-136">Microsoft Word integration</span></span>

<span data-ttu-id="c6c32-137">В Core HR теперь можно использовать шаблоны документов.</span><span class="sxs-lookup"><span data-stu-id="c6c32-137">Document templates have been enabled throughout Core HR.</span></span> <span data-ttu-id="c6c32-138">Это позволяет создавать письма и отчеты на основе созданных вами шаблонов Word.</span><span class="sxs-lookup"><span data-stu-id="c6c32-138">This feature allows you to create letters and reports based on Word templates that you create.</span></span>

<span data-ttu-id="c6c32-139">Дополнительные сведения об этой возможности доступны в [учебнике по интеграции с Office](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span><span class="sxs-lookup"><span data-stu-id="c6c32-139">Additional information about this feature is available in the [Office integration tutorial](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span></span>


## <a name="other-fixes"></a><span data-ttu-id="c6c32-140">Другие исправления</span><span class="sxs-lookup"><span data-stu-id="c6c32-140">Other fixes</span></span>

<span data-ttu-id="c6c32-141">Этот выпуск также включает в себя ряд исправлений ошибок, новые объекты, исправления в существующих объектах, а также изменения в локализованных метках.</span><span class="sxs-lookup"><span data-stu-id="c6c32-141">This release also includes a number of bug fixes, the addition of new entities, fixes to existing entities, and localized label changes.</span></span>
