---
title: Обработка изменений в жизни
description: Обработка изменений жизненных событий в Microsoft Dynamics 365 Human Resources для изменений жизненных событий.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: d32d6ba893a99149e27f644ac80e430db3c08fa0
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114028"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="4ac4a-103">Обработка изменений в жизни</span><span class="sxs-lookup"><span data-stu-id="4ac4a-103">Process life event changes</span></span>

<span data-ttu-id="4ac4a-104">Обработка изменений жизненных событий в Microsoft Dynamics 365 Human Resources для двух изменений жизненных событий:</span><span class="sxs-lookup"><span data-stu-id="4ac4a-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="4ac4a-105">Изменения дней рождения</span><span class="sxs-lookup"><span data-stu-id="4ac4a-105">Birthday changes</span></span>
- <span data-ttu-id="4ac4a-106">Изменения окончания срока действия переопределения правила допустимости</span><span class="sxs-lookup"><span data-stu-id="4ac4a-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="4ac4a-107">В рабочей области **Управление льготами** в **Обработка** выберите **Обработка изменений жизненных событий**.</span><span class="sxs-lookup"><span data-stu-id="4ac4a-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="4ac4a-108">В диалоговом окне **Выполнение процесса изменения жизненного события** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="4ac4a-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="4ac4a-109">Поле</span><span class="sxs-lookup"><span data-stu-id="4ac4a-109">Field</span></span> | <span data-ttu-id="4ac4a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4ac4a-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4ac4a-111">Период регистрации</span><span class="sxs-lookup"><span data-stu-id="4ac4a-111">Enrollment period</span></span> | <span data-ttu-id="4ac4a-112">Период регистрации, для которого необходимо обработать изменения жизненного события.</span><span class="sxs-lookup"><span data-stu-id="4ac4a-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="4ac4a-113">Информация о компании</span><span class="sxs-lookup"><span data-stu-id="4ac4a-113">Legal entity</span></span> | <span data-ttu-id="4ac4a-114">Юридическое лицо, для которого необходимо обработать изменения жизненного события.</span><span class="sxs-lookup"><span data-stu-id="4ac4a-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="4ac4a-115">Если необходимо выполнить процесс в фоновом режиме, выберите **Выполнить в фоновом режиме** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4ac4a-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="4ac4a-116">Введите сведения для процесса.</span><span class="sxs-lookup"><span data-stu-id="4ac4a-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="4ac4a-117">Чтобы настроить повторяющееся задание, выберите **Повторение**, введите сведения о повторении, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4ac4a-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="4ac4a-118">Чтобы настроить оповещение о заданиях, выберите **Оповещения**, выберите получаемые оповещения и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4ac4a-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="4ac4a-119">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4ac4a-119">Select **OK**.</span></span> <span data-ttu-id="4ac4a-120">Процесс будет выполнен с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="4ac4a-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="4ac4a-121">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4ac4a-121">Select **OK**.</span></span>
