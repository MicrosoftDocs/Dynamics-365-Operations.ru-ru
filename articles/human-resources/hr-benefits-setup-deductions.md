---
title: Настройка вычетов
description: Используйте вычеты в Microsoft Dynamics 365 Human Resources, чтобы определить, сколько (если применимо) необходимо вычесть из зарплаты сотруднику по чеку для каждой льготы.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 4a916ca2d0d47407ff0d8cc2cc7ca179ecb59bae
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803665"
---
# <a name="configure-deductions"></a><span data-ttu-id="880cd-103">Настройка вычетов</span><span class="sxs-lookup"><span data-stu-id="880cd-103">Configure deductions</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="880cd-104">Используйте вычеты в Microsoft Dynamics 365 Human Resources, чтобы определить, сколько (если применимо) необходимо вычесть из зарплаты сотруднику по чеку для каждой льготы.</span><span class="sxs-lookup"><span data-stu-id="880cd-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="880cd-105">Вычеты зависят от даты, поэтому можно хранить запись журнала с информацией о вычетах.</span><span class="sxs-lookup"><span data-stu-id="880cd-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="880cd-106">В рабочей области **Управление льготами** в разделе **Настройка** выберите **Вычеты**.</span><span class="sxs-lookup"><span data-stu-id="880cd-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="880cd-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="880cd-107">Select **New**.</span></span>

3. <span data-ttu-id="880cd-108">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="880cd-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="880cd-109">Поле</span><span class="sxs-lookup"><span data-stu-id="880cd-109">Field</span></span> | <span data-ttu-id="880cd-110">Описание</span><span class="sxs-lookup"><span data-stu-id="880cd-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="880cd-111">**Вычет**</span><span class="sxs-lookup"><span data-stu-id="880cd-111">**Deduction**</span></span> | <span data-ttu-id="880cd-112">Уникальный код, используемый для идентификации вычета льготы.</span><span class="sxs-lookup"><span data-stu-id="880cd-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="880cd-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="880cd-113">**Description**</span></span> | <span data-ttu-id="880cd-114">Описание вычета.</span><span class="sxs-lookup"><span data-stu-id="880cd-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="880cd-115">**Действует**</span><span class="sxs-lookup"><span data-stu-id="880cd-115">**Effective**</span></span> | <span data-ttu-id="880cd-116">Дата начала.</span><span class="sxs-lookup"><span data-stu-id="880cd-116">The start date.</span></span> <span data-ttu-id="880cd-117">Значение по умолчанию — текущая системная дата.</span><span class="sxs-lookup"><span data-stu-id="880cd-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="880cd-118">**Истечение срока действия**</span><span class="sxs-lookup"><span data-stu-id="880cd-118">**Expiration**</span></span> | <span data-ttu-id="880cd-119">Дата окончания.</span><span class="sxs-lookup"><span data-stu-id="880cd-119">The end date.</span></span> <span data-ttu-id="880cd-120">Значение по умолчанию — 12/31/2154, что означает "никогда".</span><span class="sxs-lookup"><span data-stu-id="880cd-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="880cd-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="880cd-121">**Heading**</span></span> | <span data-ttu-id="880cd-122">Код заголовка из системы зарплаты, который будет использоваться данным вычетом для сотрудника в части вычета при обработке льгот для зарплаты.</span><span class="sxs-lookup"><span data-stu-id="880cd-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="880cd-123">Используется при использовании стороннего поставщика зарплаты.</span><span class="sxs-lookup"><span data-stu-id="880cd-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="880cd-124">**Ссылка сотрудника для вычета из зарплаты**</span><span class="sxs-lookup"><span data-stu-id="880cd-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="880cd-125">Код вычета из системы расчета зарплаты, который этот вычет будет использовать для доли сотрудника в вычете при обработке льгот для зарплаты.</span><span class="sxs-lookup"><span data-stu-id="880cd-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="880cd-126">**Заголовок суммы**</span><span class="sxs-lookup"><span data-stu-id="880cd-126">**Amount heading**</span></span> | <span data-ttu-id="880cd-127">Код заголовка из системы зарплаты, который будет использоваться суммой вычета для сотрудника в части вычета при обработке льгот для зарплаты.</span><span class="sxs-lookup"><span data-stu-id="880cd-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="880cd-128">Обычно используется при использовании стороннего поставщика зарплаты.</span><span class="sxs-lookup"><span data-stu-id="880cd-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="880cd-129">**Может удалять**</span><span class="sxs-lookup"><span data-stu-id="880cd-129">**Can delete**</span></span> | <span data-ttu-id="880cd-130">Указывает, может ли экспортированное значение из Dynamics 365 for Finance and Operations быть причиной удаления значения в системе зарплаты.</span><span class="sxs-lookup"><span data-stu-id="880cd-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="880cd-131">**Парные столбцы**</span><span class="sxs-lookup"><span data-stu-id="880cd-131">**Paired columns**</span></span> | <span data-ttu-id="880cd-132">Указывает, следует ли экспортировать заголовок и сумму вычета в парные смежные столбцы в системе зарплаты.</span><span class="sxs-lookup"><span data-stu-id="880cd-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="880cd-133">**Дата вступления изменения в силу**</span><span class="sxs-lookup"><span data-stu-id="880cd-133">**Change effective date**</span></span> | <span data-ttu-id="880cd-134">Дата вступления в силу изменения вычета льготы.</span><span class="sxs-lookup"><span data-stu-id="880cd-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="880cd-135">В эту дату система автоматически изменяет вычет льготы и обновляет все планы льгот, связанные с данным вычетом, при условии, что выполняется обработка **Обновление изменения вычета**.</span><span class="sxs-lookup"><span data-stu-id="880cd-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="880cd-136">**Изменение вычета завершено**</span><span class="sxs-lookup"><span data-stu-id="880cd-136">**Deduction change completed**</span></span> | <span data-ttu-id="880cd-137">Флажок **Изменение вычета завершено** будет выбран автоматически после того, как изменения вычета льгот завершены с помощью обработки изменения обновления вычета.</span><span class="sxs-lookup"><span data-stu-id="880cd-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="880cd-138">Чтобы отследить и настроить изменения настройки ставки льгот, выберите **Действия**, а затем выберите **Управление версиями**.</span><span class="sxs-lookup"><span data-stu-id="880cd-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="880cd-139">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="880cd-139">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]