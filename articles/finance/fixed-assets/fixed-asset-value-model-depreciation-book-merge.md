---
title: Объединение модели стоимости основных средств и журнала амортизации
description: В предыдущих выпусках имелось две концепции оценки для основных средств — модели стоимости и журналы амортизации. В Microsoft Dynamics 365 for Operations (1611) функция модели стоимости и функция журнала амортизации были объединены в одно понятие книги.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3225b214e729ff13d4ffe8ad1d8cf0f2d6baae49
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187207"
---
# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a><span data-ttu-id="b78fc-104">Объединение модели стоимости основных средств и журнала амортизации</span><span class="sxs-lookup"><span data-stu-id="b78fc-104">Fixed asset value model and depreciation book merge</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b78fc-105">В предыдущих выпусках имелось две концепции оценки для основных средств — модели стоимости и журналы амортизации.</span><span class="sxs-lookup"><span data-stu-id="b78fc-105">In previous releases, there were two valuation concepts for fixed assets -  value models and depreciation books.</span></span> <span data-ttu-id="b78fc-106">В Microsoft Dynamics 365 for Operations (1611) функция модели стоимости и функция журнала амортизации были объединены в одно понятие книги.</span><span class="sxs-lookup"><span data-stu-id="b78fc-106">In the Microsoft Dynamics 365 for Operations (1611) release, the value model functionality and depreciation book functionality have been merged into a single concept that is known as a book.</span></span>

<span data-ttu-id="b78fc-107">Новая функциональность книги основана на более ранней функции модели стоимости, но также включает все функции, которые ранее были представлены только в журналах амортизации.</span><span class="sxs-lookup"><span data-stu-id="b78fc-107">The new book functionality is based on earlier value model functionality but also includes all functionality that was previously provided only in depreciation books.</span></span> <span data-ttu-id="b78fc-108">[![Книга как объединение функциональностей модели стоимости и журнала амортизации](./media/fixed-assets.png)](./media/fixed-assets.png) Вследствие этого слияния теперь можно использовать один набор страниц, запросов и отчетов для всех ваших процессов основных средств.</span><span class="sxs-lookup"><span data-stu-id="b78fc-108">[![Book as a merging of value model and depreciation book functionality](./media/fixed-assets.png)](./media/fixed-assets.png) Because of this merge, you can now use a single set of pages, inquiries, and reports for all your fixed asset processes.</span></span> <span data-ttu-id="b78fc-109">Таблицы в этом разделе описывают более раннюю функциональность для журналов амортизации и моделей стоимости вместе с новой функциональностью для книг.</span><span class="sxs-lookup"><span data-stu-id="b78fc-109">The tables in this topic describe the earlier functionality for depreciation books and value models, together with the new functionality for books.</span></span>

## <a name="setup"></a><span data-ttu-id="b78fc-110">Настройка</span><span class="sxs-lookup"><span data-stu-id="b78fc-110">Setup</span></span>
<span data-ttu-id="b78fc-111">По умолчанию книги разносятся как в главную книгу (GL), так и в субкнигу основных средств.</span><span class="sxs-lookup"><span data-stu-id="b78fc-111">By default, books post to both the general ledger (GL) and the fixed asset subledger.</span></span> <span data-ttu-id="b78fc-112">Книги имеют новый параметр **Разноска в главную книгу**, который позволяет отключить разноску отключен в ГК и выполнять разноску только в субкнигу основных средств.</span><span class="sxs-lookup"><span data-stu-id="b78fc-112">Books have a new **Post to general ledger** option that lets you disable posting to the GL and post only to the fixed asset subledger.</span></span> <span data-ttu-id="b78fc-113">Эта функция похожа на более раннее поведение разноски для журналов амортизации.</span><span class="sxs-lookup"><span data-stu-id="b78fc-113">This functionality resembles the earlier posting behavior for depreciation books.</span></span> <span data-ttu-id="b78fc-114">Настройка имен журналов имеет новый слой разноски, который называется "Нет".</span><span class="sxs-lookup"><span data-stu-id="b78fc-114">The journal names setup has a new posting layer that is named None.</span></span> <span data-ttu-id="b78fc-115">Этот слой разноски был добавлен специально для проводок с основными средствами.</span><span class="sxs-lookup"><span data-stu-id="b78fc-115">This posting layer was added specifically for fixed asset transactions.</span></span> <span data-ttu-id="b78fc-116">Для разноски проводок для книг, которые не будет разноситься в ГК, необходимо использовать имя журнала, у которого для слоя разноски задано значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="b78fc-116">To post transactions for books that don't post to the GL, you must use a journal name that has the posting layer set to **None**.</span></span>

