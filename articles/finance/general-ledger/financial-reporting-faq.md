---
title: Вопросы и ответы по финансовой отчетности
description: В этом разделе перечислены вопросы, касающиеся финансовой отчетности, которые возникли у других пользователей.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923033"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="17cc7-103">Вопросы и ответы по финансовой отчетности</span><span class="sxs-lookup"><span data-stu-id="17cc7-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="17cc7-104">В этом разделе представлены ответы на часто задаваемые вопросы о финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="17cc7-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="17cc7-105">Как ограничить доступ к отчету с помощью средств безопасности дерева?</span><span class="sxs-lookup"><span data-stu-id="17cc7-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="17cc7-106">В следующем примере показано, как ограничить доступ к отчету, используя средства безопасности дерева.</span><span class="sxs-lookup"><span data-stu-id="17cc7-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="17cc7-107">Демонстрационная компания USMF имеет балансовый отчет, который должен быть доступен не всем пользователям Financial Reporting.</span><span class="sxs-lookup"><span data-stu-id="17cc7-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="17cc7-108">Вы можете использовать средства безопасности дерева для ограничения доступа к отдельному отчету, В результате доступ к отчету будет только у определенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="17cc7-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="17cc7-109">Чтобы ограничить доступ, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="17cc7-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="17cc7-110">Войдите в Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="17cc7-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="17cc7-111">Создайте новое определение дерева.</span><span class="sxs-lookup"><span data-stu-id="17cc7-111">Create a new tree definition.</span></span> <span data-ttu-id="17cc7-112">Выберите **Файл > Создать > Определение дерева**.</span><span class="sxs-lookup"><span data-stu-id="17cc7-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="17cc7-113">Дважды щелкните строку **Сводка** в столбце **Безопасность блоков**.</span><span class="sxs-lookup"><span data-stu-id="17cc7-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="17cc7-114">Выберите **Пользователи и группы**.</span><span class="sxs-lookup"><span data-stu-id="17cc7-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="17cc7-115">Выберите пользователей или группу, которым требуется доступ к этому отчету.</span><span class="sxs-lookup"><span data-stu-id="17cc7-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="17cc7-116">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="17cc7-116">Select **Save**.</span></span>
7. <span data-ttu-id="17cc7-117">В определении отчета добавьте новое определение дерева.</span><span class="sxs-lookup"><span data-stu-id="17cc7-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="17cc7-118">В определении дерева выберите **Параметр**.</span><span class="sxs-lookup"><span data-stu-id="17cc7-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="17cc7-119">В разделе **Выбор элемента аналитической структуры** выберите **Включить все блоки**.</span><span class="sxs-lookup"><span data-stu-id="17cc7-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="17cc7-120">Как определить, какие счета вызывают несоответствие сальдо?</span><span class="sxs-lookup"><span data-stu-id="17cc7-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="17cc7-121">Если у вас есть отчет с несоответствующими сальдо, пот несколько шагов, которые можно предпринять, чтобы выявить проблемные счета и отклонения.</span><span class="sxs-lookup"><span data-stu-id="17cc7-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="17cc7-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="17cc7-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="17cc7-123">В Financial Reporter Report Designer создайте новое определение строки.</span><span class="sxs-lookup"><span data-stu-id="17cc7-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="17cc7-124">Выберите **Правка > Вставить строки из аналитик**.</span><span class="sxs-lookup"><span data-stu-id="17cc7-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="17cc7-125">Выберите **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="17cc7-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="17cc7-126">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="17cc7-126">Select **OK**.</span></span>
5. <span data-ttu-id="17cc7-127">Сохраните определение строки.</span><span class="sxs-lookup"><span data-stu-id="17cc7-127">Save the row definition.</span></span>
6. <span data-ttu-id="17cc7-128">Создайте новое определение столбца</span><span class="sxs-lookup"><span data-stu-id="17cc7-128">Create a new column definition</span></span>
7. <span data-ttu-id="17cc7-129">Создайте новое определение отчета.</span><span class="sxs-lookup"><span data-stu-id="17cc7-129">Create a new report definition.</span></span>
8. <span data-ttu-id="17cc7-130">Выберите **Параметры** и снимите флажок для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="17cc7-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="17cc7-131">Создайте отчет.</span><span class="sxs-lookup"><span data-stu-id="17cc7-131">Generate the report.</span></span> 
10. <span data-ttu-id="17cc7-132">Экспортируйте отчет в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="17cc7-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="17cc7-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="17cc7-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="17cc7-134">В Dynamics 365 Finance выберите **Главная книга > Запросы и отчеты > Пробный баланс**.</span><span class="sxs-lookup"><span data-stu-id="17cc7-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="17cc7-135">Настройте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="17cc7-135">Set the following parameters:</span></span>
   - <span data-ttu-id="17cc7-136">**Начальная дата** — введите начало финансового года.</span><span class="sxs-lookup"><span data-stu-id="17cc7-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="17cc7-137">**Конечная дата** — введите дату, для которой создается отчет.</span><span class="sxs-lookup"><span data-stu-id="17cc7-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="17cc7-138">**Финансовая аналитика** — установите для этого поля значение **Набор счета ГК**.</span><span class="sxs-lookup"><span data-stu-id="17cc7-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="17cc7-139">Выберите **Рассчитать**.</span><span class="sxs-lookup"><span data-stu-id="17cc7-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="17cc7-140">Экспортируйте отчет в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="17cc7-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="17cc7-141">Теперь можно скопировать данные из финансового отчета Excel в отчет пробного баланса, чтобы сравнить столбцы **Исходящее сальдо**.</span><span class="sxs-lookup"><span data-stu-id="17cc7-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]