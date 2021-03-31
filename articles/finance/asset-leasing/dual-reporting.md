---
title: Двойная отчетность
description: В этой теме рассматривается пример, показывающий, как можно выполнить требования как для международной финансовой отчетности по стандарту МСФО, так и для регламентной отчетности в аренде активов.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6daa43178625316a40427728e7e4186691cc13c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229558"
---
# <a name="dual-reporting"></a><span data-ttu-id="a8042-103">Двойная отчетность</span><span class="sxs-lookup"><span data-stu-id="a8042-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8042-104">В этой теме рассматривается пример, показывающий, как можно выполнить требования как для международной финансовой отчетности по стандарту МСФО, так и для регламентной отчетности в аренде активов.</span><span class="sxs-lookup"><span data-stu-id="a8042-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="a8042-105">Знакомство с уровнями разноски в Microsoft Dynamics 365 Finance является обязательным и облегчит понимание этого примера.</span><span class="sxs-lookup"><span data-stu-id="a8042-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="a8042-106">Пример</span><span class="sxs-lookup"><span data-stu-id="a8042-106">Example</span></span>

<span data-ttu-id="a8042-107">Следующий пример счетов для аренды в соответствии с итальянскими нормативными отчетами с использованием обоих методов расчета наличных денег и способов отчетности МСФО.</span><span class="sxs-lookup"><span data-stu-id="a8042-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="a8042-108">Компания должна создать три книги для учета как для итальянских регламентных требований, так и требований МСФО 16.</span><span class="sxs-lookup"><span data-stu-id="a8042-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="a8042-109">Для МСФО 16 требуется одна книга, одна книга требуется которой для регламентных требований, и одна книга требуется для автоматической реверсирования регламентных разносок.</span><span class="sxs-lookup"><span data-stu-id="a8042-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="a8042-110">Книги настраиваются так, как показано в следующих таблицах.</span><span class="sxs-lookup"><span data-stu-id="a8042-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="a8042-111">**Книга МСФО 16**</span><span class="sxs-lookup"><span data-stu-id="a8042-111">**IFRS 16 book**</span></span>

<span data-ttu-id="a8042-112">Книга МСФО 16 настроена таким образом, что она соответствует стандарту отчетности МСФО 16.</span><span class="sxs-lookup"><span data-stu-id="a8042-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="a8042-113">Все записи, учитываемые в этой книге, будут разнесены в пользовательский слой.</span><span class="sxs-lookup"><span data-stu-id="a8042-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="a8042-114">Наименование</span><span class="sxs-lookup"><span data-stu-id="a8042-114">Name</span></span>                                    | <span data-ttu-id="a8042-115">описание</span><span class="sxs-lookup"><span data-stu-id="a8042-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="a8042-116">Тип книги</span><span class="sxs-lookup"><span data-stu-id="a8042-116">Book type</span></span>                               | <span data-ttu-id="a8042-117">МСФО 16</span><span class="sxs-lookup"><span data-stu-id="a8042-117">IFRS 16</span></span>        |
| <span data-ttu-id="a8042-118">Бухгалтерская запись</span><span class="sxs-lookup"><span data-stu-id="a8042-118">Book description</span></span>                        | <span data-ttu-id="a8042-119">МСФО 16</span><span class="sxs-lookup"><span data-stu-id="a8042-119">IFRS 16</span></span>        |
| <span data-ttu-id="a8042-120">Слой разноски</span><span class="sxs-lookup"><span data-stu-id="a8042-120">Posting Layer</span></span>                           | <span data-ttu-id="a8042-121">Пользовательский слой 1</span><span class="sxs-lookup"><span data-stu-id="a8042-121">Custom layer 1</span></span> |
| <span data-ttu-id="a8042-122">Тип аренды</span><span class="sxs-lookup"><span data-stu-id="a8042-122">Lease Type</span></span>                              | <span data-ttu-id="a8042-123">Finance</span><span class="sxs-lookup"><span data-stu-id="a8042-123">Finance</span></span>        |
| <span data-ttu-id="a8042-124">Платформа учета</span><span class="sxs-lookup"><span data-stu-id="a8042-124">Accounting Framework</span></span>                    | <span data-ttu-id="a8042-125">МСФО 16</span><span class="sxs-lookup"><span data-stu-id="a8042-125">IFRS 16</span></span>        |
| <span data-ttu-id="a8042-126">Настройка отношения срока аренды к сроку службы</span><span class="sxs-lookup"><span data-stu-id="a8042-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="a8042-127">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-127">0.00</span></span>           |
| <span data-ttu-id="a8042-128">Настройка отношения "Текущая стоимость / Реальная стоимость актива"</span><span class="sxs-lookup"><span data-stu-id="a8042-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="a8042-129">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-129">0.00</span></span>           |
| <span data-ttu-id="a8042-130">Порог краткосрочной аренды</span><span class="sxs-lookup"><span data-stu-id="a8042-130">Short-term threshold</span></span>                    | <span data-ttu-id="a8042-131">12</span><span class="sxs-lookup"><span data-stu-id="a8042-131">12</span></span>             |
| <span data-ttu-id="a8042-132">Порог аренды малоценного актива</span><span class="sxs-lookup"><span data-stu-id="a8042-132">Low Value Threshold</span></span>                     | <span data-ttu-id="a8042-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-133">5,000.00</span></span>       |
| <span data-ttu-id="a8042-134">Оплата поставщику</span><span class="sxs-lookup"><span data-stu-id="a8042-134">Pay to Vendor</span></span>                           | <span data-ttu-id="a8042-135">Нет</span><span class="sxs-lookup"><span data-stu-id="a8042-135">No</span></span>             |

<span data-ttu-id="a8042-136">**Регламентная книга**</span><span class="sxs-lookup"><span data-stu-id="a8042-136">**Statutory book**</span></span>

