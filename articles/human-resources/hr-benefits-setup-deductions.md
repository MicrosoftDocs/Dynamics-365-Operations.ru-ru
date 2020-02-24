---
title: Настройка вычетов
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010356"
---
# <a name="configure-deductions"></a><span data-ttu-id="8ca24-102">Настройка вычетов</span><span class="sxs-lookup"><span data-stu-id="8ca24-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="8ca24-103">Используйте вычеты в Microsoft Dynamics 365 Human Resources, чтобы определить, сколько (если применимо) необходимо вычесть из зарплаты сотруднику по чеку для каждой льготы.</span><span class="sxs-lookup"><span data-stu-id="8ca24-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="8ca24-104">Вычеты зависят от даты, поэтому можно хранить запись журнала с информацией о вычетах.</span><span class="sxs-lookup"><span data-stu-id="8ca24-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="8ca24-105">В рабочей области **Управление льготами** в разделе **Настройка** выберите **Вычеты**.</span><span class="sxs-lookup"><span data-stu-id="8ca24-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="8ca24-106">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="8ca24-106">Select **New**.</span></span>

3. <span data-ttu-id="8ca24-107">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="8ca24-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="8ca24-108">Поле</span><span class="sxs-lookup"><span data-stu-id="8ca24-108">Field</span></span> | <span data-ttu-id="8ca24-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8ca24-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="8ca24-110">Вычет</span><span class="sxs-lookup"><span data-stu-id="8ca24-110">Deduction</span></span> | <span data-ttu-id="8ca24-111">Уникальный код, используемый для идентификации вычета льготы.</span><span class="sxs-lookup"><span data-stu-id="8ca24-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="8ca24-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8ca24-112">Description</span></span> | <span data-ttu-id="8ca24-113">Описание вычета.</span><span class="sxs-lookup"><span data-stu-id="8ca24-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="8ca24-114">Действует</span><span class="sxs-lookup"><span data-stu-id="8ca24-114">Effective</span></span> | <span data-ttu-id="8ca24-115">Дата начала.</span><span class="sxs-lookup"><span data-stu-id="8ca24-115">The start date.</span></span> <span data-ttu-id="8ca24-116">Значение по умолчанию — текущая системная дата.</span><span class="sxs-lookup"><span data-stu-id="8ca24-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="8ca24-117">Истечение срока действия</span><span class="sxs-lookup"><span data-stu-id="8ca24-117">Expiration</span></span> | <span data-ttu-id="8ca24-118">Дата окончания.</span><span class="sxs-lookup"><span data-stu-id="8ca24-118">The end date.</span></span> <span data-ttu-id="8ca24-119">Значение по умолчанию — 12/31/2154, что означает "никогда".</span><span class="sxs-lookup"><span data-stu-id="8ca24-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="8ca24-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8ca24-120">Heading</span></span> | <span data-ttu-id="8ca24-121">Код заголовка из системы зарплаты, который будет использоваться данным вычетом для сотрудника в части вычета при обработке льгот для зарплаты.</span><span class="sxs-lookup"><span data-stu-id="8ca24-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="8ca24-122">Используется при использовании стороннего поставщика зарплаты.</span><span class="sxs-lookup"><span data-stu-id="8ca24-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="8ca24-123">Ссылка сотрудника для вычета из зарплаты</span><span class="sxs-lookup"><span data-stu-id="8ca24-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="8ca24-124">Код вычета из системы расчета зарплаты, который этот вычет будет использовать для доли сотрудника в вычете при обработке льгот для зарплаты.</span><span class="sxs-lookup"><span data-stu-id="8ca24-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="8ca24-125">Заголовок суммы</span><span class="sxs-lookup"><span data-stu-id="8ca24-125">Amount heading</span></span> | <span data-ttu-id="8ca24-126">Код заголовка из системы зарплаты, который будет использоваться суммой вычета для сотрудника в части вычета при обработке льгот для зарплаты.</span><span class="sxs-lookup"><span data-stu-id="8ca24-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="8ca24-127">Обычно используется при использовании стороннего поставщика зарплаты.</span><span class="sxs-lookup"><span data-stu-id="8ca24-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="8ca24-128">Может удалять</span><span class="sxs-lookup"><span data-stu-id="8ca24-128">Can delete</span></span> | <span data-ttu-id="8ca24-129">Указывает, может ли экспортированное значение из Dynamics 365 for Finance and Operations быть причиной удаления значения в системе зарплаты.</span><span class="sxs-lookup"><span data-stu-id="8ca24-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="8ca24-130">Парные столбцы</span><span class="sxs-lookup"><span data-stu-id="8ca24-130">Paired columns</span></span> | <span data-ttu-id="8ca24-131">Указывает, следует ли экспортировать заголовок и сумму вычета в парные смежные столбцы в системе зарплаты.</span><span class="sxs-lookup"><span data-stu-id="8ca24-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="8ca24-132">Дата вступления изменения в силу</span><span class="sxs-lookup"><span data-stu-id="8ca24-132">Change effective date</span></span> | <span data-ttu-id="8ca24-133">Дата вступления в силу изменения вычета льготы.</span><span class="sxs-lookup"><span data-stu-id="8ca24-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="8ca24-134">В эту дату система автоматически изменит вычет льготы и обновит все планы льгот, связанные с данным вычетом, при условии, что выполняется обработка обновления изменения вычета.</span><span class="sxs-lookup"><span data-stu-id="8ca24-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="8ca24-135">Изменение вычета завершено</span><span class="sxs-lookup"><span data-stu-id="8ca24-135">Deduction change completed</span></span> | <span data-ttu-id="8ca24-136">Флажок завершенного изменения вычета будет выбран автоматически после того, как изменения вычета льгот завершены с помощью обработки изменения обновления вычета.</span><span class="sxs-lookup"><span data-stu-id="8ca24-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="8ca24-137">Чтобы отследить и настроить изменения настройки ставки льгот, выберите **Действия**, а затем выберите **Управление версиями**.</span><span class="sxs-lookup"><span data-stu-id="8ca24-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="8ca24-138">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8ca24-138">Select **Save**.</span></span> 
