--- 
title: "Сопоставление моделей для использования финансовых аналитик как источника данных для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a3eafa7b66dcc0c2481d7eeaf98bed7f58e4be33
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="5637b-103">Сопоставление моделей для использования финансовых аналитик как источника данных для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="5637b-103">Map models  to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5637b-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="5637b-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="5637b-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="5637b-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="5637b-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 1. Модель проектных данных)".</span><span class="sxs-lookup"><span data-stu-id="5637b-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="5637b-107">Добавление необходимых источников данных в сопоставление модели</span><span class="sxs-lookup"><span data-stu-id="5637b-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="5637b-108">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="5637b-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="5637b-109">В дереве выберите "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="5637b-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="5637b-110">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="5637b-110">Click Designer.</span></span>
4. <span data-ttu-id="5637b-111">Щелкните "Сопоставить модель с источником данных".</span><span class="sxs-lookup"><span data-stu-id="5637b-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="5637b-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="5637b-112">Click New.</span></span>
6. <span data-ttu-id="5637b-113">В поле "Определение" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="5637b-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="5637b-114">В поле "Имя" введите "Сопоставление данные аналитик".</span><span class="sxs-lookup"><span data-stu-id="5637b-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="5637b-115">В поле "Описание" введите "Сопоставление данные аналитик".</span><span class="sxs-lookup"><span data-stu-id="5637b-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="5637b-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="5637b-116">Click Save.</span></span>
10. <span data-ttu-id="5637b-117">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="5637b-117">Click Designer.</span></span>
11. <span data-ttu-id="5637b-118">В дереве выберите "Dynamics 365 for Operations\Таблица".</span><span class="sxs-lookup"><span data-stu-id="5637b-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="5637b-119">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="5637b-119">Click Add root.</span></span>
13. <span data-ttu-id="5637b-120">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="5637b-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="5637b-121">В поле "Таблица" введите "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="5637b-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="5637b-122">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="5637b-122">Click OK.</span></span>
16. <span data-ttu-id="5637b-123">В дереве выберите "Функции\Сведения о финансовых аналитиках".</span><span class="sxs-lookup"><span data-stu-id="5637b-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="5637b-124">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="5637b-124">Click Add root.</span></span>
    * <span data-ttu-id="5637b-125">Этот источник данных определяет, как область финансовых аналитик будет определена для любого отчета, который будет использовать эту модель в качестве источника данных.</span><span class="sxs-lookup"><span data-stu-id="5637b-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="5637b-126">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5637b-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="5637b-127">Выберите "Да" в поле "Запросить аналитики".</span><span class="sxs-lookup"><span data-stu-id="5637b-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="5637b-128">Выберите "Да", чтобы разрешить пользователю выбирать аналитики во время выполнении в форме диалогового окна пользователя.</span><span class="sxs-lookup"><span data-stu-id="5637b-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="5637b-129">Если задано значение "Нет", по умолчанию будут использоваться все финансовые аналитики текущего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="5637b-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="5637b-130">В поле "Выбор финансовых аналитик", выберите "Юридическое лицо".</span><span class="sxs-lookup"><span data-stu-id="5637b-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="5637b-131">Выберите "Все", чтобы разрешить пользователю выбирать требуемые аналитики для текущего экземпляра в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="5637b-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="5637b-132">Выберите "Юридическое лицо", чтобы разрешить пользователю выбирать требуемые аналитики для компании в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="5637b-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="5637b-133">Выберите "Аналитика", чтобы разрешить пользователю выбирать аналитики с использованием одного набора аналитик.</span><span class="sxs-lookup"><span data-stu-id="5637b-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="5637b-134">Выберите "Да" в поле "Запросить счет ГК".</span><span class="sxs-lookup"><span data-stu-id="5637b-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="5637b-135">Установите для параметра "Запросить счет ГК", чтобы разрешить пользователям выбирать счет ГК как часть списка аналитик.</span><span class="sxs-lookup"><span data-stu-id="5637b-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="5637b-136">Если задано значение "Нет", счет ГК не будет включен в список аналитик и будет включен параметр "Счет ГК является обязательным".</span><span class="sxs-lookup"><span data-stu-id="5637b-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="5637b-137">Если для параметра "Счет ГК является обязательным" задано значение "Да", включите счет ГК в список аналитик независимо от значения, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="5637b-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="5637b-138">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="5637b-138">Click OK.</span></span>