<span data-ttu-id="a8042-137">Регламентная книга — это книга на основе наличных, в которой компания будет учитывать расходы на аренду в качестве суммы денежных средств, выплачиваемых ежемесячно за аренду.</span><span class="sxs-lookup"><span data-stu-id="a8042-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="a8042-138">Эта книга не будет создавать актив в форме права пользования или арендного обязательства.</span><span class="sxs-lookup"><span data-stu-id="a8042-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="a8042-139">Наименование</span><span class="sxs-lookup"><span data-stu-id="a8042-139">Name</span></span>                                    | <span data-ttu-id="a8042-140">описание</span><span class="sxs-lookup"><span data-stu-id="a8042-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="a8042-141">Тип книги</span><span class="sxs-lookup"><span data-stu-id="a8042-141">Book type</span></span>                               | <span data-ttu-id="a8042-142">Регламентная</span><span class="sxs-lookup"><span data-stu-id="a8042-142">Statutory</span></span>   |
| <span data-ttu-id="a8042-143">Бухгалтерская запись</span><span class="sxs-lookup"><span data-stu-id="a8042-143">Book description</span></span>                        | <span data-ttu-id="a8042-144">Локальная GAAP</span><span class="sxs-lookup"><span data-stu-id="a8042-144">Local GAAP</span></span>  |
| <span data-ttu-id="a8042-145">Слой разноски</span><span class="sxs-lookup"><span data-stu-id="a8042-145">Posting Layer</span></span>                           | <span data-ttu-id="a8042-146">Текущие</span><span class="sxs-lookup"><span data-stu-id="a8042-146">Current</span></span>     |
| <span data-ttu-id="a8042-147">Тип аренды</span><span class="sxs-lookup"><span data-stu-id="a8042-147">Lease Type</span></span>                              | <span data-ttu-id="a8042-148">Автоматически</span><span class="sxs-lookup"><span data-stu-id="a8042-148">Automatic</span></span>   |
| <span data-ttu-id="a8042-149">Платформа учета</span><span class="sxs-lookup"><span data-stu-id="a8042-149">Accounting Framework</span></span>                    | <span data-ttu-id="a8042-150">Кассовый метод</span><span class="sxs-lookup"><span data-stu-id="a8042-150">Cash basis</span></span>  |
| <span data-ttu-id="a8042-151">Настройка отношения срока аренды к сроку службы</span><span class="sxs-lookup"><span data-stu-id="a8042-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="a8042-152">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-152">0.00</span></span>        |
| <span data-ttu-id="a8042-153">Настройка отношения "Текущая стоимость / Реальная стоимость актива"</span><span class="sxs-lookup"><span data-stu-id="a8042-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="a8042-154">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-154">0.00</span></span>        |
| <span data-ttu-id="a8042-155">Порог краткосрочной аренды</span><span class="sxs-lookup"><span data-stu-id="a8042-155">Short-term threshold</span></span>                    | <span data-ttu-id="a8042-156">0</span><span class="sxs-lookup"><span data-stu-id="a8042-156">0</span></span>           |
| <span data-ttu-id="a8042-157">Порог аренды малоценного актива</span><span class="sxs-lookup"><span data-stu-id="a8042-157">Low Value Threshold</span></span>                     | <span data-ttu-id="a8042-158">0</span><span class="sxs-lookup"><span data-stu-id="a8042-158">0</span></span>           |
| <span data-ttu-id="a8042-159">Оплата поставщику</span><span class="sxs-lookup"><span data-stu-id="a8042-159">Pay to Vendor</span></span>                           | <span data-ttu-id="a8042-160">Нет</span><span class="sxs-lookup"><span data-stu-id="a8042-160">No</span></span>          |

<span data-ttu-id="a8042-161">**Книга регламентного сторнирования**</span><span class="sxs-lookup"><span data-stu-id="a8042-161">**Statutory reversal book**</span></span>

<span data-ttu-id="a8042-162">Книга регламентного сторнирования настраивается так же, как и регламентная книга.</span><span class="sxs-lookup"><span data-stu-id="a8042-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="a8042-163">Наименование</span><span class="sxs-lookup"><span data-stu-id="a8042-163">Name</span></span>                                    | <span data-ttu-id="a8042-164">описание</span><span class="sxs-lookup"><span data-stu-id="a8042-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="a8042-165">Тип книги</span><span class="sxs-lookup"><span data-stu-id="a8042-165">Book type</span></span>                               | <span data-ttu-id="a8042-166">Регламентная — сторнирование</span><span class="sxs-lookup"><span data-stu-id="a8042-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="a8042-167">Бухгалтерская запись</span><span class="sxs-lookup"><span data-stu-id="a8042-167">Book description</span></span>                        | <span data-ttu-id="a8042-168">Книга для сторнирования регламентной книги</span><span class="sxs-lookup"><span data-stu-id="a8042-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="a8042-169">Слой разноски</span><span class="sxs-lookup"><span data-stu-id="a8042-169">Posting Layer</span></span>                           | <span data-ttu-id="a8042-170">Пользовательский слой 1</span><span class="sxs-lookup"><span data-stu-id="a8042-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="a8042-171">Тип аренды</span><span class="sxs-lookup"><span data-stu-id="a8042-171">Lease Type</span></span>                              | <span data-ttu-id="a8042-172">Автоматически</span><span class="sxs-lookup"><span data-stu-id="a8042-172">Automatic</span></span>                      |
| <span data-ttu-id="a8042-173">Платформа учета</span><span class="sxs-lookup"><span data-stu-id="a8042-173">Accounting Framework</span></span>                    | <span data-ttu-id="a8042-174">Кассовый метод</span><span class="sxs-lookup"><span data-stu-id="a8042-174">Cash basis</span></span>                     |
| <span data-ttu-id="a8042-175">Настройка отношения срока аренды к сроку службы</span><span class="sxs-lookup"><span data-stu-id="a8042-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="a8042-176">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-176">0.00</span></span>                           |
| <span data-ttu-id="a8042-177">Настройка отношения "Текущая стоимость / Реальная стоимость актива"</span><span class="sxs-lookup"><span data-stu-id="a8042-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="a8042-178">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-178">0.00</span></span>                           |
| <span data-ttu-id="a8042-179">Порог краткосрочной аренды</span><span class="sxs-lookup"><span data-stu-id="a8042-179">Short-term threshold</span></span>                    | <span data-ttu-id="a8042-180">0</span><span class="sxs-lookup"><span data-stu-id="a8042-180">0</span></span>                              |
| <span data-ttu-id="a8042-181">Порог аренды малоценного актива</span><span class="sxs-lookup"><span data-stu-id="a8042-181">Low Value Threshold</span></span>                     | <span data-ttu-id="a8042-182">0</span><span class="sxs-lookup"><span data-stu-id="a8042-182">0</span></span>                              |
| <span data-ttu-id="a8042-183">Оплата поставщику</span><span class="sxs-lookup"><span data-stu-id="a8042-183">Pay to Vendor</span></span>                           | <span data-ttu-id="a8042-184">Нет</span><span class="sxs-lookup"><span data-stu-id="a8042-184">No</span></span>                             |

<span data-ttu-id="a8042-185">В данном примере была создана аренда со следующими настройками на вкладках **Общие** и **Строки графика платежей**.</span><span class="sxs-lookup"><span data-stu-id="a8042-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="a8042-186">**Вкладка "Общие"**</span><span class="sxs-lookup"><span data-stu-id="a8042-186">**General tab**</span></span>

| <span data-ttu-id="a8042-187">Поле</span><span class="sxs-lookup"><span data-stu-id="a8042-187">Field</span></span>                      | <span data-ttu-id="a8042-188">значение</span><span class="sxs-lookup"><span data-stu-id="a8042-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="a8042-189">Приростная ставка процента на заемный капитал</span><span class="sxs-lookup"><span data-stu-id="a8042-189">Incremental borrowing rate</span></span> | <span data-ttu-id="a8042-190">5%</span><span class="sxs-lookup"><span data-stu-id="a8042-190">5%</span></span>               |
| <span data-ttu-id="a8042-191">Дата начала</span><span class="sxs-lookup"><span data-stu-id="a8042-191">Commencement date</span></span>          | <span data-ttu-id="a8042-192">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="a8042-192">1/1/2020</span></span>         |
| <span data-ttu-id="a8042-193">Группа аренды</span><span class="sxs-lookup"><span data-stu-id="a8042-193">Lease group</span></span>                | <span data-ttu-id="a8042-194">Постройки</span><span class="sxs-lookup"><span data-stu-id="a8042-194">Buildings</span></span>        |
| <span data-ttu-id="a8042-195">Поставщик</span><span class="sxs-lookup"><span data-stu-id="a8042-195">Vendor</span></span>                     | <span data-ttu-id="a8042-196">1001</span><span class="sxs-lookup"><span data-stu-id="a8042-196">1001</span></span>             |
| <span data-ttu-id="a8042-197">Реальная стоимость актива</span><span class="sxs-lookup"><span data-stu-id="a8042-197">Fair value of the asset</span></span>    | <span data-ttu-id="a8042-198">245,000</span><span class="sxs-lookup"><span data-stu-id="a8042-198">245,000</span></span>          |
| <span data-ttu-id="a8042-199">Срок службы актива</span><span class="sxs-lookup"><span data-stu-id="a8042-199">Asset useful life</span></span>          | <span data-ttu-id="a8042-200">120</span><span class="sxs-lookup"><span data-stu-id="a8042-200">120</span></span>              |
| <span data-ttu-id="a8042-201">Тип аннуитета</span><span class="sxs-lookup"><span data-stu-id="a8042-201">Annuity type</span></span>               | <span data-ttu-id="a8042-202">Аннуитет постнумерандо</span><span class="sxs-lookup"><span data-stu-id="a8042-202">Ordinary annuity</span></span> |
| <span data-ttu-id="a8042-203">Интервал объединения</span><span class="sxs-lookup"><span data-stu-id="a8042-203">Compounding interval</span></span>       | <span data-ttu-id="a8042-204">ежемесячно</span><span class="sxs-lookup"><span data-stu-id="a8042-204">Monthly</span></span>          |

