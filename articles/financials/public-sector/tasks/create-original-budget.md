---
title: Создание исходного бюджета, а затем реверсирование предварительных записей бюджета для государственного сектора
description: При создании записи исходного бюджета и использовании бюджетной модели и значений аналитики, которые содержат предварительные бюджетные суммы, предварительные бюджетные суммы можно реверсировать.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d1c34ac2bd94196b7bad599e9aca7ed942ae9c8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "344946"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="46a5b-103">Создание исходного бюджета, а затем реверсирование предварительных записей бюджета для государственного сектора</span><span class="sxs-lookup"><span data-stu-id="46a5b-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46a5b-104">При создании записи исходного бюджета и использовании бюджетной модели и значений аналитики, которые содержат предварительные бюджетные суммы, предварительные бюджетные суммы можно реверсировать.</span><span class="sxs-lookup"><span data-stu-id="46a5b-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="46a5b-105">Эта процедура была создана с использованием демонстрационных данных компании PSUS в разделе государственного сектора.</span><span class="sxs-lookup"><span data-stu-id="46a5b-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="46a5b-106">Перейдите в раздел "Бюджетирование" > "Записи бюджетного регистра".</span><span class="sxs-lookup"><span data-stu-id="46a5b-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="46a5b-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="46a5b-107">Click New.</span></span>
3. <span data-ttu-id="46a5b-108">В поле "Бюджетная модель" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="46a5b-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="46a5b-109">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="46a5b-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="46a5b-110">В поле "Код бюджета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="46a5b-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="46a5b-111">В списке щелкните "Исходный бюджет".</span><span class="sxs-lookup"><span data-stu-id="46a5b-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="46a5b-112">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="46a5b-112">Click Save.</span></span>
8. <span data-ttu-id="46a5b-113">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="46a5b-113">Click Add line.</span></span>
9. <span data-ttu-id="46a5b-114">Необязательно. Если вы хотите изменить дату в одном из заголовков, введите новую дату.</span><span class="sxs-lookup"><span data-stu-id="46a5b-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="46a5b-115">Эта дата определяет финансовый период, для которого будет записан бюджет.</span><span class="sxs-lookup"><span data-stu-id="46a5b-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="46a5b-116">В поле "Структура счета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="46a5b-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="46a5b-117">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="46a5b-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="46a5b-118">В поле "Значения аналитик" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="46a5b-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="46a5b-119">В поле "Сумма" введите число.</span><span class="sxs-lookup"><span data-stu-id="46a5b-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="46a5b-120">В поле "Валюта" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="46a5b-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="46a5b-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="46a5b-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="46a5b-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="46a5b-122">Click Save.</span></span>
17. <span data-ttu-id="46a5b-123">Щелкните "Обновить сальдо бюджета".</span><span class="sxs-lookup"><span data-stu-id="46a5b-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="46a5b-124">Необязательно. Можно выбрать параметр реверсирования предварительного бюджета.</span><span class="sxs-lookup"><span data-stu-id="46a5b-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="46a5b-125">Обратите внимание, что можно реверсировать как все записи предварительного бюджета, так и только те записи предварительного бюджета, которые имеют указанный код бюджета.</span><span class="sxs-lookup"><span data-stu-id="46a5b-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="46a5b-126">Чтобы выбрать дополнительные параметры, щелкните значок "Разблокировать" в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="46a5b-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="46a5b-127">Щелкните Обновить.</span><span class="sxs-lookup"><span data-stu-id="46a5b-127">Click Update.</span></span>

