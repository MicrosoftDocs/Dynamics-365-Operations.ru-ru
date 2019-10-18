---
title: Создание кода процента с диапазоном
description: Коды процента можно настроить для расчета различных сумм процента на основе диапазона значений.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d684eedd5b40ee9775ab779c243d05cdc6e01f58
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188863"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="51412-103">Создание кода процента с диапазоном</span><span class="sxs-lookup"><span data-stu-id="51412-103">Create an interest code with a range</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51412-104">Коды процента можно настроить для расчета различных сумм процента на основе диапазона значений.</span><span class="sxs-lookup"><span data-stu-id="51412-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="51412-105">В этой процедуре показано, как добавить код процента и добавить в него диапазон.</span><span class="sxs-lookup"><span data-stu-id="51412-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="51412-106">Перейдите в раздел "Кредит и коллекции" > "Процент" > "Настройка кодов процентов".</span><span class="sxs-lookup"><span data-stu-id="51412-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="51412-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="51412-107">Click New.</span></span>
3. <span data-ttu-id="51412-108">В поле "Код процента" введите полное имя кода процента.</span><span class="sxs-lookup"><span data-stu-id="51412-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="51412-109">В поле "Описание" введите описание кода процента.</span><span class="sxs-lookup"><span data-stu-id="51412-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="51412-110">Выберите месяц.</span><span class="sxs-lookup"><span data-stu-id="51412-110">Select Month.</span></span>
6. <span data-ttu-id="51412-111">Разверните раздел "Доход".</span><span class="sxs-lookup"><span data-stu-id="51412-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="51412-112">Разверните раздел "Прибыль по валюте".</span><span class="sxs-lookup"><span data-stu-id="51412-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="51412-113">В поле "Счет для разноски ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="51412-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="51412-114">В поле "Проценты по диапазону" выберите "Месяцы".</span><span class="sxs-lookup"><span data-stu-id="51412-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="51412-115">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="51412-115">Click Add.</span></span>
11. <span data-ttu-id="51412-116">В поле "Описание" введите описание текущей валюты и диапазона.</span><span class="sxs-lookup"><span data-stu-id="51412-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="51412-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="51412-117">Click Save.</span></span>
13. <span data-ttu-id="51412-118">Щелкните "Диапазоны".</span><span class="sxs-lookup"><span data-stu-id="51412-118">Click Ranges.</span></span>
14. <span data-ttu-id="51412-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="51412-119">Click New.</span></span>
15. <span data-ttu-id="51412-120">Введите 0 в качестве значения "С", а затем введите процент в месяц, который будет использоваться для расчета процента.</span><span class="sxs-lookup"><span data-stu-id="51412-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="51412-121">В нашем примере он равен 1,5.</span><span class="sxs-lookup"><span data-stu-id="51412-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="51412-122">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="51412-122">Click New.</span></span>
17. <span data-ttu-id="51412-123">Введите следующее значение "С" как 4, что означает первый месяц, когда будет рассчитываться новый уровень процентов.</span><span class="sxs-lookup"><span data-stu-id="51412-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="51412-124">Введите процент в месяц, который будет использоваться для расчета процента начиная с месяца 4.</span><span class="sxs-lookup"><span data-stu-id="51412-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="51412-125"> В этом примере он равен 2,0.</span><span class="sxs-lookup"><span data-stu-id="51412-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="51412-126">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="51412-126">Click New.</span></span>
20. <span data-ttu-id="51412-127">Введите следующее значение "С" как 7, что означает следующий месяц, с которого будет рассчитываться новый уровень процентов.</span><span class="sxs-lookup"><span data-stu-id="51412-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="51412-128">Введите процент в месяц, который будет использоваться для расчета процента начиная с месяца 7.</span><span class="sxs-lookup"><span data-stu-id="51412-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="51412-129">В этом примере он равен 2,5.</span><span class="sxs-lookup"><span data-stu-id="51412-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="51412-130">Щелкните "Закрыть", чтобы завершить настройку.</span><span class="sxs-lookup"><span data-stu-id="51412-130">Click Close to complete the setup.</span></span>