<span data-ttu-id="a8042-205">**Вкладка "Строки графика платежей"**</span><span class="sxs-lookup"><span data-stu-id="a8042-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="a8042-206">Поле</span><span class="sxs-lookup"><span data-stu-id="a8042-206">Field</span></span>             | <span data-ttu-id="a8042-207">значение</span><span class="sxs-lookup"><span data-stu-id="a8042-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="a8042-208">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="a8042-208">Start date</span></span>        | <span data-ttu-id="a8042-209">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="a8042-209">1/1/2020</span></span>   |
| <span data-ttu-id="a8042-210">Интервал периода</span><span class="sxs-lookup"><span data-stu-id="a8042-210">Period interval</span></span>   | <span data-ttu-id="a8042-211">Месяцы</span><span class="sxs-lookup"><span data-stu-id="a8042-211">Months</span></span>     |
| <span data-ttu-id="a8042-212">Периоды</span><span class="sxs-lookup"><span data-stu-id="a8042-212">Periods</span></span>           | <span data-ttu-id="a8042-213">24</span><span class="sxs-lookup"><span data-stu-id="a8042-213">24</span></span>         |
| <span data-ttu-id="a8042-214">Конечная дата</span><span class="sxs-lookup"><span data-stu-id="a8042-214">End date</span></span>          | <span data-ttu-id="a8042-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="a8042-215">12/31/2020</span></span> |
| <span data-ttu-id="a8042-216">Частота платежей</span><span class="sxs-lookup"><span data-stu-id="a8042-216">Payment frequency</span></span> | <span data-ttu-id="a8042-217">ежемесячно</span><span class="sxs-lookup"><span data-stu-id="a8042-217">Monthly</span></span>    |
| <span data-ttu-id="a8042-218">Сумма оплаты</span><span class="sxs-lookup"><span data-stu-id="a8042-218">Payment amount</span></span>    | <span data-ttu-id="a8042-219">1000</span><span class="sxs-lookup"><span data-stu-id="a8042-219">1,000</span></span>      |