23. <span data-ttu-id="5637b-139">В дереве выберите "Dynamics 365 for Operations\Записи таблицы".</span><span class="sxs-lookup"><span data-stu-id="5637b-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="5637b-140">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="5637b-140">Click Add root.</span></span>
25. <span data-ttu-id="5637b-141">В поле "Имя" введите "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="5637b-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="5637b-142">Выберите "Да" в поле "Запросить запрос".</span><span class="sxs-lookup"><span data-stu-id="5637b-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="5637b-143">В поле "Таблица" введите "LedgerJournalTable".</span><span class="sxs-lookup"><span data-stu-id="5637b-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="5637b-144">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="5637b-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="5637b-145">Сопоставление элементов модели данных с добавленными источниками данных</span><span class="sxs-lookup"><span data-stu-id="5637b-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="5637b-146">В дереве разверните узел "Журнал".</span><span class="sxs-lookup"><span data-stu-id="5637b-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="5637b-147">В дереве разверните узел "Журнал\Проводки".</span><span class="sxs-lookup"><span data-stu-id="5637b-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="5637b-148">В дереве разверните узел "Журнал\Проводки\Данные аналитик".</span><span class="sxs-lookup"><span data-stu-id="5637b-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="5637b-149">В дереве разверните узел "Настройка аналитик".</span><span class="sxs-lookup"><span data-stu-id="5637b-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="5637b-150">В дереве разверните узел "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="5637b-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="5637b-151">В дереве разверните узел "LedgerJournal\<Связи".</span><span class="sxs-lookup"><span data-stu-id="5637b-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="5637b-152">В дереве разверните узел "LedgerJournal\<Связи\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="5637b-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="5637b-153">В дереве выберите узел "LedgerJournal\<Связи\LedgerJournalTrans\Ваучер".</span><span class="sxs-lookup"><span data-stu-id="5637b-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="5637b-154">В дереве выберите "Журнал\Проводка\Ваучер".</span><span class="sxs-lookup"><span data-stu-id="5637b-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="5637b-155">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-155">Click Bind.</span></span>
11. <span data-ttu-id="5637b-156">В дереве выберите "LedgerJournal\<Связи\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)".</span><span class="sxs-lookup"><span data-stu-id="5637b-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="5637b-157">Обратите внимание, что для любой ссылки на финансовые аналитиками, которая установлена, например, на LedgerDimension, соответствующий элемент источника данных доступен (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="5637b-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="5637b-158">Этот элемент источника данных предлагает финансовые аналитики набора аналитик в виде списка записей.</span><span class="sxs-lookup"><span data-stu-id="5637b-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="5637b-159">В дереве разверните узел "LedgerJournal\<Связи\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)".</span><span class="sxs-lookup"><span data-stu-id="5637b-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="5637b-160">В дереве разверните узел "LedgerJournal\<Связи\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Счет ГК и аналитики".</span><span class="sxs-lookup"><span data-stu-id="5637b-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="5637b-161">В дереве разверните узел "LedgerJournal\<Связи\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Счет ГК и аналитики\Значение".</span><span class="sxs-lookup"><span data-stu-id="5637b-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="5637b-162">В дереве разверните узел "LedgerJournal\<Связи\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Счет ГК и аналитики\Определение".</span><span class="sxs-lookup"><span data-stu-id="5637b-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="5637b-163">В дереве выберите узел "LedgerJournal\<Связи\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Счет ГК и аналитики\Определение\Имя".</span><span class="sxs-lookup"><span data-stu-id="5637b-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="5637b-164">В дереве выберите узел "Журнал\Проводки\Данные аналитик\Имя".</span><span class="sxs-lookup"><span data-stu-id="5637b-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="5637b-165">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-165">Click Bind.</span></span>
19. <span data-ttu-id="5637b-166">В дереве выберите узел "LedgerJournal\<Связи\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Счет ГК и аналитики\Значение\Описание".</span><span class="sxs-lookup"><span data-stu-id="5637b-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="5637b-167">В дереве выберите узел "Журнал\Проводки\Данные аналитик\Описание".</span><span class="sxs-lookup"><span data-stu-id="5637b-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="5637b-168">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-168">Click Bind.</span></span>
22. <span data-ttu-id="5637b-169">В дереве выберите узел "LedgerJournal\<Связи\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Счет ГК и аналитики\Значение\Код".</span><span class="sxs-lookup"><span data-stu-id="5637b-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="5637b-170">В дереве выберите узел "Журнал\Проводки\Данные аналитик\Код".</span><span class="sxs-lookup"><span data-stu-id="5637b-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="5637b-171">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-171">Click Bind.</span></span>
25. <span data-ttu-id="5637b-172">В дереве выберите узел "LedgerJournal\<Связи\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Счет ГК и аналитики".</span><span class="sxs-lookup"><span data-stu-id="5637b-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="5637b-173">В дереве выберите узел "Журнал\Проводки\Данные аналитик".</span><span class="sxs-lookup"><span data-stu-id="5637b-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="5637b-174">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-174">Click Bind.</span></span>
28. <span data-ttu-id="5637b-175">В дереве выберите узел "LedgerJournal\<Связи\LedgerJournalTrans\Debit(AmountCurDebit)".</span><span class="sxs-lookup"><span data-stu-id="5637b-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="5637b-176">В дереве выберите "Журнал\Проводка\Дебет".</span><span class="sxs-lookup"><span data-stu-id="5637b-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="5637b-177">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-177">Click Bind.</span></span>
31. <span data-ttu-id="5637b-178">В дереве выберите узел "LedgerJournal\<Связи\LedgerJournalTrans\Date(TransDate)".</span><span class="sxs-lookup"><span data-stu-id="5637b-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="5637b-179">В дереве выберите "Журнал\Проводка\Дата".</span><span class="sxs-lookup"><span data-stu-id="5637b-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="5637b-180">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-180">Click Bind.</span></span>
34. <span data-ttu-id="5637b-181">В дереве выберите узел "LedgerJournal\<Связи\LedgerJournalTrans\Currency(CurrencyCode)".</span><span class="sxs-lookup"><span data-stu-id="5637b-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="5637b-182">В дереве выберите "Журнал\Проводка\Валюта".</span><span class="sxs-lookup"><span data-stu-id="5637b-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="5637b-183">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-183">Click Bind.</span></span>
37. <span data-ttu-id="5637b-184">В дереве выберите узел "LedgerJournal\<Связи\LedgerJournalTrans\Credit(AmountCurCredit)".</span><span class="sxs-lookup"><span data-stu-id="5637b-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="5637b-185">В дереве выберите "Журнал\Проводка\Кредит".</span><span class="sxs-lookup"><span data-stu-id="5637b-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="5637b-186">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-186">Click Bind.</span></span>
40. <span data-ttu-id="5637b-187">В дереве выберите узел "LedgerJournal\<Связи\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="5637b-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="5637b-188">В дереве выберите "Журнал\Проводка".</span><span class="sxs-lookup"><span data-stu-id="5637b-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="5637b-189">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-189">Click Bind.</span></span>
43. <span data-ttu-id="5637b-190">В дереве выберите «LedgerJournal\Номер партии журнала(JournalNum)".</span><span class="sxs-lookup"><span data-stu-id="5637b-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="5637b-191">В дереве выберите "Журнал\Партия".</span><span class="sxs-lookup"><span data-stu-id="5637b-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="5637b-192">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-192">Click Bind.</span></span>
46. <span data-ttu-id="5637b-193">В дереве выберите "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="5637b-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="5637b-194">В дереве выберите "Журнал".</span><span class="sxs-lookup"><span data-stu-id="5637b-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="5637b-195">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-195">Click Bind.</span></span>
49. <span data-ttu-id="5637b-196">В дереве разверните узел "Аналитики".</span><span class="sxs-lookup"><span data-stu-id="5637b-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="5637b-197">В дереве разверните узел "Аналитики\Счет ГК и аналитики".</span><span class="sxs-lookup"><span data-stu-id="5637b-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="5637b-198">В дереве разверните узел "Аналитики\Счет ГК и аналитики\Определение".</span><span class="sxs-lookup"><span data-stu-id="5637b-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="5637b-199">В дереве выберите узел "Аналитики\Счет ГК и аналитики\Определение\Имя".</span><span class="sxs-lookup"><span data-stu-id="5637b-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="5637b-200">В дереве выберите узел "Настройка аналитик\Код".</span><span class="sxs-lookup"><span data-stu-id="5637b-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="5637b-201">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-201">Click Bind.</span></span>
55. <span data-ttu-id="5637b-202">В дереве выберите узел "Аналитики\Счет ГК и аналитики\Определение\Имя столбца отчета".</span><span class="sxs-lookup"><span data-stu-id="5637b-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="5637b-203">В дереве выберите узел "Настройка аналитик\Имя".</span><span class="sxs-lookup"><span data-stu-id="5637b-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="5637b-204">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-204">Click Bind.</span></span>
58. <span data-ttu-id="5637b-205">В дереве выберите узел "Аналитики\Счет ГК и аналитики".</span><span class="sxs-lookup"><span data-stu-id="5637b-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="5637b-206">В дереве выберите узел "Настройка аналитик".</span><span class="sxs-lookup"><span data-stu-id="5637b-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="5637b-207">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="5637b-207">Click Bind.</span></span>
61. <span data-ttu-id="5637b-208">В дереве выберите "Компания".</span><span class="sxs-lookup"><span data-stu-id="5637b-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="5637b-209">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="5637b-209">Click Edit.</span></span>
63. <span data-ttu-id="5637b-210">В поле expressionAsStringText введите "Company.'find()'.'name()'".</span><span class="sxs-lookup"><span data-stu-id="5637b-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="5637b-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="5637b-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="5637b-212">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="5637b-212">Click Save.</span></span>
65. <span data-ttu-id="5637b-213">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5637b-213">Close the page.</span></span>
66. <span data-ttu-id="5637b-214">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="5637b-214">Click Save.</span></span>
67. <span data-ttu-id="5637b-215">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5637b-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="5637b-216">Завершение этой черновой версии модели</span><span class="sxs-lookup"><span data-stu-id="5637b-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="5637b-217">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5637b-217">Close the page.</span></span>
2. <span data-ttu-id="5637b-218">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5637b-218">Close the page.</span></span>
3. <span data-ttu-id="5637b-219">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="5637b-219">Click Change status.</span></span>
4. <span data-ttu-id="5637b-220">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="5637b-220">Click Complete.</span></span>
5. <span data-ttu-id="5637b-221">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="5637b-221">Click OK.</span></span>


