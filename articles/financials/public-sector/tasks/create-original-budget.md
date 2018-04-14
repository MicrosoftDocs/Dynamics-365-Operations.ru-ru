--- 
title: "Создание исходного бюджета и реверсирование предварительных записей бюджета для государственного сектора"
description: "При создании записи исходного бюджета и использовании бюджетной модели и значений аналитики, которые содержат предварительные бюджетные суммы, предварительные бюджетные суммы можно реверсировать."
author: twheeloc
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e70c7f77ad0bb159f4cc037de895a83928c693c5
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="create-an-original-budget-and-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="f1d8e-103">Создание исходного бюджета и реверсирование предварительных записей бюджета для государственного сектора</span><span class="sxs-lookup"><span data-stu-id="f1d8e-103">Create an original budget and reverse preliminary budget entries in the public sector</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1d8e-104">При создании записи исходного бюджета и использовании бюджетной модели и значений аналитики, которые содержат предварительные бюджетные суммы, предварительные бюджетные суммы можно реверсировать.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="f1d8e-105">Эта процедура была создана с использованием демонстрационных данных компании PSUS в разделе государственного сектора.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="f1d8e-106">Перейдите в раздел "Бюджетирование" > "Записи бюджетного регистра".</span><span class="sxs-lookup"><span data-stu-id="f1d8e-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="f1d8e-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f1d8e-107">Click New.</span></span>
3. <span data-ttu-id="f1d8e-108">В поле "Бюджетная модель" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f1d8e-109">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f1d8e-110">В поле "Код бюджета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f1d8e-111">В списке щелкните "Исходный бюджет".</span><span class="sxs-lookup"><span data-stu-id="f1d8e-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="f1d8e-112">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-112">Click Save.</span></span>
8. <span data-ttu-id="f1d8e-113">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="f1d8e-113">Click Add line.</span></span>
9. <span data-ttu-id="f1d8e-114">Необязательно. Если вы хотите изменить дату в одном из заголовков, введите новую дату.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="f1d8e-115">Эта дата определяет финансовый период, для которого будет записан бюджет.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="f1d8e-116">В поле "Структура счета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f1d8e-117">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="f1d8e-118">В поле "Значения аналитик" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="f1d8e-119">В поле "Сумма" введите число.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="f1d8e-120">В поле "Валюта" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="f1d8e-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="f1d8e-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f1d8e-122">Click Save.</span></span>
17. <span data-ttu-id="f1d8e-123">Щелкните "Обновить сальдо бюджета".</span><span class="sxs-lookup"><span data-stu-id="f1d8e-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="f1d8e-124">Необязательно. Можно выбрать параметр реверсирования предварительного бюджета.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="f1d8e-125">Обратите внимание, что можно реверсировать как все записи предварительного бюджета, так и только те записи предварительного бюджета, которые имеют указанный код бюджета.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="f1d8e-126">Чтобы выбрать дополнительные параметры, щелкните значок "Разблокировать" в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="f1d8e-127">Щелкните Обновить.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-127">Click Update.</span></span>