<span data-ttu-id="a8042-220">Для учета данной аренды с помощью двух платформ используется текущий слой разноски и пользовательский слой разноски.</span><span class="sxs-lookup"><span data-stu-id="a8042-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="a8042-221">В следующей таблице показан пример каждой записи в журнале, которая требуется для правильного представления финансовых данных в соответствии с каждым стандартом отчетности.</span><span class="sxs-lookup"><span data-stu-id="a8042-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="a8042-222">Подробное описание каждой записи в журнале для первого месяца аренды предоставляется впоследствии.</span><span class="sxs-lookup"><span data-stu-id="a8042-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="a8042-223">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="a8042-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="a8042-224">описание</span><span class="sxs-lookup"><span data-stu-id="a8042-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="a8042-225">Регламентная книга (текущий слой)</span><span class="sxs-lookup"><span data-stu-id="a8042-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="a8042-226">Текущий слой, итого</span><span class="sxs-lookup"><span data-stu-id="a8042-226">Current layer total</span></span></th>
<th><span data-ttu-id="a8042-227">Книга сторнирования (настраиваемый слой)</span><span class="sxs-lookup"><span data-stu-id="a8042-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="a8042-228">Книга МСФО 16 (настраиваемый слой)</span><span class="sxs-lookup"><span data-stu-id="a8042-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="a8042-229">Текущий слой + пользовательский слой, итого</span><span class="sxs-lookup"><span data-stu-id="a8042-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a8042-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="a8042-230">JE-100</span></span></th>
<th><span data-ttu-id="a8042-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="a8042-231">JE-110</span></span></th>
<th><span data-ttu-id="a8042-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="a8042-232">JE-120</span></span></th>
<th><span data-ttu-id="a8042-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="a8042-233">JE-130</span></span></th>
<th><span data-ttu-id="a8042-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="a8042-234">JE-140</span></span></th>
<th><span data-ttu-id="a8042-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="a8042-235">JE-150</span></span></th>
<th><span data-ttu-id="a8042-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="a8042-236">JE-160</span></span></th>
<th><span data-ttu-id="a8042-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="a8042-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a8042-238">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="a8042-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a8042-239">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="a8042-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a8042-240">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="a8042-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a8042-241">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="a8042-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a8042-242">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="a8042-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a8042-243">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="a8042-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a8042-244">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="a8042-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a8042-245">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="a8042-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8042-246">1</span><span class="sxs-lookup"><span data-stu-id="a8042-246">1</span></span></td>
<td><span data-ttu-id="a8042-247">Расходы по аренде</span><span class="sxs-lookup"><span data-stu-id="a8042-247">Lease expense</span></span></td>
<td><span data-ttu-id="a8042-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-249">1,000.00</span></span></td>
<td><span data-ttu-id="a8042-250">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="a8042-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-251">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-252">2</span><span class="sxs-lookup"><span data-stu-id="a8042-252">2</span></span></td>
<td><span data-ttu-id="a8042-253">Банковские сборы</span><span class="sxs-lookup"><span data-stu-id="a8042-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-254">3.00</span><span class="sxs-lookup"><span data-stu-id="a8042-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-255">3.00</span><span class="sxs-lookup"><span data-stu-id="a8042-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-256">3.00</span><span class="sxs-lookup"><span data-stu-id="a8042-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-257">3</span><span class="sxs-lookup"><span data-stu-id="a8042-257">3</span></span></td>
<td><span data-ttu-id="a8042-258">Расходы на НДС</span><span class="sxs-lookup"><span data-stu-id="a8042-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-259">5.00</span><span class="sxs-lookup"><span data-stu-id="a8042-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-260">5.00</span><span class="sxs-lookup"><span data-stu-id="a8042-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-261">5.00</span><span class="sxs-lookup"><span data-stu-id="a8042-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-262">4</span><span class="sxs-lookup"><span data-stu-id="a8042-262">4</span></span></td>
<td><span data-ttu-id="a8042-263">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="a8042-263">Clearing account</span></span></td>
<td><span data-ttu-id="a8042-264">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="a8042-264">-1,000.00</span></span></td>
<td><span data-ttu-id="a8042-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-266">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-266">0.00</span></span></td>
<td><span data-ttu-id="a8042-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-268">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="a8042-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-269">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-270">5</span><span class="sxs-lookup"><span data-stu-id="a8042-270">5</span></span></td>
<td><span data-ttu-id="a8042-271">Кредиторская задолженность</span><span class="sxs-lookup"><span data-stu-id="a8042-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-272">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="a8042-272">-1,008.00</span></span></td>
<td><span data-ttu-id="a8042-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a8042-273">1,008.00</span></span></td>
<td><span data-ttu-id="a8042-274">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-275">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-276">6</span><span class="sxs-lookup"><span data-stu-id="a8042-276">6</span></span></td>
<td><span data-ttu-id="a8042-277">Актив ФПП</span><span class="sxs-lookup"><span data-stu-id="a8042-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-278">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="a8042-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="a8042-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-281">7</span><span class="sxs-lookup"><span data-stu-id="a8042-281">7</span></span></td>
<td><span data-ttu-id="a8042-282">Обязательство по финансовой аренде</span><span class="sxs-lookup"><span data-stu-id="a8042-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-283">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="a8042-284">-22,794.00</span></span></td>
<td><span data-ttu-id="a8042-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-285">1,000.00</span></span></td>
<td><span data-ttu-id="a8042-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="a8042-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="a8042-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-288">8</span><span class="sxs-lookup"><span data-stu-id="a8042-288">8</span></span></td>
<td><span data-ttu-id="a8042-289">Расходы на выплату процентов</span><span class="sxs-lookup"><span data-stu-id="a8042-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-290">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-291">94.97</span><span class="sxs-lookup"><span data-stu-id="a8042-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-292">94.97</span><span class="sxs-lookup"><span data-stu-id="a8042-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-293">9</span><span class="sxs-lookup"><span data-stu-id="a8042-293">9</span></span></td>
<td><span data-ttu-id="a8042-294">Касса</span><span class="sxs-lookup"><span data-stu-id="a8042-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-295">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="a8042-295">-1,008.00</span></span></td>
<td><span data-ttu-id="a8042-296">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="a8042-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-297">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="a8042-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-298">10</span><span class="sxs-lookup"><span data-stu-id="a8042-298">10</span></span></td>
<td><span data-ttu-id="a8042-299">Расходы на амортизацию</span><span class="sxs-lookup"><span data-stu-id="a8042-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-300">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-301">949.75</span><span class="sxs-lookup"><span data-stu-id="a8042-301">949.75</span></span></td>
<td><span data-ttu-id="a8042-302">949.75</span><span class="sxs-lookup"><span data-stu-id="a8042-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-303">11</span><span class="sxs-lookup"><span data-stu-id="a8042-303">11</span></span></td>
<td><span data-ttu-id="a8042-304">Накопленная амортизация</span><span class="sxs-lookup"><span data-stu-id="a8042-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-305">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="a8042-306">-949.75</span></span></td>
<td><span data-ttu-id="a8042-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="a8042-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8042-308">Как показано в предыдущей таблице, три книги требуются для обеспечения как регламентной отчетности, так и отчетности МСФО.</span><span class="sxs-lookup"><span data-stu-id="a8042-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="a8042-309">Регламентная книга записывает платеж по аренде в соответствии с правилами учета денежных средств в текущем слое.</span><span class="sxs-lookup"><span data-stu-id="a8042-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="a8042-310">В книге по регламентному сторнированию отменяются записи регламентного журнала.</span><span class="sxs-lookup"><span data-stu-id="a8042-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="a8042-311">Книга МСФО 16 создает записи журнала, которые необходимы в соответствии с МСФО 16.</span><span class="sxs-lookup"><span data-stu-id="a8042-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="a8042-312">Аренда должна быть введена только один раз.</span><span class="sxs-lookup"><span data-stu-id="a8042-312">You must enter a lease only one time.</span></span> <span data-ttu-id="a8042-313">Затем можно открыть страницу **Книги**, чтобы просмотреть все книги, связанные с арендой.</span><span class="sxs-lookup"><span data-stu-id="a8042-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="a8042-314">При создании книг все три из них должны быть связаны с одной и той же записью аренды.</span><span class="sxs-lookup"><span data-stu-id="a8042-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="a8042-315">Первая запись журнала записывает расходы на аренду в рамках регламентной книги.</span><span class="sxs-lookup"><span data-stu-id="a8042-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="a8042-316">Платежи можно создавать либо пакетом, либо путем выбора графика оплаты в регламентной книге.</span><span class="sxs-lookup"><span data-stu-id="a8042-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="a8042-317">В данном примере следующая запись журнала создается для регламентной книги из графика оплаты.</span><span class="sxs-lookup"><span data-stu-id="a8042-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="a8042-318">Арендный платеж — 31.01.2020 — JE 100</span><span class="sxs-lookup"><span data-stu-id="a8042-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="a8042-319">Тип счета</span><span class="sxs-lookup"><span data-stu-id="a8042-319">Account type</span></span> | <span data-ttu-id="a8042-320">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="a8042-320">Account number</span></span> | <span data-ttu-id="a8042-321">Слой</span><span class="sxs-lookup"><span data-stu-id="a8042-321">Layer</span></span>   | <span data-ttu-id="a8042-322">Описание счета</span><span class="sxs-lookup"><span data-stu-id="a8042-322">Account description</span></span> | <span data-ttu-id="a8042-323">по дебету</span><span class="sxs-lookup"><span data-stu-id="a8042-323">Debit</span></span>    | <span data-ttu-id="a8042-324">По кредиту</span><span class="sxs-lookup"><span data-stu-id="a8042-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="a8042-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-325">Ledger</span></span>       | <span data-ttu-id="a8042-326">1</span><span class="sxs-lookup"><span data-stu-id="a8042-326">1</span></span>              | <span data-ttu-id="a8042-327">Текущие</span><span class="sxs-lookup"><span data-stu-id="a8042-327">Current</span></span> | <span data-ttu-id="a8042-328">Расходы по аренде</span><span class="sxs-lookup"><span data-stu-id="a8042-328">Lease expense</span></span>       | <span data-ttu-id="a8042-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-329">1,000.00</span></span> |          |
| <span data-ttu-id="a8042-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-330">Ledger</span></span>       | <span data-ttu-id="a8042-331">4</span><span class="sxs-lookup"><span data-stu-id="a8042-331">4</span></span>              | <span data-ttu-id="a8042-332">Текущие</span><span class="sxs-lookup"><span data-stu-id="a8042-332">Current</span></span> | <span data-ttu-id="a8042-333">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="a8042-333">Clearing account</span></span>    |          | <span data-ttu-id="a8042-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-334">1,000.00</span></span> |

