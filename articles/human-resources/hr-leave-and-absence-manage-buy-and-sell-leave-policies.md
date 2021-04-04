---
title: Управление политиками покупки и продажи отпуска
description: Можно позволить сотрудникам покупать и продавать отпуск в Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ccc6bf2e8b070e92cc4dbb98d8ec35ce60723516
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468091"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="7f591-103">Управление политиками покупки и продажи отпусков</span><span class="sxs-lookup"><span data-stu-id="7f591-103">Manage buy and sell leave policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7f591-104">Можно разрешить сотрудникам покупать и продавать отпуск, создав политику покупки и продажи отпуска.</span><span class="sxs-lookup"><span data-stu-id="7f591-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="7f591-105">Можно настроить эти политики для использования рабочего процесса для утверждений, установки максимальных сумм и ставок и установки ставок для покупки и продажи.</span><span class="sxs-lookup"><span data-stu-id="7f591-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="7f591-106">Разрешение сотрудникам покупать и продавать отпуск</span><span class="sxs-lookup"><span data-stu-id="7f591-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="7f591-107">На странице **Параметры отпуска и отсутствия** выберите **Да**, чтобы **Разрешить сотрудникам покупать отпуск** и **Разрешить сотрудникам продавать отпуск**.</span><span class="sxs-lookup"><span data-stu-id="7f591-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="7f591-108">Создание политики покупки и продажи отпуска</span><span class="sxs-lookup"><span data-stu-id="7f591-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="7f591-109">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="7f591-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="7f591-110">Выберите **Политика покупки и продажи отпуска**.</span><span class="sxs-lookup"><span data-stu-id="7f591-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="7f591-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7f591-111">Select **New**.</span></span>

4. <span data-ttu-id="7f591-112">Введите **Имя** и **Описание** политики в разделе **Политика покупки и продажи отпуска**.</span><span class="sxs-lookup"><span data-stu-id="7f591-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="7f591-113">Выбор **Тип политики**.</span><span class="sxs-lookup"><span data-stu-id="7f591-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="7f591-114">Доступными типами политик являются **Сумма** и **Часов в неделю**.</span><span class="sxs-lookup"><span data-stu-id="7f591-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="7f591-115">Выберите **Сумма** для ввода **Фиксированная сумма** для максимальной суммы, на которую сотрудники могут купить и продать.</span><span class="sxs-lookup"><span data-stu-id="7f591-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="7f591-116">Если выбрано **Часов в неделю**, для определения максимальной суммы политики используется рабочее время, определенное в назначенном календаре рабочего времени сотрудника.</span><span class="sxs-lookup"><span data-stu-id="7f591-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="7f591-117">Выберите **Дата начал** и **Дата окончания** для политики.</span><span class="sxs-lookup"><span data-stu-id="7f591-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="7f591-118">Запросы на покупку или продажу отпуска будут доступны для отправки только в течение этого временного интервала.</span><span class="sxs-lookup"><span data-stu-id="7f591-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="7f591-119">Выберите **Идентификатор рабочего процесса** для политики.</span><span class="sxs-lookup"><span data-stu-id="7f591-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="7f591-120">Любые запросы на покупку и продажу будут использовать этот рабочий процесс для проверки и утверждения.</span><span class="sxs-lookup"><span data-stu-id="7f591-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="7f591-121">В разделе **Политика покупки** выберите значение **Эквивалент полной занятости** (FTE) для расчета максимальной суммы на основе FTE, определенного по должности сотрудника.</span><span class="sxs-lookup"><span data-stu-id="7f591-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="7f591-122">Если типом политики является **Сумма**, введите **Максимальная фиксированная сумма**.</span><span class="sxs-lookup"><span data-stu-id="7f591-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="7f591-123">Выберите **Добавить**, чтобы добавить типы отпуска для сотрудников для покупки отпуска.</span><span class="sxs-lookup"><span data-stu-id="7f591-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="7f591-124">В политику можно добавить несколько типов отпусков.</span><span class="sxs-lookup"><span data-stu-id="7f591-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="7f591-125">Введите **Месяцы службы** для типа отпуска, чтобы разрешить другие месяцы службы для определения максимальной суммы, на которую сотрудник может купить.</span><span class="sxs-lookup"><span data-stu-id="7f591-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="7f591-126">Введите **Максимальная сумма** для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="7f591-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="7f591-127">Введите **Ставка**, по которой сотрудник будет покупать отпуск.</span><span class="sxs-lookup"><span data-stu-id="7f591-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="7f591-128">При необходимости введите **Код дохода**, который будет использоваться для покупки отпуска.</span><span class="sxs-lookup"><span data-stu-id="7f591-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="7f591-129">При необходимости укажите, следует ли использовать FTE для определения максимальной суммы для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="7f591-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="7f591-130">Чтобы создать политику продажи, выполните шаги с 8 по 14 в разделе **Политика продажи**.</span><span class="sxs-lookup"><span data-stu-id="7f591-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="7f591-131">Добавление политики покупки и продажи отпуска в план отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="7f591-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="7f591-132">На странице **Отпуск и отсутствие** выберите план отпусков и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="7f591-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="7f591-133">В разделе **Правила** выберите **Политика покупки и продажи отпуска**.</span><span class="sxs-lookup"><span data-stu-id="7f591-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f591-134">См. также</span><span class="sxs-lookup"><span data-stu-id="7f591-134">See also</span></span>

[<span data-ttu-id="7f591-135">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="7f591-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="7f591-136">Настройка типов отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="7f591-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="7f591-137">Начисление планов отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="7f591-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="7f591-138">Покупка и продажа отпуска</span><span class="sxs-lookup"><span data-stu-id="7f591-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]