---
title: Обработка чеков по расходам
description: В этой теме содержатся сведения об обработке распознавания текста символов для чеков. Эта функция предназначена для улучшения работы при создании отчетов по расходам в Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 49cdfeac8cda9f1ddd3aca61f902f00f30f3485b
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154048"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="72c4c-104">Обработка чеков по расходам</span><span class="sxs-lookup"><span data-stu-id="72c4c-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


<span data-ttu-id="72c4c-105">Запись о расходах была улучшена с помощью введения обработки распознавания текста для чеков.</span><span class="sxs-lookup"><span data-stu-id="72c4c-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="72c4c-106">Эта функция предназначена для улучшения работы при создании отчетов по расходам.</span><span class="sxs-lookup"><span data-stu-id="72c4c-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="72c4c-107">Ключевые возможности</span><span class="sxs-lookup"><span data-stu-id="72c4c-107">Key features</span></span>

- <span data-ttu-id="72c4c-108">Наименование получателя платежа, дата и общая сумма извлекаются из чеков.</span><span class="sxs-lookup"><span data-stu-id="72c4c-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="72c4c-109">Функция пытается сопоставить несвязанные чеки с несвязанными расходными проводками.</span><span class="sxs-lookup"><span data-stu-id="72c4c-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="72c4c-110">Пользователи могут создавать проводки по расходам, введенные вручную, из чеков.</span><span class="sxs-lookup"><span data-stu-id="72c4c-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="72c4c-111">Примеры использования</span><span class="sxs-lookup"><span data-stu-id="72c4c-111">Usage examples</span></span>

- <span data-ttu-id="72c4c-112">**Автоматическая привязка чеков, включающих проводки по кредитным картам, при создании отчета о расходах.**</span><span class="sxs-lookup"><span data-stu-id="72c4c-112">**Automatically attach receipts that include credit card transactions when an expense report is created.**</span></span>

    1. <span data-ttu-id="72c4c-113">Откройте рабочую область **Управление расходами**.</span><span class="sxs-lookup"><span data-stu-id="72c4c-113">Open the **Expense management** workspace.</span></span>
    2. <span data-ttu-id="72c4c-114">На вкладке **Чеки** убедитесь, что имеются несвязанные чеки.</span><span class="sxs-lookup"><span data-stu-id="72c4c-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="72c4c-115">Можно также загрузить чеки на вкладке **Чеки**.</span><span class="sxs-lookup"><span data-stu-id="72c4c-115">You can also upload receipts on the **Receipts** tab.</span></span>
    3. <span data-ttu-id="72c4c-116">На вкладке **Расходы** убедитесь, что имеются несвязанные расходы.</span><span class="sxs-lookup"><span data-stu-id="72c4c-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="72c4c-117">Обычно администратор по расходам импортирует эти расходы от поставщика кредитных карт.</span><span class="sxs-lookup"><span data-stu-id="72c4c-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
    4. <span data-ttu-id="72c4c-118">Выберите **Создать отчет по расходам**.</span><span class="sxs-lookup"><span data-stu-id="72c4c-118">Select **New expense report**.</span></span> <span data-ttu-id="72c4c-119">Обратите внимание, что теперь при создании отчета по расходам можно также включить расходы и чеки.</span><span class="sxs-lookup"><span data-stu-id="72c4c-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="72c4c-120">При добавлении расходов и чеков включается автоматическое сопоставление чеков с расходами.</span><span class="sxs-lookup"><span data-stu-id="72c4c-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

- <span data-ttu-id="72c4c-121">**Создание расхода или сопоставление расхода из чека.**</span><span class="sxs-lookup"><span data-stu-id="72c4c-121">**Create an expense, or match an expense from a receipt.**</span></span>

    1. <span data-ttu-id="72c4c-122">В отчете о расходах на вкладке **Чеки** приложите чек, выбрав **Добавить чеки**.</span><span class="sxs-lookup"><span data-stu-id="72c4c-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
    2. <span data-ttu-id="72c4c-123">В отправленном изображении чека обратите внимание на параметры **Создать** и **Сопоставить**.</span><span class="sxs-lookup"><span data-stu-id="72c4c-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

        - <span data-ttu-id="72c4c-124">Выберите **Создать**, чтобы создать введенную вручную проводку расхода и ввести значения, извлеченные из чека.</span><span class="sxs-lookup"><span data-stu-id="72c4c-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
        - <span data-ttu-id="72c4c-125">Если выбрано **Сопоставить**, система пытается выполнить сопоставление по существующему расходу для чека.</span><span class="sxs-lookup"><span data-stu-id="72c4c-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="72c4c-126">Установка</span><span class="sxs-lookup"><span data-stu-id="72c4c-126">Installation</span></span>

<span data-ttu-id="72c4c-127">Эта возможность используется вместе с функцией **Повторно сформированные отчеты о расходах**, чтобы упростить процесс расходов.</span><span class="sxs-lookup"><span data-stu-id="72c4c-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span>