|                                                  |                                 |                                 |                                                         |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
|                                                  | <span data-ttu-id="b78fc-117">Журнал амортизации</span><span class="sxs-lookup"><span data-stu-id="b78fc-117">Depreciation book</span></span>               | <span data-ttu-id="b78fc-118">Модель учета</span><span class="sxs-lookup"><span data-stu-id="b78fc-118">Value model</span></span>                     | <span data-ttu-id="b78fc-119">Книга (новая)</span><span class="sxs-lookup"><span data-stu-id="b78fc-119">Book (New)</span></span>                                              |
| <span data-ttu-id="b78fc-120">Разноска в ГК</span><span class="sxs-lookup"><span data-stu-id="b78fc-120">Post to the GL</span></span>                                   | <span data-ttu-id="b78fc-121">Никогда</span><span class="sxs-lookup"><span data-stu-id="b78fc-121">Never</span></span>                           | <span data-ttu-id="b78fc-122">Всегда</span><span class="sxs-lookup"><span data-stu-id="b78fc-122">Always</span></span>                          | <span data-ttu-id="b78fc-123">Параметр для разноски в ГК</span><span class="sxs-lookup"><span data-stu-id="b78fc-123">Option to post to the GL</span></span>                                |
| <span data-ttu-id="b78fc-124">Слои разноски</span><span class="sxs-lookup"><span data-stu-id="b78fc-124">Posting layers</span></span>                                   | <span data-ttu-id="b78fc-125">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="b78fc-125">Not applicable</span></span>                  | <span data-ttu-id="b78fc-126">3: Текущий, Операции и Налог</span><span class="sxs-lookup"><span data-stu-id="b78fc-126">3: Current, Operations, and Tax</span></span> | <span data-ttu-id="b78fc-127">11: Текущий, Операции, Налог, 7 настраиваемых слоев и Нет</span><span class="sxs-lookup"><span data-stu-id="b78fc-127">11: Current, Operations, Tax, 7 custom layers, and None</span></span> |
| <span data-ttu-id="b78fc-128">Наименования журналов</span><span class="sxs-lookup"><span data-stu-id="b78fc-128">Journal names</span></span>                                    | <span data-ttu-id="b78fc-129">Имена книг журналов амортизации</span><span class="sxs-lookup"><span data-stu-id="b78fc-129">Depreciation book journal names</span></span> | <span data-ttu-id="b78fc-130">ГК - Наименования журналов</span><span class="sxs-lookup"><span data-stu-id="b78fc-130">GL - Journal names</span></span>              | <span data-ttu-id="b78fc-131">ГК - Наименования журналов</span><span class="sxs-lookup"><span data-stu-id="b78fc-131">GL - Journal names</span></span>                                      |
| <span data-ttu-id="b78fc-132">Производные книги</span><span class="sxs-lookup"><span data-stu-id="b78fc-132">Derived books</span></span>                                    | <span data-ttu-id="b78fc-133">Не разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-133">Not allowed</span></span>                     | <span data-ttu-id="b78fc-134">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-134">Allowed</span></span>                         | <span data-ttu-id="b78fc-135">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-135">Allowed</span></span>                                                 |
| <span data-ttu-id="b78fc-136">Переопределение профиля амортизации на уровне средства</span><span class="sxs-lookup"><span data-stu-id="b78fc-136">Depreciation profile override at the asset level</span></span> | <span data-ttu-id="b78fc-137">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-137">Allowed</span></span>                         | <span data-ttu-id="b78fc-138">Не разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-138">Not allowed</span></span>                     | <span data-ttu-id="b78fc-139">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-139">Allowed</span></span>                                                 |

