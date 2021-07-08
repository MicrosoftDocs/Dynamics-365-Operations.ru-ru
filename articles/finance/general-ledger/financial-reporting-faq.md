---
title: Вопросы и ответы по финансовой отчетности
description: В этом разделе представлены некоторые ответы на часто задаваемые вопросы о финансовой отчетности.
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266641"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="53b02-103">Вопросы и ответы по финансовой отчетности</span><span class="sxs-lookup"><span data-stu-id="53b02-103">Financial reporting FAQ</span></span>

<span data-ttu-id="53b02-104">В этом разделе представлены ответы на часто задаваемые вопросы о финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="53b02-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="53b02-105">Как ограничить доступ к отчету с помощью средств безопасности дерева?</span><span class="sxs-lookup"><span data-stu-id="53b02-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="53b02-106">В следующем примере показано, как ограничить доступ к отчету, используя средства безопасности дерева.</span><span class="sxs-lookup"><span data-stu-id="53b02-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="53b02-107">Демонстрационная компания USMF имеет отчет **Балансовый отчет**, который должен быть доступен не всем пользователям финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="53b02-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="53b02-108">Можно использовать средства безопасности дерева для ограничения доступа к одному отчету, чтобы доступ к отчету имели только определенные пользователи.</span><span class="sxs-lookup"><span data-stu-id="53b02-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="53b02-109">Вход в Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="53b02-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="53b02-110">Выберите **Файл \> Создать \> Определение дерева**, чтобы создать новое определение дерева.</span><span class="sxs-lookup"><span data-stu-id="53b02-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="53b02-111">Дважды коснитесь (или дважды щелкните) строку **Сводка** в столбце **Безопасность блоков**.</span><span class="sxs-lookup"><span data-stu-id="53b02-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="53b02-112">Выберите **Пользователи и группы**.</span><span class="sxs-lookup"><span data-stu-id="53b02-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="53b02-113">Выберите пользователей или группу, которым требуется доступ к отчету.</span><span class="sxs-lookup"><span data-stu-id="53b02-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="53b02-114">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="53b02-114">Select **Save**.</span></span>
7. <span data-ttu-id="53b02-115">В определении отчета добавьте новое определение дерева.</span><span class="sxs-lookup"><span data-stu-id="53b02-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="53b02-116">В определении дерева выберите **Параметр**.</span><span class="sxs-lookup"><span data-stu-id="53b02-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="53b02-117">Затем в разделе **Выбор элемента аналитической структуры** выберите **Включить все блоки**.</span><span class="sxs-lookup"><span data-stu-id="53b02-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="53b02-118">Как определить, какие счета вызывают несоответствие сальдо?</span><span class="sxs-lookup"><span data-stu-id="53b02-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="53b02-119">Если у вас есть отчет с несоответствующими сальдо, используйте следующие процедуры, чтобы определить каждый счет и отклонение.</span><span class="sxs-lookup"><span data-stu-id="53b02-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="53b02-120">В Financial Reporter Report Designer</span><span class="sxs-lookup"><span data-stu-id="53b02-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="53b02-121">Создайте новое определение строки.</span><span class="sxs-lookup"><span data-stu-id="53b02-121">Create a new row definition.</span></span>
2. <span data-ttu-id="53b02-122">Выберите **Правка \> Вставить строки из аналитик**.</span><span class="sxs-lookup"><span data-stu-id="53b02-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="53b02-123">Выберите **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="53b02-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="53b02-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="53b02-124">Select **OK**.</span></span>
5. <span data-ttu-id="53b02-125">Сохраните определение строки.</span><span class="sxs-lookup"><span data-stu-id="53b02-125">Save the row definition.</span></span>
6. <span data-ttu-id="53b02-126">Создайте новое определение столбца.</span><span class="sxs-lookup"><span data-stu-id="53b02-126">Create a new column definition.</span></span>
7. <span data-ttu-id="53b02-127">Создайте новое определение отчета.</span><span class="sxs-lookup"><span data-stu-id="53b02-127">Create a new report definition.</span></span>
8. <span data-ttu-id="53b02-128">Выберите **Параметры** и снимите флажок для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="53b02-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="53b02-129">Создайте отчет.</span><span class="sxs-lookup"><span data-stu-id="53b02-129">Generate the report.</span></span> 
10. <span data-ttu-id="53b02-130">Экспортируйте отчет в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="53b02-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="53b02-131">В Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="53b02-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="53b02-132">Перейдите в раздел **Главная книга \> Запросы и отчеты \> Пробный баланс**.</span><span class="sxs-lookup"><span data-stu-id="53b02-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="53b02-133">Задайте значения в следующих полях:</span><span class="sxs-lookup"><span data-stu-id="53b02-133">Set the following fields:</span></span>

    - <span data-ttu-id="53b02-134">**Дата начала** — введите дату начала финансового года.</span><span class="sxs-lookup"><span data-stu-id="53b02-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="53b02-135">**Дата окончания** — введите дату, для которой создается отчет.</span><span class="sxs-lookup"><span data-stu-id="53b02-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="53b02-136">**Финансовая аналитика** — установите для этого поля значение **Набор счета ГК**.</span><span class="sxs-lookup"><span data-stu-id="53b02-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="53b02-137">Выберите **Рассчитать**.</span><span class="sxs-lookup"><span data-stu-id="53b02-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="53b02-138">Экспортируйте отчет в Excel.</span><span class="sxs-lookup"><span data-stu-id="53b02-138">Export the report to Excel.</span></span>

<span data-ttu-id="53b02-139">Теперь можно скопировать данные из отчета Excel Financial Reporter в отчет **Пробный баланс**, чтобы сравнить столбцы **Исходящее сальдо**.</span><span class="sxs-lookup"><span data-stu-id="53b02-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="53b02-140">При разработке отчета в Report Designer или при создании финансового отчета я получаю следующее сообщение: "Не удалось завершить операцию из-за проблемы в структуре поставщика данных".</span><span class="sxs-lookup"><span data-stu-id="53b02-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="53b02-141">Как мне реагировать?</span><span class="sxs-lookup"><span data-stu-id="53b02-141">How should I respond?</span></span>

<span data-ttu-id="53b02-142">Сообщение указывает на то, что возникла проблема при попытке системы извлечь финансовые метаданные из киоска данных при использовании финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="53b02-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="53b02-143">Существует два способа решения этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="53b02-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="53b02-144">Проверьте состояние интеграции данных в разделе **Сервис \> Состояние интеграции** в Report Designer.</span><span class="sxs-lookup"><span data-stu-id="53b02-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="53b02-145">Если интеграция не завершена, дождитесь ее завершения.</span><span class="sxs-lookup"><span data-stu-id="53b02-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="53b02-146">Затем повторите попытку выполнить действие, которое вы пытались выполнить, когда получили сообщение.</span><span class="sxs-lookup"><span data-stu-id="53b02-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="53b02-147">Обратитесь в службу поддержки, чтобы определить и решить эту проблему.</span><span class="sxs-lookup"><span data-stu-id="53b02-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="53b02-148">В системе могут быть противоречивые данные.</span><span class="sxs-lookup"><span data-stu-id="53b02-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="53b02-149">Специалисты службы поддержки могут помочь определить эту проблему на сервере и найти необходимые данные, которые может потребоваться обновить.</span><span class="sxs-lookup"><span data-stu-id="53b02-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
