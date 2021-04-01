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
ms.openlocfilehash: 40371809f3855e57db4bc12f5466f7cef5cec600
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235564"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="e1f10-103">Создание предварительного бюджета для государственного сектора</span><span class="sxs-lookup"><span data-stu-id="e1f10-103">Create a preliminary budget for Public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1f10-104">Вы можете создать предварительные записи бюджетного регистра для определенной бюджетной модели и значений аналитик.</span><span class="sxs-lookup"><span data-stu-id="e1f10-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="e1f10-105">После того как фактический бюджет будет утвержден, можно будет создать исходные записи бюджетного регистра.</span><span class="sxs-lookup"><span data-stu-id="e1f10-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="e1f10-106">Эта процедура была создана с использованием демонстрационных данных компании PSUS в разделе государственного сектора.</span><span class="sxs-lookup"><span data-stu-id="e1f10-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="e1f10-107">Перейдите в раздел "Бюджетирование" > "Записи бюджетного регистра".</span><span class="sxs-lookup"><span data-stu-id="e1f10-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="e1f10-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e1f10-108">Click New.</span></span>
3. <span data-ttu-id="e1f10-109">В поле "Бюджетная модель" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e1f10-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e1f10-110">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="e1f10-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e1f10-111">В поле "Код бюджета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e1f10-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e1f10-112">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="e1f10-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e1f10-113">В поле "Код основания" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e1f10-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e1f10-114">В списке щелкните требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="e1f10-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="e1f10-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e1f10-115">Click Save.</span></span>
10. <span data-ttu-id="e1f10-116">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="e1f10-116">Click Add line.</span></span>
    * <span data-ttu-id="e1f10-117">Необязательно. Если вы хотите изменить дату в одном из заголовков, введите новую дату.</span><span class="sxs-lookup"><span data-stu-id="e1f10-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="e1f10-118">Эта дата определяет финансовый период, для которого будет записан бюджет.</span><span class="sxs-lookup"><span data-stu-id="e1f10-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="e1f10-119">При просмотре руководства по задаче для заполнения других полей щелкните "Разблокировать" в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="e1f10-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="e1f10-120">В поле "Структура счета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e1f10-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="e1f10-121">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="e1f10-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="e1f10-122">В поле "Значения аналитик" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="e1f10-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="e1f10-123">В поле "Сумма" введите число.</span><span class="sxs-lookup"><span data-stu-id="e1f10-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="e1f10-124">Можно также ввести тип суммы.</span><span class="sxs-lookup"><span data-stu-id="e1f10-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="e1f10-125">В поле "Валюта" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e1f10-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="e1f10-126">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="e1f10-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="e1f10-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e1f10-127">Click Save.</span></span>
18. <span data-ttu-id="e1f10-128">Щелкните "Обновить сальдо бюджета".</span><span class="sxs-lookup"><span data-stu-id="e1f10-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="e1f10-129">Щелкните Обновить.</span><span class="sxs-lookup"><span data-stu-id="e1f10-129">Click Update.</span></span>
    * <span data-ttu-id="e1f10-130">Чтобы просмотреть результаты обновления, щелкните "Сведения о сообщении" на синей панели.</span><span class="sxs-lookup"><span data-stu-id="e1f10-130">To see the results of the update, click Message details on the blue bar.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]