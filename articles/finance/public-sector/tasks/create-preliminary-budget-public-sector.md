---
title: Создание предварительного бюджета для государственного сектора
description: Вы можете создать предварительные записи бюджетного регистра для определенной бюджетной модели и значений аналитик.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22538d58cc3499bd030848699d6c5831dfd8888a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975168"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="0a5cb-103">Создание предварительного бюджета для государственного сектора</span><span class="sxs-lookup"><span data-stu-id="0a5cb-103">Create a preliminary budget for Public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a5cb-104">Вы можете создать предварительные записи бюджетного регистра для определенной бюджетной модели и значений аналитик.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="0a5cb-105">После того как фактический бюджет будет утвержден, можно будет создать исходные записи бюджетного регистра.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="0a5cb-106">Эта процедура была создана с использованием демонстрационных данных компании PSUS в разделе государственного сектора.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="0a5cb-107">Перейдите в раздел "Бюджетирование" > "Записи бюджетного регистра".</span><span class="sxs-lookup"><span data-stu-id="0a5cb-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="0a5cb-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="0a5cb-108">Click New.</span></span>
3. <span data-ttu-id="0a5cb-109">В поле "Бюджетная модель" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0a5cb-110">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0a5cb-111">В поле "Код бюджета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0a5cb-112">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="0a5cb-113">В поле "Код основания" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0a5cb-114">В списке щелкните требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="0a5cb-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0a5cb-115">Click Save.</span></span>
10. <span data-ttu-id="0a5cb-116">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="0a5cb-116">Click Add line.</span></span>
    * <span data-ttu-id="0a5cb-117">Необязательно. Если вы хотите изменить дату в одном из заголовков, введите новую дату.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="0a5cb-118">Эта дата определяет финансовый период, для которого будет записан бюджет.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="0a5cb-119">При просмотре руководства по задаче для заполнения других полей щелкните "Разблокировать" в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="0a5cb-120">В поле "Структура счета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="0a5cb-121">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="0a5cb-122">В поле "Значения аналитик" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="0a5cb-123">В поле "Сумма" введите число.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="0a5cb-124">Можно также ввести тип суммы.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="0a5cb-125">В поле "Валюта" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="0a5cb-126">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="0a5cb-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0a5cb-127">Click Save.</span></span>
18. <span data-ttu-id="0a5cb-128">Щелкните "Обновить сальдо бюджета".</span><span class="sxs-lookup"><span data-stu-id="0a5cb-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="0a5cb-129">Щелкните Обновить.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-129">Click Update.</span></span>
    * <span data-ttu-id="0a5cb-130">Чтобы просмотреть результаты обновления, щелкните "Сведения о сообщении" на синей панели.</span><span class="sxs-lookup"><span data-stu-id="0a5cb-130">To see the results of the update, click Message details on the blue bar.</span></span>  