<span data-ttu-id="a8042-335">Служащий отдела расчетов с поставщиками использует стандартную функциональность Dynamics 365, чтобы создать накладную для оплаты за аренду за пределами модуля аренды актива.</span><span class="sxs-lookup"><span data-stu-id="a8042-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="a8042-336">Однако вместо того, чтобы выбирать **Расходы по аренде** в качестве дебетового счета, сотрудник отдела расчетов с поставщиками выбирает клиринговый счет для создания следующей записи.</span><span class="sxs-lookup"><span data-stu-id="a8042-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="a8042-337">Процесс AP — 31.01.2020 — JE 110</span><span class="sxs-lookup"><span data-stu-id="a8042-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="a8042-338">Тип счета</span><span class="sxs-lookup"><span data-stu-id="a8042-338">Account type</span></span> | <span data-ttu-id="a8042-339">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="a8042-339">Account number</span></span> | <span data-ttu-id="a8042-340">Слой</span><span class="sxs-lookup"><span data-stu-id="a8042-340">Layer</span></span>   | <span data-ttu-id="a8042-341">Описание счета</span><span class="sxs-lookup"><span data-stu-id="a8042-341">Account description</span></span> | <span data-ttu-id="a8042-342">по дебету</span><span class="sxs-lookup"><span data-stu-id="a8042-342">Debit</span></span>    | <span data-ttu-id="a8042-343">По кредиту</span><span class="sxs-lookup"><span data-stu-id="a8042-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="a8042-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-344">Ledger</span></span>       | <span data-ttu-id="a8042-345">4</span><span class="sxs-lookup"><span data-stu-id="a8042-345">4</span></span>              | <span data-ttu-id="a8042-346">Текущие</span><span class="sxs-lookup"><span data-stu-id="a8042-346">Current</span></span> | <span data-ttu-id="a8042-347">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="a8042-347">Clearing account</span></span>    | <span data-ttu-id="a8042-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-348">1,000.00</span></span> |          |
| <span data-ttu-id="a8042-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-349">Ledger</span></span>       | <span data-ttu-id="a8042-350">2</span><span class="sxs-lookup"><span data-stu-id="a8042-350">2</span></span>              | <span data-ttu-id="a8042-351">Текущие</span><span class="sxs-lookup"><span data-stu-id="a8042-351">Current</span></span> | <span data-ttu-id="a8042-352">Банковские сборы</span><span class="sxs-lookup"><span data-stu-id="a8042-352">Bank fee</span></span>            | <span data-ttu-id="a8042-353">3.00</span><span class="sxs-lookup"><span data-stu-id="a8042-353">3.00</span></span>     |          |
| <span data-ttu-id="a8042-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-354">Ledger</span></span>       | <span data-ttu-id="a8042-355">3</span><span class="sxs-lookup"><span data-stu-id="a8042-355">3</span></span>              | <span data-ttu-id="a8042-356">Текущие</span><span class="sxs-lookup"><span data-stu-id="a8042-356">Current</span></span> | <span data-ttu-id="a8042-357">Расходы на НДС</span><span class="sxs-lookup"><span data-stu-id="a8042-357">VAT expense</span></span>         | <span data-ttu-id="a8042-358">5.00</span><span class="sxs-lookup"><span data-stu-id="a8042-358">5.00</span></span>     |          |
| <span data-ttu-id="a8042-359">Поставщик</span><span class="sxs-lookup"><span data-stu-id="a8042-359">Vendor</span></span>       | <span data-ttu-id="a8042-360">5</span><span class="sxs-lookup"><span data-stu-id="a8042-360">5</span></span>              | <span data-ttu-id="a8042-361">Текущие</span><span class="sxs-lookup"><span data-stu-id="a8042-361">Current</span></span> | <span data-ttu-id="a8042-362">Кредиторская задолженность</span><span class="sxs-lookup"><span data-stu-id="a8042-362">Accounts payable</span></span>    |          | <span data-ttu-id="a8042-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a8042-363">1,008.00</span></span> |

<span data-ttu-id="a8042-364">Когда отчет выдается поставщику, вы следуете обычному процессу оплаты.</span><span class="sxs-lookup"><span data-stu-id="a8042-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="a8042-365">В ходе этого процесса создается следующая запись журнала.</span><span class="sxs-lookup"><span data-stu-id="a8042-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="a8042-366">Оплата наличными — 31.01.2020 — JE 120</span><span class="sxs-lookup"><span data-stu-id="a8042-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="a8042-367">Тип счета</span><span class="sxs-lookup"><span data-stu-id="a8042-367">Account type</span></span> | <span data-ttu-id="a8042-368">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="a8042-368">Account number</span></span> | <span data-ttu-id="a8042-369">Слой</span><span class="sxs-lookup"><span data-stu-id="a8042-369">Layer</span></span>   | <span data-ttu-id="a8042-370">Описание счета</span><span class="sxs-lookup"><span data-stu-id="a8042-370">Account description</span></span> | <span data-ttu-id="a8042-371">по дебету</span><span class="sxs-lookup"><span data-stu-id="a8042-371">Debit</span></span>    | <span data-ttu-id="a8042-372">По кредиту</span><span class="sxs-lookup"><span data-stu-id="a8042-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="a8042-373">Поставщик</span><span class="sxs-lookup"><span data-stu-id="a8042-373">Vendor</span></span>       | <span data-ttu-id="a8042-374">5</span><span class="sxs-lookup"><span data-stu-id="a8042-374">5</span></span>              | <span data-ttu-id="a8042-375">Текущие</span><span class="sxs-lookup"><span data-stu-id="a8042-375">Current</span></span> | <span data-ttu-id="a8042-376">Расчеты с поставщиками</span><span class="sxs-lookup"><span data-stu-id="a8042-376">Accounts Payable</span></span>    | <span data-ttu-id="a8042-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a8042-377">1,008.00</span></span> |          |
| <span data-ttu-id="a8042-378">Денежные средства</span><span class="sxs-lookup"><span data-stu-id="a8042-378">Bank</span></span>         | <span data-ttu-id="a8042-379">9</span><span class="sxs-lookup"><span data-stu-id="a8042-379">9</span></span>              | <span data-ttu-id="a8042-380">Текущие</span><span class="sxs-lookup"><span data-stu-id="a8042-380">Current</span></span> | <span data-ttu-id="a8042-381">Касса</span><span class="sxs-lookup"><span data-stu-id="a8042-381">Cash</span></span>                |          | <span data-ttu-id="a8042-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a8042-382">1,008.00</span></span> |