## <a name="processes"></a><span data-ttu-id="b78fc-140">Процессы</span><span class="sxs-lookup"><span data-stu-id="b78fc-140">Processes</span></span>
<span data-ttu-id="b78fc-141">Процессы теперь используют общую страницу.</span><span class="sxs-lookup"><span data-stu-id="b78fc-141">Processes now use a common page.</span></span> <span data-ttu-id="b78fc-142">Некоторые процессы допускаются только в том случае, если в настройках книги для параметра **Разноска в главную книгу** задано значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="b78fc-142">Some processes are allowed only if the **Post to general ledger** option is set to **No** in the book setup.</span></span>

|                                |                           |                     |                                          |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
|                                | <span data-ttu-id="b78fc-143">Журнал амортизации</span><span class="sxs-lookup"><span data-stu-id="b78fc-143">Depreciation book</span></span>         | <span data-ttu-id="b78fc-144">Модель учета</span><span class="sxs-lookup"><span data-stu-id="b78fc-144">Value model</span></span>         | <span data-ttu-id="b78fc-145">Книга (новая)</span><span class="sxs-lookup"><span data-stu-id="b78fc-145">Book (New)</span></span>                               |
| <span data-ttu-id="b78fc-146">Запись проводки</span><span class="sxs-lookup"><span data-stu-id="b78fc-146">Transaction entry</span></span>              | <span data-ttu-id="b78fc-147">Книга журналов амортизации</span><span class="sxs-lookup"><span data-stu-id="b78fc-147">Depreciation book journal</span></span> | <span data-ttu-id="b78fc-148">Журнал основных средств</span><span class="sxs-lookup"><span data-stu-id="b78fc-148">Fixed asset journal</span></span> | <span data-ttu-id="b78fc-149">Журнал основных средств</span><span class="sxs-lookup"><span data-stu-id="b78fc-149">Fixed asset journal</span></span>                      |
| <span data-ttu-id="b78fc-150">Амортизационная премия</span><span class="sxs-lookup"><span data-stu-id="b78fc-150">Bonus depreciation</span></span>             | <span data-ttu-id="b78fc-151">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-151">Allowed</span></span>                   | <span data-ttu-id="b78fc-152">Не разрешено</span><span class="sxs-lookup"><span data-stu-id="b78fc-152">Not Allowed</span></span>         | <span data-ttu-id="b78fc-153">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-153">Allowed</span></span>                                  |
| <span data-ttu-id="b78fc-154">Удаление исторических проводок</span><span class="sxs-lookup"><span data-stu-id="b78fc-154">Delete historical transactions</span></span> | <span data-ttu-id="b78fc-155">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-155">Allowed</span></span>                   | <span data-ttu-id="b78fc-156">Не разрешено</span><span class="sxs-lookup"><span data-stu-id="b78fc-156">Not Allowed</span></span>         | <span data-ttu-id="b78fc-157">Разрешено, кроме случаев разноски в ГК</span><span class="sxs-lookup"><span data-stu-id="b78fc-157">Allowed, unless you're posting to the GL</span></span> |
| <span data-ttu-id="b78fc-158">Массовое обновление</span><span class="sxs-lookup"><span data-stu-id="b78fc-158">Mass update</span></span>                    | <span data-ttu-id="b78fc-159">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-159">Allowed</span></span>                   | <span data-ttu-id="b78fc-160">Не разрешено</span><span class="sxs-lookup"><span data-stu-id="b78fc-160">Not Allowed</span></span>         | <span data-ttu-id="b78fc-161">Разрешено, кроме случаев разноски в ГК</span><span class="sxs-lookup"><span data-stu-id="b78fc-161">Allowed, unless you're posting to the GL</span></span> |

## <a name="inquiries-and-reports"></a><span data-ttu-id="b78fc-162">Запросы и отчеты</span><span class="sxs-lookup"><span data-stu-id="b78fc-162">Inquiries and reports</span></span>
<span data-ttu-id="b78fc-163">Запросы и отчеты поддерживают все книги.</span><span class="sxs-lookup"><span data-stu-id="b78fc-163">Inquiries and reports support all books.</span></span> <span data-ttu-id="b78fc-164">Отчеты, которые не включены в следующую таблицу, ранее поддерживали как журналы амортизации, так и модели стоимости, и будут теперь продолжать поддерживать все типы книг.</span><span class="sxs-lookup"><span data-stu-id="b78fc-164">Reports that aren't included in the following table previously supported both depreciation books and value models, and will now continue to support all book types.</span></span> <span data-ttu-id="b78fc-165">Поле **Слой разноски** также добавлено к отчетам, чтобы можно было легче идентифицировать разноски проводок.</span><span class="sxs-lookup"><span data-stu-id="b78fc-165">The **Posting layer** field has also been added to reports, so that you can more easily identify the transaction postings.</span></span>

