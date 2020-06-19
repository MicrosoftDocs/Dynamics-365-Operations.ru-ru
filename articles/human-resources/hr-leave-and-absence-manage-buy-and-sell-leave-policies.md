---
title: Управление политиками покупки и продажи отпуска
description: Можно позволить сотрудникам покупать и продавать отпуск в Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429021"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="1af0a-103">Управление политиками покупки и продажи отпуска</span><span class="sxs-lookup"><span data-stu-id="1af0a-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="1af0a-104">Можно разрешить сотрудникам покупать отпуск, создав политику покупки отпуска.</span><span class="sxs-lookup"><span data-stu-id="1af0a-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="1af0a-105">Разрешение сотрудникам покупать и продавать отпуск</span><span class="sxs-lookup"><span data-stu-id="1af0a-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="1af0a-106">На странице **Параметры отпуска и отсутствия** выберите **Да**, чтобы **Разрешить сотрудникам покупать отпуск**.</span><span class="sxs-lookup"><span data-stu-id="1af0a-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="1af0a-107">Создание политики покупки отпуска</span><span class="sxs-lookup"><span data-stu-id="1af0a-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="1af0a-108">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="1af0a-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="1af0a-109">Выберите **Политика покупки и продажи отпуска**.</span><span class="sxs-lookup"><span data-stu-id="1af0a-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="1af0a-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1af0a-110">Select **New**.</span></span>

4. <span data-ttu-id="1af0a-111">Введите **Имя** и **Описание** политики в разделе **Политика покупки и продажи отпуска**.</span><span class="sxs-lookup"><span data-stu-id="1af0a-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="1af0a-112">Выбор **Тип политики**.</span><span class="sxs-lookup"><span data-stu-id="1af0a-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="1af0a-113">Доступными типами политик являются **Сумма** и **Часов в неделю**.</span><span class="sxs-lookup"><span data-stu-id="1af0a-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="1af0a-114">Выберите **Сумма** для ввода **Фиксированная сумма** для максимальной суммы, на которую сотрудники могут купить и продать.</span><span class="sxs-lookup"><span data-stu-id="1af0a-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="1af0a-115">Если выбрано **Часов в неделю**, для определения максимальной суммы политики используется рабочее время, определенное в назначенном календаре рабочего времени сотрудника.</span><span class="sxs-lookup"><span data-stu-id="1af0a-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="1af0a-116">Выберите **Дата начал** и **Дата окончания** для политики.</span><span class="sxs-lookup"><span data-stu-id="1af0a-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="1af0a-117">Запросы на покупку или продажу отпуска будут доступны для отправки только в течение этого временного интервала.</span><span class="sxs-lookup"><span data-stu-id="1af0a-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="1af0a-118">В разделе **Политика покупки** выберите значение **Эквивалент полной занятости** (FTE) для расчета максимальной суммы на основе FTE, определенного по должности сотрудника.</span><span class="sxs-lookup"><span data-stu-id="1af0a-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="1af0a-119">Если типом политики является **Сумма**, введите **Максимальная фиксированная сумма**.</span><span class="sxs-lookup"><span data-stu-id="1af0a-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="1af0a-120">Выберите **Добавить**, чтобы добавить типы отпуска для сотрудников для покупки отпуска.</span><span class="sxs-lookup"><span data-stu-id="1af0a-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="1af0a-121">В политику можно добавить несколько типов отпусков.</span><span class="sxs-lookup"><span data-stu-id="1af0a-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="1af0a-122">Введите **Месяцы службы** для типа отпуска, чтобы разрешить другие месяцы службы для определения максимальной суммы, на которую сотрудник может купить.</span><span class="sxs-lookup"><span data-stu-id="1af0a-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="1af0a-123">Введите **Максимальная сумма** для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="1af0a-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="1af0a-124">Введите **Ставка**, по которой сотрудник будет покупать отпуск.</span><span class="sxs-lookup"><span data-stu-id="1af0a-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="1af0a-125">При необходимости введите **Код дохода**, который будет использоваться для покупки отпуска.</span><span class="sxs-lookup"><span data-stu-id="1af0a-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="1af0a-126">При необходимости укажите, следует ли использовать FTE для определения максимальной суммы для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="1af0a-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="1af0a-127">Добавление политики покупки и продажи отпуска в план отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="1af0a-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="1af0a-128">На странице **Отпуск и отсутствие** выберите план отпусков и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="1af0a-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="1af0a-129">В разделе **Правила** выберите **Политика покупки и продажи отпуска**.</span><span class="sxs-lookup"><span data-stu-id="1af0a-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1af0a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="1af0a-130">See also</span></span>

[<span data-ttu-id="1af0a-131">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="1af0a-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="1af0a-132">Настройка типов отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="1af0a-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="1af0a-133">Начисление планов отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="1af0a-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="1af0a-134">Покупка и продажа отпуска</span><span class="sxs-lookup"><span data-stu-id="1af0a-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