<span data-ttu-id="a8042-383">В этот момент вы полностью выполнили учет этой аренды в соответствии с регламентными требованиями к отчетности и можете создать пробный баланс с помощью текущего слоя.</span><span class="sxs-lookup"><span data-stu-id="a8042-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="a8042-384">Система возвращает пробный баланс со следующими показателями.</span><span class="sxs-lookup"><span data-stu-id="a8042-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="a8042-385">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="a8042-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="a8042-386">описание</span><span class="sxs-lookup"><span data-stu-id="a8042-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="a8042-387">Регламентная книга (текущий слой)</span><span class="sxs-lookup"><span data-stu-id="a8042-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="a8042-388">Текущий слой, итого</span><span class="sxs-lookup"><span data-stu-id="a8042-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a8042-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="a8042-389">JE-100</span></span></th>
<th><span data-ttu-id="a8042-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="a8042-390">JE-110</span></span></th>
<th><span data-ttu-id="a8042-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="a8042-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a8042-392">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="a8042-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a8042-393">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="a8042-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a8042-394">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="a8042-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8042-395">1</span><span class="sxs-lookup"><span data-stu-id="a8042-395">1</span></span></td>
<td><span data-ttu-id="a8042-396">Расходы по аренде</span><span class="sxs-lookup"><span data-stu-id="a8042-396">Lease expense</span></span></td>
<td><span data-ttu-id="a8042-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-399">2</span><span class="sxs-lookup"><span data-stu-id="a8042-399">2</span></span></td>
<td><span data-ttu-id="a8042-400">Банковские сборы</span><span class="sxs-lookup"><span data-stu-id="a8042-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-401">3.00</span><span class="sxs-lookup"><span data-stu-id="a8042-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-402">3.00</span><span class="sxs-lookup"><span data-stu-id="a8042-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-403">3</span><span class="sxs-lookup"><span data-stu-id="a8042-403">3</span></span></td>
<td><span data-ttu-id="a8042-404">Расходы на НДС</span><span class="sxs-lookup"><span data-stu-id="a8042-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-405">5.00</span><span class="sxs-lookup"><span data-stu-id="a8042-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-406">5.00</span><span class="sxs-lookup"><span data-stu-id="a8042-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-407">4</span><span class="sxs-lookup"><span data-stu-id="a8042-407">4</span></span></td>
<td><span data-ttu-id="a8042-408">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="a8042-408">Clearing account</span></span></td>
<td><span data-ttu-id="a8042-409">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="a8042-409">-1,000.00</span></span></td>
<td><span data-ttu-id="a8042-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-411">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-412">5</span><span class="sxs-lookup"><span data-stu-id="a8042-412">5</span></span></td>
<td><span data-ttu-id="a8042-413">Кредиторская задолженность</span><span class="sxs-lookup"><span data-stu-id="a8042-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="a8042-414">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="a8042-414">-1,008.00</span></span></td>
<td><span data-ttu-id="a8042-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a8042-415">1,008.00</span></span></td>
<td><span data-ttu-id="a8042-416">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-417">6</span><span class="sxs-lookup"><span data-stu-id="a8042-417">6</span></span></td>
<td><span data-ttu-id="a8042-418">Актив ФПП</span><span class="sxs-lookup"><span data-stu-id="a8042-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-419">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-420">7</span><span class="sxs-lookup"><span data-stu-id="a8042-420">7</span></span></td>
<td><span data-ttu-id="a8042-421">Обязательство по финансовой аренде</span><span class="sxs-lookup"><span data-stu-id="a8042-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-422">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-423">8</span><span class="sxs-lookup"><span data-stu-id="a8042-423">8</span></span></td>
<td><span data-ttu-id="a8042-424">Расходы на выплату процентов</span><span class="sxs-lookup"><span data-stu-id="a8042-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-425">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-426">9</span><span class="sxs-lookup"><span data-stu-id="a8042-426">9</span></span></td>
<td><span data-ttu-id="a8042-427">Касса</span><span class="sxs-lookup"><span data-stu-id="a8042-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-428">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="a8042-428">-1,008.00</span></span></td>
<td><span data-ttu-id="a8042-429">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="a8042-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-430">10</span><span class="sxs-lookup"><span data-stu-id="a8042-430">10</span></span></td>
<td><span data-ttu-id="a8042-431">Расходы на амортизацию</span><span class="sxs-lookup"><span data-stu-id="a8042-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-432">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8042-433">11</span><span class="sxs-lookup"><span data-stu-id="a8042-433">11</span></span></td>
<td><span data-ttu-id="a8042-434">Накопленная амортизация</span><span class="sxs-lookup"><span data-stu-id="a8042-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a8042-435">0.00</span><span class="sxs-lookup"><span data-stu-id="a8042-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8042-436">Если вы хотите использовать цифры МСФО 16 для запуска того же пробного баланса, записи журнала регламентного учета должны быть реверсированы, а записи журнала МСФО 16 должны быть разнесены.</span><span class="sxs-lookup"><span data-stu-id="a8042-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="a8042-437">Для реверсирования записей регламентного журнала этот пример включает регламентную книгу сторнирования с той же настройкой, что и у регламентной книги, но с противоположным профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="a8042-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="a8042-438">Например, регламентная книга *дебетовала* на счет расходов на аренду, но книга сторнирования будет *кредитовать* этот счет.</span><span class="sxs-lookup"><span data-stu-id="a8042-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="a8042-439">Эти связи легко определить в счетах разноски аренды активов на странице **Параметры аренды активов** (**Аренда активов \> Настройка \> Параметры аренды активов**).</span><span class="sxs-lookup"><span data-stu-id="a8042-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="a8042-440">При использовании того же процесса, который использовался для регламентной книги, используется для книги сторнирования, будет создана следующая запись журнала.</span><span class="sxs-lookup"><span data-stu-id="a8042-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="a8042-441">Разница заключается в том, что книга сторнирования резервирует записи сторнирования из регламентной книги.</span><span class="sxs-lookup"><span data-stu-id="a8042-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="a8042-442">Операции сторнирования также выполняются в пользовательском слое.</span><span class="sxs-lookup"><span data-stu-id="a8042-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="a8042-443">Когда пробный баланс запускается на текущем слое, операции журнала сторнирования не включаются.</span><span class="sxs-lookup"><span data-stu-id="a8042-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="a8042-444">Арендный платеж — 31.01.2020 — JE 130</span><span class="sxs-lookup"><span data-stu-id="a8042-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="a8042-445">Тип счета</span><span class="sxs-lookup"><span data-stu-id="a8042-445">Account type</span></span> | <span data-ttu-id="a8042-446">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="a8042-446">Account number</span></span> | <span data-ttu-id="a8042-447">Слой</span><span class="sxs-lookup"><span data-stu-id="a8042-447">Layer</span></span>  | <span data-ttu-id="a8042-448">Описание счета</span><span class="sxs-lookup"><span data-stu-id="a8042-448">Account description</span></span> | <span data-ttu-id="a8042-449">по дебету</span><span class="sxs-lookup"><span data-stu-id="a8042-449">Debit</span></span>    | <span data-ttu-id="a8042-450">По кредиту</span><span class="sxs-lookup"><span data-stu-id="a8042-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="a8042-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-451">Ledger</span></span>       | <span data-ttu-id="a8042-452">4</span><span class="sxs-lookup"><span data-stu-id="a8042-452">4</span></span>              | <span data-ttu-id="a8042-453">Произвольная</span><span class="sxs-lookup"><span data-stu-id="a8042-453">Custom</span></span> | <span data-ttu-id="a8042-454">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="a8042-454">Clearing account</span></span>    | <span data-ttu-id="a8042-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-455">1,000.00</span></span> |          |
| <span data-ttu-id="a8042-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-456">Ledger</span></span>       | <span data-ttu-id="a8042-457">1</span><span class="sxs-lookup"><span data-stu-id="a8042-457">1</span></span>              | <span data-ttu-id="a8042-458">Произвольная</span><span class="sxs-lookup"><span data-stu-id="a8042-458">Custom</span></span> | <span data-ttu-id="a8042-459">Расходы по аренде</span><span class="sxs-lookup"><span data-stu-id="a8042-459">Lease expense</span></span>       |          | <span data-ttu-id="a8042-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-460">1,000.00</span></span> |

<span data-ttu-id="a8042-461">После того, как записи регламентного журнала удалены, будут учтены все записи журнала, необходимые для МСФО 16 в книге МСФО 16.</span><span class="sxs-lookup"><span data-stu-id="a8042-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="a8042-462">Эти записи включают первоначальное признание актива ФПП и его обязательства, а также запись процента и амортизации.</span><span class="sxs-lookup"><span data-stu-id="a8042-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="a8042-463">Первоначальное признание — 01.01.2020 — JE 140</span><span class="sxs-lookup"><span data-stu-id="a8042-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="a8042-464">Тип счета</span><span class="sxs-lookup"><span data-stu-id="a8042-464">Account type</span></span> | <span data-ttu-id="a8042-465">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="a8042-465">Account number</span></span> | <span data-ttu-id="a8042-466">Слой</span><span class="sxs-lookup"><span data-stu-id="a8042-466">Layer</span></span>  | <span data-ttu-id="a8042-467">Описание счета</span><span class="sxs-lookup"><span data-stu-id="a8042-467">Account description</span></span>      | <span data-ttu-id="a8042-468">по дебету</span><span class="sxs-lookup"><span data-stu-id="a8042-468">Debit</span></span>     | <span data-ttu-id="a8042-469">По кредиту</span><span class="sxs-lookup"><span data-stu-id="a8042-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="a8042-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-470">Ledger</span></span>       | <span data-ttu-id="a8042-471">6</span><span class="sxs-lookup"><span data-stu-id="a8042-471">6</span></span>              | <span data-ttu-id="a8042-472">Произвольная</span><span class="sxs-lookup"><span data-stu-id="a8042-472">Custom</span></span> | <span data-ttu-id="a8042-473">Актив ФПП</span><span class="sxs-lookup"><span data-stu-id="a8042-473">ROU Asset</span></span>                | <span data-ttu-id="a8042-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="a8042-474">22,793.90</span></span> |           |
| <span data-ttu-id="a8042-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-475">Ledger</span></span>       | <span data-ttu-id="a8042-476">7</span><span class="sxs-lookup"><span data-stu-id="a8042-476">7</span></span>              | <span data-ttu-id="a8042-477">Произвольная</span><span class="sxs-lookup"><span data-stu-id="a8042-477">Custom</span></span> | <span data-ttu-id="a8042-478">Обязательство по финансовой аренде</span><span class="sxs-lookup"><span data-stu-id="a8042-478">Finance lease obligation</span></span> |           | <span data-ttu-id="a8042-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="a8042-479">22,793.90</span></span> |

