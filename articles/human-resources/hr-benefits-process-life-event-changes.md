---
title: Обработка изменений в жизни
description: Обработка изменений жизненных событий в Microsoft Dynamics 365 Human Resources для изменений жизненных событий.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39d1e94347809a1756fc4f66e5edc345c70eaf39
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420192"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="b0cd0-103">Обработка изменений в жизни</span><span class="sxs-lookup"><span data-stu-id="b0cd0-103">Process life event changes</span></span>

<span data-ttu-id="b0cd0-104">Обработка изменений жизненных событий в Microsoft Dynamics 365 Human Resources для двух изменений жизненных событий:</span><span class="sxs-lookup"><span data-stu-id="b0cd0-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="b0cd0-105">Изменения дней рождения</span><span class="sxs-lookup"><span data-stu-id="b0cd0-105">Birthday changes</span></span>
- <span data-ttu-id="b0cd0-106">Изменения окончания срока действия переопределения правила допустимости</span><span class="sxs-lookup"><span data-stu-id="b0cd0-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="b0cd0-107">В рабочей области **Управление льготами** в **Обработка** выберите **Обработка изменений жизненных событий**.</span><span class="sxs-lookup"><span data-stu-id="b0cd0-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="b0cd0-108">В диалоговом окне **Выполнение процесса изменения жизненного события** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="b0cd0-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="b0cd0-109">Поле</span><span class="sxs-lookup"><span data-stu-id="b0cd0-109">Field</span></span> | <span data-ttu-id="b0cd0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b0cd0-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b0cd0-111">Период регистрации</span><span class="sxs-lookup"><span data-stu-id="b0cd0-111">Enrollment period</span></span> | <span data-ttu-id="b0cd0-112">Период регистрации, для которого необходимо обработать изменения жизненного события.</span><span class="sxs-lookup"><span data-stu-id="b0cd0-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="b0cd0-113">Информация о компании</span><span class="sxs-lookup"><span data-stu-id="b0cd0-113">Legal entity</span></span> | <span data-ttu-id="b0cd0-114">Юридическое лицо, для которого необходимо обработать изменения жизненного события.</span><span class="sxs-lookup"><span data-stu-id="b0cd0-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="b0cd0-115">Если необходимо выполнить процесс в фоновом режиме, выберите **Выполнить в фоновом режиме** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b0cd0-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="b0cd0-116">Введите сведения для процесса.</span><span class="sxs-lookup"><span data-stu-id="b0cd0-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="b0cd0-117">Чтобы настроить повторяющееся задание, выберите **Повторение**, введите сведения о повторении, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b0cd0-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="b0cd0-118">Чтобы настроить оповещение о заданиях, выберите **Оповещения**, выберите получаемые оповещения и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b0cd0-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="b0cd0-119">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b0cd0-119">Select **OK**.</span></span> <span data-ttu-id="b0cd0-120">Процесс будет выполнен с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="b0cd0-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="b0cd0-121">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b0cd0-121">Select **OK**.</span></span>