<span data-ttu-id="72c4c-128">Чтобы использовать эти дополнительные возможности по расходам, установите надстройку службы управления расходами для Microsoft Dynamics 365 Finance и включите функции в своем экземпляре.</span><span class="sxs-lookup"><span data-stu-id="72c4c-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="72c4c-129">Можно получить доступ к надстройке из своего проекта Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="72c4c-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="72c4c-130">Выполните вход в LCS и откройте нужную среду.</span><span class="sxs-lookup"><span data-stu-id="72c4c-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="72c4c-131">Перейдите **Полные сведения**.</span><span class="sxs-lookup"><span data-stu-id="72c4c-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="72c4c-132">Выберите **Поддержка** или перейдите на экспресс-вкладку **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="72c4c-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="72c4c-133">Выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="72c4c-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="72c4c-134">Выберите **Службу управления расходами**.</span><span class="sxs-lookup"><span data-stu-id="72c4c-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="72c4c-135">Следуйте указаниям руководства по установке и примите условия и положения.</span><span class="sxs-lookup"><span data-stu-id="72c4c-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="72c4c-136">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="72c4c-136">Select **Install**.</span></span>

<span data-ttu-id="72c4c-137">В рабочей области **Управление функциями** включите следующие функции:</span><span class="sxs-lookup"><span data-stu-id="72c4c-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="72c4c-138">Повторно сформированные отчеты о расходах</span><span class="sxs-lookup"><span data-stu-id="72c4c-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="72c4c-139">Автоматическое сопоставление и создание расхода из чека</span><span class="sxs-lookup"><span data-stu-id="72c4c-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="72c4c-140">При включении этих функций выполняются следующие действия:</span><span class="sxs-lookup"><span data-stu-id="72c4c-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="72c4c-141">Существующая рабочая область **Управление расходами** заменяется новой рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="72c4c-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="72c4c-142">Добавляется новый пункт меню для отображения поля расходов.</span><span class="sxs-lookup"><span data-stu-id="72c4c-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="72c4c-143">Страницу **Отчеты по расходам** можно открыть, перейдя в **Управление расходами > Мои расходы > Отчеты по расходам**.</span><span class="sxs-lookup"><span data-stu-id="72c4c-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="72c4c-144">Рабочие процессы и любые утверждения по прежнему ведут на существующую страницу отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="72c4c-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="72c4c-145">Чеки будут обрабатываться через Microsoft Azure Cognitive Services, и метаданные будут извлечены и добавлены.</span><span class="sxs-lookup"><span data-stu-id="72c4c-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="72c4c-146">Добавлен параметр, позволяющий создать отчет по расходам, который включает сопоставленные несвязанные чеки.</span><span class="sxs-lookup"><span data-stu-id="72c4c-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="72c4c-147">Параметр, который добавляется к отчетам о расходах, позволяет создать строку расходов из чека, или пытается сопоставить существующий чек с существующей строкой расходов.</span><span class="sxs-lookup"><span data-stu-id="72c4c-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="72c4c-148">Дополнительные сведения о функции повторно сформированных отчеты о расходах см. в разделе [Повторно сформированные отчеты о расходах](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="72c4c-148">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="72c4c-149">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="72c4c-149">Frequently asked questions</span></span>

<span data-ttu-id="72c4c-150">**Используют ли Microsoft мои данные для моделей?**</span><span class="sxs-lookup"><span data-stu-id="72c4c-150">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="72c4c-151">Нет, корпорация Майкрософт создала общую модель машинного обучения для службы обработки чеков.</span><span class="sxs-lookup"><span data-stu-id="72c4c-151">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="72c4c-152">Эта модель не основана на отправленных чеках.</span><span class="sxs-lookup"><span data-stu-id="72c4c-152">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="72c4c-153">**Где доступна и обрабатывается эта функция?**</span><span class="sxs-lookup"><span data-stu-id="72c4c-153">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="72c4c-154">В настоящее время поддерживаются США.</span><span class="sxs-lookup"><span data-stu-id="72c4c-154">Currently, the United States is supported.</span></span>

<span data-ttu-id="72c4c-155">**Куда поступают мои чеки?**</span><span class="sxs-lookup"><span data-stu-id="72c4c-155">**Where do my receipts go?**</span></span>

<span data-ttu-id="72c4c-156">Finance будет обращаться в Cognitive Services, чтобы извлечь данные полей.</span><span class="sxs-lookup"><span data-stu-id="72c4c-156">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="72c4c-157">Cognitive Services хранят копию вашего чека до 24 часов с момента обработки.</span><span class="sxs-lookup"><span data-stu-id="72c4c-157">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="72c4c-158">После завершения обработки чек будет удален из Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="72c4c-158">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="72c4c-159">Чеки по-прежнему хранятся в Finance.</span><span class="sxs-lookup"><span data-stu-id="72c4c-159">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="72c4c-160">Дополнительные сведения см. в разделе [Включение распознавания чеков с новыми возможностями распознавателя форм](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="72c4c-160">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
