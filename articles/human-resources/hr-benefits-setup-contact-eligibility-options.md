---
title: Настройка параметров приемлемости личных контактов
description: Настройка параметров допустимости для личных контактов в Microsoft Dynamics 365 Human Resources. Личные контакты могут быть бенефициарами или иждивенцами.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f300ac917ac21db9fffbffcc6eb8589357c0a3e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466214"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="437a6-104">Настройка параметров приемлемости личных контактов</span><span class="sxs-lookup"><span data-stu-id="437a6-104">Configure personal contact eligibility options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="437a6-105">В этой статье показано, как настроить типы личных контактов для использования в Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="437a6-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="437a6-106">Личные контакты могут быть бенефициарами или иждивенцами.</span><span class="sxs-lookup"><span data-stu-id="437a6-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="437a6-107">В рабочей области **Управление льготами** в **Настройка** выберите **Параметры допустимости личных контактов**.</span><span class="sxs-lookup"><span data-stu-id="437a6-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="437a6-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="437a6-108">Select **New**.</span></span>

3. <span data-ttu-id="437a6-109">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="437a6-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="437a6-110">Поле</span><span class="sxs-lookup"><span data-stu-id="437a6-110">Field</span></span> | <span data-ttu-id="437a6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="437a6-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="437a6-112">**Параметр допустимости**</span><span class="sxs-lookup"><span data-stu-id="437a6-112">**Eligibility option**</span></span> | <span data-ttu-id="437a6-113">Уникальное имя или код параметра допустимости для идентификации параметра допустимости.</span><span class="sxs-lookup"><span data-stu-id="437a6-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="437a6-114">**Описание**</span><span class="sxs-lookup"><span data-stu-id="437a6-114">**Description**</span></span> | <span data-ttu-id="437a6-115">Краткое описание параметра допустимости.</span><span class="sxs-lookup"><span data-stu-id="437a6-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="437a6-116">**Код допустимости для контакта**</span><span class="sxs-lookup"><span data-stu-id="437a6-116">**Contact eligibility code**</span></span> | <span data-ttu-id="437a6-117">Системный код, наилучшим образом описывающий личный параметр допустимости.</span><span class="sxs-lookup"><span data-stu-id="437a6-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="437a6-118">Варианты:</span><span class="sxs-lookup"><span data-stu-id="437a6-118">You can choose from:</span></span> <ul><li><span data-ttu-id="437a6-119">Связь</span><span class="sxs-lookup"><span data-stu-id="437a6-119">Relationship</span></span></li><li><span data-ttu-id="437a6-120">Студент</span><span class="sxs-lookup"><span data-stu-id="437a6-120">Student</span></span></li><li><span data-ttu-id="437a6-121">Не соответствующий по возрасту иждивенец</span><span class="sxs-lookup"><span data-stu-id="437a6-121">Overage dependent</span></span></li><li><span data-ttu-id="437a6-122">Пожилой недееспособный иждивенец</span><span class="sxs-lookup"><span data-stu-id="437a6-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="437a6-123">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="437a6-123">**Status**</span></span> | <span data-ttu-id="437a6-124">Статус параметра допустимости.</span><span class="sxs-lookup"><span data-stu-id="437a6-124">The status of the eligibility option.</span></span> <span data-ttu-id="437a6-125">Если статус параметра допустимости имеет значение "неактивный", вы не можете выбрать этот параметр допустимости личных контактов для личных контактов.</span><span class="sxs-lookup"><span data-stu-id="437a6-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="437a6-126">**Связь**</span><span class="sxs-lookup"><span data-stu-id="437a6-126">**Relationship**</span></span> | <span data-ttu-id="437a6-127">Определяет связь между личным контактом и сотрудником.</span><span class="sxs-lookup"><span data-stu-id="437a6-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="437a6-128">Это поле активно, только если код допустимости контакта имеет значение "связь".</span><span class="sxs-lookup"><span data-stu-id="437a6-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="437a6-129">**Возраст**</span><span class="sxs-lookup"><span data-stu-id="437a6-129">**Age**</span></span> | <span data-ttu-id="437a6-130">Максимальный возраст допустимого личного контакта для плана льгот.</span><span class="sxs-lookup"><span data-stu-id="437a6-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="437a6-131">Это поле активно, только если выбрана "связь".</span><span class="sxs-lookup"><span data-stu-id="437a6-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="437a6-132">Этот возраст сравнивается с расчетным возрастом личного контакта.</span><span class="sxs-lookup"><span data-stu-id="437a6-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="437a6-133">Рассчитанный возраст: (дата покрытия – дата рождения личного контакта / 365).</span><span class="sxs-lookup"><span data-stu-id="437a6-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="437a6-134">Это число всегда является целым числом.</span><span class="sxs-lookup"><span data-stu-id="437a6-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="437a6-135">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="437a6-135">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]