|                                       |                                |                          |                          |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
|                                       | <span data-ttu-id="b78fc-166">Журнал амортизации</span><span class="sxs-lookup"><span data-stu-id="b78fc-166">Depreciation book</span></span>              | <span data-ttu-id="b78fc-167">Модель учета</span><span class="sxs-lookup"><span data-stu-id="b78fc-167">Value model</span></span>              | <span data-ttu-id="b78fc-168">Книга (новая)</span><span class="sxs-lookup"><span data-stu-id="b78fc-168">Book (New)</span></span>               |
| <span data-ttu-id="b78fc-169">Запросы</span><span class="sxs-lookup"><span data-stu-id="b78fc-169">Inquiries</span></span>                             | <span data-ttu-id="b78fc-170">Проводки журнала амортизации</span><span class="sxs-lookup"><span data-stu-id="b78fc-170">Depreciation book transactions</span></span> | <span data-ttu-id="b78fc-171">Проводки по ОС</span><span class="sxs-lookup"><span data-stu-id="b78fc-171">Fixed asset transactions</span></span> | <span data-ttu-id="b78fc-172">Проводки по ОС</span><span class="sxs-lookup"><span data-stu-id="b78fc-172">Fixed asset transactions</span></span> |
| <span data-ttu-id="b78fc-173">Выписка по основным средствам</span><span class="sxs-lookup"><span data-stu-id="b78fc-173">Fixed asset statement</span></span>                 | <span data-ttu-id="b78fc-174">Не разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-174">Not allowed</span></span>                    | <span data-ttu-id="b78fc-175">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-175">Allowed</span></span>                  | <span data-ttu-id="b78fc-176">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-176">Allowed</span></span>                  |
| <span data-ttu-id="b78fc-177">Базовые ОС</span><span class="sxs-lookup"><span data-stu-id="b78fc-177">Fixed asset basis</span></span>                     | <span data-ttu-id="b78fc-178">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-178">Allowed</span></span>                        | <span data-ttu-id="b78fc-179">Не разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-179">Not allowed</span></span>              | <span data-ttu-id="b78fc-180">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-180">Allowed</span></span>                  |
| <span data-ttu-id="b78fc-181">Возможность применения ОС в середине квартала</span><span class="sxs-lookup"><span data-stu-id="b78fc-181">Fixed asset mid-quarter applicability</span></span> | <span data-ttu-id="b78fc-182">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-182">Allowed</span></span>                        | <span data-ttu-id="b78fc-183">Не разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-183">Not allowed</span></span>              | <span data-ttu-id="b78fc-184">Разрешенный</span><span class="sxs-lookup"><span data-stu-id="b78fc-184">Allowed</span></span>                  |

## <a name="upgrade"></a><span data-ttu-id="b78fc-185">Обновить</span><span class="sxs-lookup"><span data-stu-id="b78fc-185">Upgrade</span></span>
<span data-ttu-id="b78fc-186">В процессе обновления ваша существующая настройка и все ваши существующие проводки будут перемещены в структуру новой книги.</span><span class="sxs-lookup"><span data-stu-id="b78fc-186">The upgrade process will move your existing setup and all your existing transactions to the new book structure.</span></span> <span data-ttu-id="b78fc-187">Модели стоимости будут оставаться как есть на данный момент в качестве книги, которая выполняет разноску в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="b78fc-187">Value models will remain as they currently are, as a book that posts to the general ledger.</span></span> <span data-ttu-id="b78fc-188">Однако журналы амортизации будет перемещены в книгу, в которой для параметра **Разноска в главную книгу** задано значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="b78fc-188">However, depreciation books will be moved to a book that has the **Post to general ledger** option set to **No**.</span></span> <span data-ttu-id="b78fc-189">Имена журналов амортизации будут перемещены в имя журнала ГК, в котором для слоя разноски установлено значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="b78fc-189">Depreciation book journal names will be moved to a general ledger journal name that has the posting layer set to **None**.</span></span>