<span data-ttu-id="a8042-480">Арендный платеж разносится как другие платежи по аренде.</span><span class="sxs-lookup"><span data-stu-id="a8042-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="a8042-481">Причиной использования клирингового счета является обеспечение того, что наличные деньги кредитуются только один раз.</span><span class="sxs-lookup"><span data-stu-id="a8042-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="a8042-482">Арендный платеж — 31.01.2020 — JE 150</span><span class="sxs-lookup"><span data-stu-id="a8042-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="a8042-483">Тип счета</span><span class="sxs-lookup"><span data-stu-id="a8042-483">Account type</span></span> | <span data-ttu-id="a8042-484">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="a8042-484">Account number</span></span> | <span data-ttu-id="a8042-485">Слой</span><span class="sxs-lookup"><span data-stu-id="a8042-485">Layer</span></span>  | <span data-ttu-id="a8042-486">Описание счета</span><span class="sxs-lookup"><span data-stu-id="a8042-486">Account description</span></span>      | <span data-ttu-id="a8042-487">по дебету</span><span class="sxs-lookup"><span data-stu-id="a8042-487">Debit</span></span>    | <span data-ttu-id="a8042-488">По кредиту</span><span class="sxs-lookup"><span data-stu-id="a8042-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="a8042-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-489">Ledger</span></span>       | <span data-ttu-id="a8042-490">7</span><span class="sxs-lookup"><span data-stu-id="a8042-490">7</span></span>              | <span data-ttu-id="a8042-491">Произвольная</span><span class="sxs-lookup"><span data-stu-id="a8042-491">Custom</span></span> | <span data-ttu-id="a8042-492">Обязательство по финансовой аренде</span><span class="sxs-lookup"><span data-stu-id="a8042-492">Finance lease obligation</span></span> | <span data-ttu-id="a8042-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-493">1,000.00</span></span> |          |
| <span data-ttu-id="a8042-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-494">Ledger</span></span>       | <span data-ttu-id="a8042-495">4</span><span class="sxs-lookup"><span data-stu-id="a8042-495">4</span></span>              | <span data-ttu-id="a8042-496">Произвольная</span><span class="sxs-lookup"><span data-stu-id="a8042-496">Custom</span></span> | <span data-ttu-id="a8042-497">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="a8042-497">Clearing account</span></span>         |          | <span data-ttu-id="a8042-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a8042-498">1,000.00</span></span> |

<span data-ttu-id="a8042-499">Запись журнала расходов по процентам создается на основе графика амортизации обязательств.</span><span class="sxs-lookup"><span data-stu-id="a8042-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="a8042-500">Расходы на выплату процентов — 31.01.2020 — JE 160</span><span class="sxs-lookup"><span data-stu-id="a8042-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="a8042-501">Тип счета</span><span class="sxs-lookup"><span data-stu-id="a8042-501">Account type</span></span> | <span data-ttu-id="a8042-502">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="a8042-502">Account number</span></span> | <span data-ttu-id="a8042-503">Слой</span><span class="sxs-lookup"><span data-stu-id="a8042-503">Layer</span></span>  | <span data-ttu-id="a8042-504">Описание счета</span><span class="sxs-lookup"><span data-stu-id="a8042-504">Account description</span></span>      | <span data-ttu-id="a8042-505">по дебету</span><span class="sxs-lookup"><span data-stu-id="a8042-505">Debit</span></span> | <span data-ttu-id="a8042-506">По кредиту</span><span class="sxs-lookup"><span data-stu-id="a8042-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="a8042-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-507">Ledger</span></span>       | <span data-ttu-id="a8042-508">8</span><span class="sxs-lookup"><span data-stu-id="a8042-508">8</span></span>              | <span data-ttu-id="a8042-509">Произвольная</span><span class="sxs-lookup"><span data-stu-id="a8042-509">Custom</span></span> | <span data-ttu-id="a8042-510">Расходы на выплату процентов</span><span class="sxs-lookup"><span data-stu-id="a8042-510">Interest expense</span></span>         | <span data-ttu-id="a8042-511">94.97</span><span class="sxs-lookup"><span data-stu-id="a8042-511">94.97</span></span> |        |
| <span data-ttu-id="a8042-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-512">Ledger</span></span>       | <span data-ttu-id="a8042-513">7</span><span class="sxs-lookup"><span data-stu-id="a8042-513">7</span></span>              | <span data-ttu-id="a8042-514">Произвольная</span><span class="sxs-lookup"><span data-stu-id="a8042-514">Custom</span></span> | <span data-ttu-id="a8042-515">Обязательство по финансовой аренде</span><span class="sxs-lookup"><span data-stu-id="a8042-515">Finance lease obligation</span></span> |       | <span data-ttu-id="a8042-516">94.97</span><span class="sxs-lookup"><span data-stu-id="a8042-516">94.97</span></span>  |

<span data-ttu-id="a8042-517">Запись журнала расходов по амортизации создается на основе графика амортизации активов.</span><span class="sxs-lookup"><span data-stu-id="a8042-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="a8042-518">Амортизационные расходы — 31.01.2020 — JE 170</span><span class="sxs-lookup"><span data-stu-id="a8042-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="a8042-519">Тип счета</span><span class="sxs-lookup"><span data-stu-id="a8042-519">Account type</span></span> | <span data-ttu-id="a8042-520">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="a8042-520">Account number</span></span> | <span data-ttu-id="a8042-521">Слой</span><span class="sxs-lookup"><span data-stu-id="a8042-521">Layer</span></span>  | <span data-ttu-id="a8042-522">Описание счета</span><span class="sxs-lookup"><span data-stu-id="a8042-522">Account description</span></span>      | <span data-ttu-id="a8042-523">по дебету</span><span class="sxs-lookup"><span data-stu-id="a8042-523">Debit</span></span>  | <span data-ttu-id="a8042-524">По кредиту</span><span class="sxs-lookup"><span data-stu-id="a8042-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="a8042-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-525">Ledger</span></span>       | <span data-ttu-id="a8042-526">10</span><span class="sxs-lookup"><span data-stu-id="a8042-526">10</span></span>             | <span data-ttu-id="a8042-527">Произвольная</span><span class="sxs-lookup"><span data-stu-id="a8042-527">Custom</span></span> | <span data-ttu-id="a8042-528">Расходы на амортизацию</span><span class="sxs-lookup"><span data-stu-id="a8042-528">Depreciation expense</span></span>     | <span data-ttu-id="a8042-529">949.75</span><span class="sxs-lookup"><span data-stu-id="a8042-529">949.75</span></span> |        |
| <span data-ttu-id="a8042-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="a8042-530">Ledger</span></span>       | <span data-ttu-id="a8042-531">11</span><span class="sxs-lookup"><span data-stu-id="a8042-531">11</span></span>             | <span data-ttu-id="a8042-532">Произвольная</span><span class="sxs-lookup"><span data-stu-id="a8042-532">Custom</span></span> | <span data-ttu-id="a8042-533">Накопленная амортизация</span><span class="sxs-lookup"><span data-stu-id="a8042-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="a8042-534">949.75</span><span class="sxs-lookup"><span data-stu-id="a8042-534">949.75</span></span> |

<span data-ttu-id="a8042-535">После создания и разноски всех этих записей журнала будут отображены следующие значения "пользовательского слоя 1".</span><span class="sxs-lookup"><span data-stu-id="a8042-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="a8042-536">Обратите внимание, что последний столбец включает банковские сборы, расход на налог на добавленную стоимость (НДС) и сокращение наличности из предыдущего слоя, но не включает записи журнала регламентной отчетности.</span><span class="sxs-lookup"><span data-stu-id="a8042-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="a8042-537">Таким образом, вы достигли истинных возможностей двойной отчетности.</span><span class="sxs-lookup"><span data-stu-id="a8042-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="a8042-538">На этом этапе компании просто требуется выполнить свой пробный баланс и объединить текущий слой и пользовательский слой для создания пробного баланса МСФО.</span><span class="sxs-lookup"><span data-stu-id="a8042-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="a8042-539">Номер счета</span><span class="sxs-lookup"><span data-stu-id="a8042-539">Account No</span></span> | <span data-ttu-id="a8042-540">описание</span><span class="sxs-lookup"><span data-stu-id="a8042-540">Description</span></span>              | <span data-ttu-id="a8042-541">Регламентная книга\-Текущий слой\-JE\-100\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="a8042-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="a8042-542">Регламентная книга\-Текущий слой\-JE\-110\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="a8042-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="a8042-543">Регламентная книга\-Текущий слой\-JE\-120\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="a8042-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="a8042-544">Текущий слой \- Итого</span><span class="sxs-lookup"><span data-stu-id="a8042-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="a8042-545">Книга сторнирования\-Пользовательский слой\-JE\-130\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="a8042-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="a8042-546">Книга МСФО 16\-Пользовательский слой\-JE\-140\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="a8042-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="a8042-547">Книга МСФО 16\-Пользовательский слой\-JE\-150\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="a8042-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="a8042-548">Книга МСФО 16\-Пользовательский слой\-JE\-160\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="a8042-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="a8042-549">Книга МСФО 16\-Пользовательский слой\-JE\-170\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="a8042-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="a8042-550">Текущий слой \+ Текущий слой \- Итого</span><span class="sxs-lookup"><span data-stu-id="a8042-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="a8042-551">1</span><span class="sxs-lookup"><span data-stu-id="a8042-551">1</span></span>          | <span data-ttu-id="a8042-552">Расходы по аренде</span><span class="sxs-lookup"><span data-stu-id="a8042-552">Lease expense</span></span>            | <span data-ttu-id="a8042-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="a8042-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-554">1,000\.00</span></span>               |   | <span data-ttu-id="a8042-555">\-1 000</span><span class="sxs-lookup"><span data-stu-id="a8042-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="a8042-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-556">0\.00</span></span>                                   |
| <span data-ttu-id="a8042-557">2</span><span class="sxs-lookup"><span data-stu-id="a8042-557">2</span></span>          | <span data-ttu-id="a8042-558">Банковские сборы</span><span class="sxs-lookup"><span data-stu-id="a8042-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="a8042-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="a8042-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="a8042-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-561">3\.00</span></span>                                   |
| <span data-ttu-id="a8042-562">3</span><span class="sxs-lookup"><span data-stu-id="a8042-562">3</span></span>          | <span data-ttu-id="a8042-563">Расходы на НДС</span><span class="sxs-lookup"><span data-stu-id="a8042-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="a8042-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="a8042-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="a8042-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-566">5\.00</span></span>                                   |
| <span data-ttu-id="a8042-567">4</span><span class="sxs-lookup"><span data-stu-id="a8042-567">4</span></span>          | <span data-ttu-id="a8042-568">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="a8042-568">Clearing account</span></span>         | <span data-ttu-id="a8042-569">\-1 000\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="a8042-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="a8042-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-571">0\.00</span></span>                   |   | <span data-ttu-id="a8042-572">1000</span><span class="sxs-lookup"><span data-stu-id="a8042-572">1,000</span></span>                                           |                                                | <span data-ttu-id="a8042-573">\-1 000</span><span class="sxs-lookup"><span data-stu-id="a8042-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="a8042-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-574">0\.00</span></span>                                   |
| <span data-ttu-id="a8042-575">5</span><span class="sxs-lookup"><span data-stu-id="a8042-575">5</span></span>          | <span data-ttu-id="a8042-576">Кредиторская задолженность</span><span class="sxs-lookup"><span data-stu-id="a8042-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="a8042-577">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="a8042-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-578">1,008\.00</span></span>                                         | <span data-ttu-id="a8042-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="a8042-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-580">0\.00</span></span>                                   |
| <span data-ttu-id="a8042-581">6</span><span class="sxs-lookup"><span data-stu-id="a8042-581">6</span></span>          | <span data-ttu-id="a8042-582">Актив ФПП</span><span class="sxs-lookup"><span data-stu-id="a8042-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="a8042-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="a8042-584">22,794</span><span class="sxs-lookup"><span data-stu-id="a8042-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="a8042-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="a8042-585">22,793\.90</span></span>                              |
| <span data-ttu-id="a8042-586">7</span><span class="sxs-lookup"><span data-stu-id="a8042-586">7</span></span>          | <span data-ttu-id="a8042-587">Обязательство по финансовой аренде</span><span class="sxs-lookup"><span data-stu-id="a8042-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="a8042-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="a8042-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="a8042-589">\-22,794</span></span>                                       | <span data-ttu-id="a8042-590">1000</span><span class="sxs-lookup"><span data-stu-id="a8042-590">1,000</span></span>                                          | <span data-ttu-id="a8042-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="a8042-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="a8042-592">\-21 888\.87</span><span class="sxs-lookup"><span data-stu-id="a8042-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="a8042-593">8</span><span class="sxs-lookup"><span data-stu-id="a8042-593">8</span></span>          | <span data-ttu-id="a8042-594">Расходы на выплату процентов</span><span class="sxs-lookup"><span data-stu-id="a8042-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="a8042-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="a8042-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="a8042-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="a8042-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="a8042-597">94\.97</span></span>                                  |
| <span data-ttu-id="a8042-598">9</span><span class="sxs-lookup"><span data-stu-id="a8042-598">9</span></span>          | <span data-ttu-id="a8042-599">Касса</span><span class="sxs-lookup"><span data-stu-id="a8042-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="a8042-600">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="a8042-601">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="a8042-602">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="a8042-603">10</span><span class="sxs-lookup"><span data-stu-id="a8042-603">10</span></span>         | <span data-ttu-id="a8042-604">Расходы на амортизацию</span><span class="sxs-lookup"><span data-stu-id="a8042-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="a8042-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="a8042-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="a8042-606">949\.75</span></span>                                        | <span data-ttu-id="a8042-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="a8042-607">949\.75</span></span>                                 |
| <span data-ttu-id="a8042-608">11</span><span class="sxs-lookup"><span data-stu-id="a8042-608">11</span></span>         | <span data-ttu-id="a8042-609">Накопленная амортизация</span><span class="sxs-lookup"><span data-stu-id="a8042-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="a8042-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="a8042-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="a8042-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="a8042-611">\-949\.75</span></span>                                      | <span data-ttu-id="a8042-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="a8042-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]