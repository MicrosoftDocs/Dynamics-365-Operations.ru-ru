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
ms.openlocfilehash: a7d9b3ea3d4f1d48b8a7326bd5a01d3119310c62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003189"
---
# <a name="dual-reporting"></a><span data-ttu-id="860a6-103">Двойная отчетность</span><span class="sxs-lookup"><span data-stu-id="860a6-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="860a6-104">В этой теме рассматривается пример, показывающий, как можно выполнить требования как для международной финансовой отчетности по стандарту МСФО, так и для регламентной отчетности в аренде активов.</span><span class="sxs-lookup"><span data-stu-id="860a6-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="860a6-105">Знакомство с уровнями разноски в Microsoft Dynamics 365 Finance является обязательным и облегчит понимание этого примера.</span><span class="sxs-lookup"><span data-stu-id="860a6-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="860a6-106">Пример</span><span class="sxs-lookup"><span data-stu-id="860a6-106">Example</span></span>

<span data-ttu-id="860a6-107">Следующий пример счетов для аренды в соответствии с итальянскими нормативными отчетами с использованием обоих методов расчета наличных денег и способов отчетности МСФО.</span><span class="sxs-lookup"><span data-stu-id="860a6-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="860a6-108">Компания должна создать три книги для учета как для итальянских регламентных требований, так и требований МСФО 16.</span><span class="sxs-lookup"><span data-stu-id="860a6-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="860a6-109">Для МСФО 16 требуется одна книга, одна книга требуется которой для регламентных требований, и одна книга требуется для автоматической реверсирования регламентных разносок.</span><span class="sxs-lookup"><span data-stu-id="860a6-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="860a6-110">Книги настраиваются так, как показано в следующих таблицах.</span><span class="sxs-lookup"><span data-stu-id="860a6-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="860a6-111">**Книга МСФО 16**</span><span class="sxs-lookup"><span data-stu-id="860a6-111">**IFRS 16 book**</span></span>

<span data-ttu-id="860a6-112">Книга МСФО 16 настроена таким образом, что она соответствует стандарту отчетности МСФО 16.</span><span class="sxs-lookup"><span data-stu-id="860a6-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="860a6-113">Все записи, учитываемые в этой книге, будут разнесены в пользовательский слой.</span><span class="sxs-lookup"><span data-stu-id="860a6-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="860a6-114">Наименование</span><span class="sxs-lookup"><span data-stu-id="860a6-114">Name</span></span>                                    | <span data-ttu-id="860a6-115">описание</span><span class="sxs-lookup"><span data-stu-id="860a6-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="860a6-116">Тип книги</span><span class="sxs-lookup"><span data-stu-id="860a6-116">Book type</span></span>                               | <span data-ttu-id="860a6-117">МСФО 16</span><span class="sxs-lookup"><span data-stu-id="860a6-117">IFRS 16</span></span>        |
| <span data-ttu-id="860a6-118">Бухгалтерская запись</span><span class="sxs-lookup"><span data-stu-id="860a6-118">Book description</span></span>                        | <span data-ttu-id="860a6-119">МСФО 16</span><span class="sxs-lookup"><span data-stu-id="860a6-119">IFRS 16</span></span>        |
| <span data-ttu-id="860a6-120">Слой разноски</span><span class="sxs-lookup"><span data-stu-id="860a6-120">Posting Layer</span></span>                           | <span data-ttu-id="860a6-121">Пользовательский слой 1</span><span class="sxs-lookup"><span data-stu-id="860a6-121">Custom layer 1</span></span> |
| <span data-ttu-id="860a6-122">Тип аренды</span><span class="sxs-lookup"><span data-stu-id="860a6-122">Lease Type</span></span>                              | <span data-ttu-id="860a6-123">Finance</span><span class="sxs-lookup"><span data-stu-id="860a6-123">Finance</span></span>        |
| <span data-ttu-id="860a6-124">Платформа учета</span><span class="sxs-lookup"><span data-stu-id="860a6-124">Accounting Framework</span></span>                    | <span data-ttu-id="860a6-125">МСФО 16</span><span class="sxs-lookup"><span data-stu-id="860a6-125">IFRS 16</span></span>        |
| <span data-ttu-id="860a6-126">Настройка отношения срока аренды к сроку службы</span><span class="sxs-lookup"><span data-stu-id="860a6-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="860a6-127">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-127">0.00</span></span>           |
| <span data-ttu-id="860a6-128">Настройка отношения "Текущая стоимость / Реальная стоимость актива"</span><span class="sxs-lookup"><span data-stu-id="860a6-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="860a6-129">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-129">0.00</span></span>           |
| <span data-ttu-id="860a6-130">Порог краткосрочной аренды</span><span class="sxs-lookup"><span data-stu-id="860a6-130">Short-term threshold</span></span>                    | <span data-ttu-id="860a6-131">12</span><span class="sxs-lookup"><span data-stu-id="860a6-131">12</span></span>             |
| <span data-ttu-id="860a6-132">Порог аренды малоценного актива</span><span class="sxs-lookup"><span data-stu-id="860a6-132">Low Value Threshold</span></span>                     | <span data-ttu-id="860a6-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-133">5,000.00</span></span>       |
| <span data-ttu-id="860a6-134">Оплата поставщику</span><span class="sxs-lookup"><span data-stu-id="860a6-134">Pay to Vendor</span></span>                           | <span data-ttu-id="860a6-135">Нет</span><span class="sxs-lookup"><span data-stu-id="860a6-135">No</span></span>             |

<span data-ttu-id="860a6-136">**Регламентная книга**</span><span class="sxs-lookup"><span data-stu-id="860a6-136">**Statutory book**</span></span>

<span data-ttu-id="860a6-137">Регламентная книга — это книга на основе наличных, в которой компания будет учитывать расходы на аренду в качестве суммы денежных средств, выплачиваемых ежемесячно за аренду.</span><span class="sxs-lookup"><span data-stu-id="860a6-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="860a6-138">Эта книга не будет создавать актив в форме права пользования или арендного обязательства.</span><span class="sxs-lookup"><span data-stu-id="860a6-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="860a6-139">Наименование</span><span class="sxs-lookup"><span data-stu-id="860a6-139">Name</span></span>                                    | <span data-ttu-id="860a6-140">описание</span><span class="sxs-lookup"><span data-stu-id="860a6-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="860a6-141">Тип книги</span><span class="sxs-lookup"><span data-stu-id="860a6-141">Book type</span></span>                               | <span data-ttu-id="860a6-142">Регламентная</span><span class="sxs-lookup"><span data-stu-id="860a6-142">Statutory</span></span>   |
| <span data-ttu-id="860a6-143">Бухгалтерская запись</span><span class="sxs-lookup"><span data-stu-id="860a6-143">Book description</span></span>                        | <span data-ttu-id="860a6-144">Локальная GAAP</span><span class="sxs-lookup"><span data-stu-id="860a6-144">Local GAAP</span></span>  |
| <span data-ttu-id="860a6-145">Слой разноски</span><span class="sxs-lookup"><span data-stu-id="860a6-145">Posting Layer</span></span>                           | <span data-ttu-id="860a6-146">Текущие</span><span class="sxs-lookup"><span data-stu-id="860a6-146">Current</span></span>     |
| <span data-ttu-id="860a6-147">Тип аренды</span><span class="sxs-lookup"><span data-stu-id="860a6-147">Lease Type</span></span>                              | <span data-ttu-id="860a6-148">Автоматически</span><span class="sxs-lookup"><span data-stu-id="860a6-148">Automatic</span></span>   |
| <span data-ttu-id="860a6-149">Платформа учета</span><span class="sxs-lookup"><span data-stu-id="860a6-149">Accounting Framework</span></span>                    | <span data-ttu-id="860a6-150">Кассовый метод</span><span class="sxs-lookup"><span data-stu-id="860a6-150">Cash basis</span></span>  |
| <span data-ttu-id="860a6-151">Настройка отношения срока аренды к сроку службы</span><span class="sxs-lookup"><span data-stu-id="860a6-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="860a6-152">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-152">0.00</span></span>        |
| <span data-ttu-id="860a6-153">Настройка отношения "Текущая стоимость / Реальная стоимость актива"</span><span class="sxs-lookup"><span data-stu-id="860a6-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="860a6-154">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-154">0.00</span></span>        |
| <span data-ttu-id="860a6-155">Порог краткосрочной аренды</span><span class="sxs-lookup"><span data-stu-id="860a6-155">Short-term threshold</span></span>                    | <span data-ttu-id="860a6-156">0</span><span class="sxs-lookup"><span data-stu-id="860a6-156">0</span></span>           |
| <span data-ttu-id="860a6-157">Порог аренды малоценного актива</span><span class="sxs-lookup"><span data-stu-id="860a6-157">Low Value Threshold</span></span>                     | <span data-ttu-id="860a6-158">0</span><span class="sxs-lookup"><span data-stu-id="860a6-158">0</span></span>           |
| <span data-ttu-id="860a6-159">Оплата поставщику</span><span class="sxs-lookup"><span data-stu-id="860a6-159">Pay to Vendor</span></span>                           | <span data-ttu-id="860a6-160">Нет</span><span class="sxs-lookup"><span data-stu-id="860a6-160">No</span></span>          |

<span data-ttu-id="860a6-161">**Книга регламентного сторнирования**</span><span class="sxs-lookup"><span data-stu-id="860a6-161">**Statutory reversal book**</span></span>

<span data-ttu-id="860a6-162">Книга регламентного сторнирования настраивается так же, как и регламентная книга.</span><span class="sxs-lookup"><span data-stu-id="860a6-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="860a6-163">Наименование</span><span class="sxs-lookup"><span data-stu-id="860a6-163">Name</span></span>                                    | <span data-ttu-id="860a6-164">описание</span><span class="sxs-lookup"><span data-stu-id="860a6-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="860a6-165">Тип книги</span><span class="sxs-lookup"><span data-stu-id="860a6-165">Book type</span></span>                               | <span data-ttu-id="860a6-166">Регламентная — сторнирование</span><span class="sxs-lookup"><span data-stu-id="860a6-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="860a6-167">Бухгалтерская запись</span><span class="sxs-lookup"><span data-stu-id="860a6-167">Book description</span></span>                        | <span data-ttu-id="860a6-168">Книга для сторнирования регламентной книги</span><span class="sxs-lookup"><span data-stu-id="860a6-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="860a6-169">Слой разноски</span><span class="sxs-lookup"><span data-stu-id="860a6-169">Posting Layer</span></span>                           | <span data-ttu-id="860a6-170">Пользовательский слой 1</span><span class="sxs-lookup"><span data-stu-id="860a6-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="860a6-171">Тип аренды</span><span class="sxs-lookup"><span data-stu-id="860a6-171">Lease Type</span></span>                              | <span data-ttu-id="860a6-172">Автоматически</span><span class="sxs-lookup"><span data-stu-id="860a6-172">Automatic</span></span>                      |
| <span data-ttu-id="860a6-173">Платформа учета</span><span class="sxs-lookup"><span data-stu-id="860a6-173">Accounting Framework</span></span>                    | <span data-ttu-id="860a6-174">Кассовый метод</span><span class="sxs-lookup"><span data-stu-id="860a6-174">Cash basis</span></span>                     |
| <span data-ttu-id="860a6-175">Настройка отношения срока аренды к сроку службы</span><span class="sxs-lookup"><span data-stu-id="860a6-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="860a6-176">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-176">0.00</span></span>                           |
| <span data-ttu-id="860a6-177">Настройка отношения "Текущая стоимость / Реальная стоимость актива"</span><span class="sxs-lookup"><span data-stu-id="860a6-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="860a6-178">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-178">0.00</span></span>                           |
| <span data-ttu-id="860a6-179">Порог краткосрочной аренды</span><span class="sxs-lookup"><span data-stu-id="860a6-179">Short-term threshold</span></span>                    | <span data-ttu-id="860a6-180">0</span><span class="sxs-lookup"><span data-stu-id="860a6-180">0</span></span>                              |
| <span data-ttu-id="860a6-181">Порог аренды малоценного актива</span><span class="sxs-lookup"><span data-stu-id="860a6-181">Low Value Threshold</span></span>                     | <span data-ttu-id="860a6-182">0</span><span class="sxs-lookup"><span data-stu-id="860a6-182">0</span></span>                              |
| <span data-ttu-id="860a6-183">Оплата поставщику</span><span class="sxs-lookup"><span data-stu-id="860a6-183">Pay to Vendor</span></span>                           | <span data-ttu-id="860a6-184">Нет</span><span class="sxs-lookup"><span data-stu-id="860a6-184">No</span></span>                             |

<span data-ttu-id="860a6-185">В данном примере была создана аренда со следующими настройками на вкладках **Общие** и **Строки графика платежей**.</span><span class="sxs-lookup"><span data-stu-id="860a6-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="860a6-186">**Вкладка "Общие"**</span><span class="sxs-lookup"><span data-stu-id="860a6-186">**General tab**</span></span>

| <span data-ttu-id="860a6-187">Поле</span><span class="sxs-lookup"><span data-stu-id="860a6-187">Field</span></span>                      | <span data-ttu-id="860a6-188">значение</span><span class="sxs-lookup"><span data-stu-id="860a6-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="860a6-189">Приростная ставка процента на заемный капитал</span><span class="sxs-lookup"><span data-stu-id="860a6-189">Incremental borrowing rate</span></span> | <span data-ttu-id="860a6-190">5%</span><span class="sxs-lookup"><span data-stu-id="860a6-190">5%</span></span>               |
| <span data-ttu-id="860a6-191">Дата начала</span><span class="sxs-lookup"><span data-stu-id="860a6-191">Commencement date</span></span>          | <span data-ttu-id="860a6-192">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="860a6-192">1/1/2020</span></span>         |
| <span data-ttu-id="860a6-193">Группа аренды</span><span class="sxs-lookup"><span data-stu-id="860a6-193">Lease group</span></span>                | <span data-ttu-id="860a6-194">Постройки</span><span class="sxs-lookup"><span data-stu-id="860a6-194">Buildings</span></span>        |
| <span data-ttu-id="860a6-195">Поставщик</span><span class="sxs-lookup"><span data-stu-id="860a6-195">Vendor</span></span>                     | <span data-ttu-id="860a6-196">1001</span><span class="sxs-lookup"><span data-stu-id="860a6-196">1001</span></span>             |
| <span data-ttu-id="860a6-197">Реальная стоимость актива</span><span class="sxs-lookup"><span data-stu-id="860a6-197">Fair value of the asset</span></span>    | <span data-ttu-id="860a6-198">245,000</span><span class="sxs-lookup"><span data-stu-id="860a6-198">245,000</span></span>          |
| <span data-ttu-id="860a6-199">Срок службы актива</span><span class="sxs-lookup"><span data-stu-id="860a6-199">Asset useful life</span></span>          | <span data-ttu-id="860a6-200">120</span><span class="sxs-lookup"><span data-stu-id="860a6-200">120</span></span>              |
| <span data-ttu-id="860a6-201">Тип аннуитета</span><span class="sxs-lookup"><span data-stu-id="860a6-201">Annuity type</span></span>               | <span data-ttu-id="860a6-202">Аннуитет постнумерандо</span><span class="sxs-lookup"><span data-stu-id="860a6-202">Ordinary annuity</span></span> |
| <span data-ttu-id="860a6-203">Интервал объединения</span><span class="sxs-lookup"><span data-stu-id="860a6-203">Compounding interval</span></span>       | <span data-ttu-id="860a6-204">ежемесячно</span><span class="sxs-lookup"><span data-stu-id="860a6-204">Monthly</span></span>          |

<span data-ttu-id="860a6-205">**Вкладка "Строки графика платежей"**</span><span class="sxs-lookup"><span data-stu-id="860a6-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="860a6-206">Поле</span><span class="sxs-lookup"><span data-stu-id="860a6-206">Field</span></span>             | <span data-ttu-id="860a6-207">значение</span><span class="sxs-lookup"><span data-stu-id="860a6-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="860a6-208">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="860a6-208">Start date</span></span>        | <span data-ttu-id="860a6-209">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="860a6-209">1/1/2020</span></span>   |
| <span data-ttu-id="860a6-210">Интервал периода</span><span class="sxs-lookup"><span data-stu-id="860a6-210">Period interval</span></span>   | <span data-ttu-id="860a6-211">Месяцы</span><span class="sxs-lookup"><span data-stu-id="860a6-211">Months</span></span>     |
| <span data-ttu-id="860a6-212">Периоды</span><span class="sxs-lookup"><span data-stu-id="860a6-212">Periods</span></span>           | <span data-ttu-id="860a6-213">24</span><span class="sxs-lookup"><span data-stu-id="860a6-213">24</span></span>         |
| <span data-ttu-id="860a6-214">Конечная дата</span><span class="sxs-lookup"><span data-stu-id="860a6-214">End date</span></span>          | <span data-ttu-id="860a6-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="860a6-215">12/31/2020</span></span> |
| <span data-ttu-id="860a6-216">Частота платежей</span><span class="sxs-lookup"><span data-stu-id="860a6-216">Payment frequency</span></span> | <span data-ttu-id="860a6-217">ежемесячно</span><span class="sxs-lookup"><span data-stu-id="860a6-217">Monthly</span></span>    |
| <span data-ttu-id="860a6-218">Сумма оплаты</span><span class="sxs-lookup"><span data-stu-id="860a6-218">Payment amount</span></span>    | <span data-ttu-id="860a6-219">1000</span><span class="sxs-lookup"><span data-stu-id="860a6-219">1,000</span></span>      |

<span data-ttu-id="860a6-220">Для учета данной аренды с помощью двух платформ используется текущий слой разноски и пользовательский слой разноски.</span><span class="sxs-lookup"><span data-stu-id="860a6-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="860a6-221">В следующей таблице показан пример каждой записи в журнале, которая требуется для правильного представления финансовых данных в соответствии с каждым стандартом отчетности.</span><span class="sxs-lookup"><span data-stu-id="860a6-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="860a6-222">Подробное описание каждой записи в журнале для первого месяца аренды предоставляется впоследствии.</span><span class="sxs-lookup"><span data-stu-id="860a6-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="860a6-223">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="860a6-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="860a6-224">описание</span><span class="sxs-lookup"><span data-stu-id="860a6-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="860a6-225">Регламентная книга (текущий слой)</span><span class="sxs-lookup"><span data-stu-id="860a6-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="860a6-226">Текущий слой, итого</span><span class="sxs-lookup"><span data-stu-id="860a6-226">Current layer total</span></span></th>
<th><span data-ttu-id="860a6-227">Книга сторнирования (настраиваемый слой)</span><span class="sxs-lookup"><span data-stu-id="860a6-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="860a6-228">Книга МСФО 16 (настраиваемый слой)</span><span class="sxs-lookup"><span data-stu-id="860a6-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="860a6-229">Текущий слой + пользовательский слой, итого</span><span class="sxs-lookup"><span data-stu-id="860a6-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="860a6-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="860a6-230">JE-100</span></span></th>
<th><span data-ttu-id="860a6-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="860a6-231">JE-110</span></span></th>
<th><span data-ttu-id="860a6-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="860a6-232">JE-120</span></span></th>
<th><span data-ttu-id="860a6-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="860a6-233">JE-130</span></span></th>
<th><span data-ttu-id="860a6-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="860a6-234">JE-140</span></span></th>
<th><span data-ttu-id="860a6-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="860a6-235">JE-150</span></span></th>
<th><span data-ttu-id="860a6-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="860a6-236">JE-160</span></span></th>
<th><span data-ttu-id="860a6-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="860a6-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="860a6-238">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="860a6-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="860a6-239">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="860a6-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="860a6-240">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="860a6-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="860a6-241">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="860a6-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="860a6-242">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="860a6-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="860a6-243">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="860a6-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="860a6-244">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="860a6-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="860a6-245">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="860a6-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="860a6-246">1</span><span class="sxs-lookup"><span data-stu-id="860a6-246">1</span></span></td>
<td><span data-ttu-id="860a6-247">Расходы по аренде</span><span class="sxs-lookup"><span data-stu-id="860a6-247">Lease expense</span></span></td>
<td><span data-ttu-id="860a6-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-249">1,000.00</span></span></td>
<td><span data-ttu-id="860a6-250">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="860a6-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-251">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-252">2</span><span class="sxs-lookup"><span data-stu-id="860a6-252">2</span></span></td>
<td><span data-ttu-id="860a6-253">Банковские сборы</span><span class="sxs-lookup"><span data-stu-id="860a6-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-254">3.00</span><span class="sxs-lookup"><span data-stu-id="860a6-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-255">3.00</span><span class="sxs-lookup"><span data-stu-id="860a6-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-256">3.00</span><span class="sxs-lookup"><span data-stu-id="860a6-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-257">3</span><span class="sxs-lookup"><span data-stu-id="860a6-257">3</span></span></td>
<td><span data-ttu-id="860a6-258">Расходы на НДС</span><span class="sxs-lookup"><span data-stu-id="860a6-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-259">5.00</span><span class="sxs-lookup"><span data-stu-id="860a6-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-260">5.00</span><span class="sxs-lookup"><span data-stu-id="860a6-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-261">5.00</span><span class="sxs-lookup"><span data-stu-id="860a6-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-262">4</span><span class="sxs-lookup"><span data-stu-id="860a6-262">4</span></span></td>
<td><span data-ttu-id="860a6-263">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="860a6-263">Clearing account</span></span></td>
<td><span data-ttu-id="860a6-264">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="860a6-264">-1,000.00</span></span></td>
<td><span data-ttu-id="860a6-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-266">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-266">0.00</span></span></td>
<td><span data-ttu-id="860a6-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-268">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="860a6-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-269">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-270">5</span><span class="sxs-lookup"><span data-stu-id="860a6-270">5</span></span></td>
<td><span data-ttu-id="860a6-271">Кредиторская задолженность</span><span class="sxs-lookup"><span data-stu-id="860a6-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-272">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="860a6-272">-1,008.00</span></span></td>
<td><span data-ttu-id="860a6-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="860a6-273">1,008.00</span></span></td>
<td><span data-ttu-id="860a6-274">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-275">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-276">6</span><span class="sxs-lookup"><span data-stu-id="860a6-276">6</span></span></td>
<td><span data-ttu-id="860a6-277">Актив ФПП</span><span class="sxs-lookup"><span data-stu-id="860a6-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-278">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="860a6-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="860a6-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-281">7</span><span class="sxs-lookup"><span data-stu-id="860a6-281">7</span></span></td>
<td><span data-ttu-id="860a6-282">Обязательство по финансовой аренде</span><span class="sxs-lookup"><span data-stu-id="860a6-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-283">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="860a6-284">-22,794.00</span></span></td>
<td><span data-ttu-id="860a6-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-285">1,000.00</span></span></td>
<td><span data-ttu-id="860a6-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="860a6-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="860a6-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-288">8</span><span class="sxs-lookup"><span data-stu-id="860a6-288">8</span></span></td>
<td><span data-ttu-id="860a6-289">Расходы на выплату процентов</span><span class="sxs-lookup"><span data-stu-id="860a6-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-290">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-291">94.97</span><span class="sxs-lookup"><span data-stu-id="860a6-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-292">94.97</span><span class="sxs-lookup"><span data-stu-id="860a6-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-293">9</span><span class="sxs-lookup"><span data-stu-id="860a6-293">9</span></span></td>
<td><span data-ttu-id="860a6-294">Касса</span><span class="sxs-lookup"><span data-stu-id="860a6-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-295">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="860a6-295">-1,008.00</span></span></td>
<td><span data-ttu-id="860a6-296">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="860a6-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-297">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="860a6-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-298">10</span><span class="sxs-lookup"><span data-stu-id="860a6-298">10</span></span></td>
<td><span data-ttu-id="860a6-299">Расходы на амортизацию</span><span class="sxs-lookup"><span data-stu-id="860a6-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-300">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-301">949.75</span><span class="sxs-lookup"><span data-stu-id="860a6-301">949.75</span></span></td>
<td><span data-ttu-id="860a6-302">949.75</span><span class="sxs-lookup"><span data-stu-id="860a6-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-303">11</span><span class="sxs-lookup"><span data-stu-id="860a6-303">11</span></span></td>
<td><span data-ttu-id="860a6-304">Накопленная амортизация</span><span class="sxs-lookup"><span data-stu-id="860a6-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-305">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="860a6-306">-949.75</span></span></td>
<td><span data-ttu-id="860a6-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="860a6-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="860a6-308">Как показано в предыдущей таблице, три книги требуются для обеспечения как регламентной отчетности, так и отчетности МСФО.</span><span class="sxs-lookup"><span data-stu-id="860a6-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="860a6-309">Регламентная книга записывает платеж по аренде в соответствии с правилами учета денежных средств в текущем слое.</span><span class="sxs-lookup"><span data-stu-id="860a6-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="860a6-310">В книге по регламентному сторнированию отменяются записи регламентного журнала.</span><span class="sxs-lookup"><span data-stu-id="860a6-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="860a6-311">Книга МСФО 16 создает записи журнала, которые необходимы в соответствии с МСФО 16.</span><span class="sxs-lookup"><span data-stu-id="860a6-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="860a6-312">Аренда должна быть введена только один раз.</span><span class="sxs-lookup"><span data-stu-id="860a6-312">You must enter a lease only one time.</span></span> <span data-ttu-id="860a6-313">Затем можно открыть страницу **Книги**, чтобы просмотреть все книги, связанные с арендой.</span><span class="sxs-lookup"><span data-stu-id="860a6-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="860a6-314">При создании книг все три из них должны быть связаны с одной и той же записью аренды.</span><span class="sxs-lookup"><span data-stu-id="860a6-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="860a6-315">Первая запись журнала записывает расходы на аренду в рамках регламентной книги.</span><span class="sxs-lookup"><span data-stu-id="860a6-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="860a6-316">Платежи можно создавать либо пакетом, либо путем выбора графика оплаты в регламентной книге.</span><span class="sxs-lookup"><span data-stu-id="860a6-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="860a6-317">В данном примере следующая запись журнала создается для регламентной книги из графика оплаты.</span><span class="sxs-lookup"><span data-stu-id="860a6-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="860a6-318">Арендный платеж — 31.01.2020 — JE 100</span><span class="sxs-lookup"><span data-stu-id="860a6-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="860a6-319">Тип счета</span><span class="sxs-lookup"><span data-stu-id="860a6-319">Account type</span></span> | <span data-ttu-id="860a6-320">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="860a6-320">Account number</span></span> | <span data-ttu-id="860a6-321">Слой</span><span class="sxs-lookup"><span data-stu-id="860a6-321">Layer</span></span>   | <span data-ttu-id="860a6-322">Описание счета</span><span class="sxs-lookup"><span data-stu-id="860a6-322">Account description</span></span> | <span data-ttu-id="860a6-323">по дебету</span><span class="sxs-lookup"><span data-stu-id="860a6-323">Debit</span></span>    | <span data-ttu-id="860a6-324">По кредиту</span><span class="sxs-lookup"><span data-stu-id="860a6-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="860a6-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-325">Ledger</span></span>       | <span data-ttu-id="860a6-326">1</span><span class="sxs-lookup"><span data-stu-id="860a6-326">1</span></span>              | <span data-ttu-id="860a6-327">Текущие</span><span class="sxs-lookup"><span data-stu-id="860a6-327">Current</span></span> | <span data-ttu-id="860a6-328">Расходы по аренде</span><span class="sxs-lookup"><span data-stu-id="860a6-328">Lease expense</span></span>       | <span data-ttu-id="860a6-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-329">1,000.00</span></span> |          |
| <span data-ttu-id="860a6-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-330">Ledger</span></span>       | <span data-ttu-id="860a6-331">4</span><span class="sxs-lookup"><span data-stu-id="860a6-331">4</span></span>              | <span data-ttu-id="860a6-332">Текущие</span><span class="sxs-lookup"><span data-stu-id="860a6-332">Current</span></span> | <span data-ttu-id="860a6-333">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="860a6-333">Clearing account</span></span>    |          | <span data-ttu-id="860a6-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-334">1,000.00</span></span> |

<span data-ttu-id="860a6-335">Служащий отдела расчетов с поставщиками использует стандартную функциональность Dynamics 365, чтобы создать накладную для оплаты за аренду за пределами модуля аренды актива.</span><span class="sxs-lookup"><span data-stu-id="860a6-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="860a6-336">Однако вместо того, чтобы выбирать **Расходы по аренде** в качестве дебетового счета, сотрудник отдела расчетов с поставщиками выбирает клиринговый счет для создания следующей записи.</span><span class="sxs-lookup"><span data-stu-id="860a6-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="860a6-337">Процесс AP — 31.01.2020 — JE 110</span><span class="sxs-lookup"><span data-stu-id="860a6-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="860a6-338">Тип счета</span><span class="sxs-lookup"><span data-stu-id="860a6-338">Account type</span></span> | <span data-ttu-id="860a6-339">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="860a6-339">Account number</span></span> | <span data-ttu-id="860a6-340">Слой</span><span class="sxs-lookup"><span data-stu-id="860a6-340">Layer</span></span>   | <span data-ttu-id="860a6-341">Описание счета</span><span class="sxs-lookup"><span data-stu-id="860a6-341">Account description</span></span> | <span data-ttu-id="860a6-342">по дебету</span><span class="sxs-lookup"><span data-stu-id="860a6-342">Debit</span></span>    | <span data-ttu-id="860a6-343">По кредиту</span><span class="sxs-lookup"><span data-stu-id="860a6-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="860a6-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-344">Ledger</span></span>       | <span data-ttu-id="860a6-345">4</span><span class="sxs-lookup"><span data-stu-id="860a6-345">4</span></span>              | <span data-ttu-id="860a6-346">Текущие</span><span class="sxs-lookup"><span data-stu-id="860a6-346">Current</span></span> | <span data-ttu-id="860a6-347">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="860a6-347">Clearing account</span></span>    | <span data-ttu-id="860a6-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-348">1,000.00</span></span> |          |
| <span data-ttu-id="860a6-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-349">Ledger</span></span>       | <span data-ttu-id="860a6-350">2</span><span class="sxs-lookup"><span data-stu-id="860a6-350">2</span></span>              | <span data-ttu-id="860a6-351">Текущие</span><span class="sxs-lookup"><span data-stu-id="860a6-351">Current</span></span> | <span data-ttu-id="860a6-352">Банковские сборы</span><span class="sxs-lookup"><span data-stu-id="860a6-352">Bank fee</span></span>            | <span data-ttu-id="860a6-353">3.00</span><span class="sxs-lookup"><span data-stu-id="860a6-353">3.00</span></span>     |          |
| <span data-ttu-id="860a6-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-354">Ledger</span></span>       | <span data-ttu-id="860a6-355">3</span><span class="sxs-lookup"><span data-stu-id="860a6-355">3</span></span>              | <span data-ttu-id="860a6-356">Текущие</span><span class="sxs-lookup"><span data-stu-id="860a6-356">Current</span></span> | <span data-ttu-id="860a6-357">Расходы на НДС</span><span class="sxs-lookup"><span data-stu-id="860a6-357">VAT expense</span></span>         | <span data-ttu-id="860a6-358">5.00</span><span class="sxs-lookup"><span data-stu-id="860a6-358">5.00</span></span>     |          |
| <span data-ttu-id="860a6-359">Поставщик</span><span class="sxs-lookup"><span data-stu-id="860a6-359">Vendor</span></span>       | <span data-ttu-id="860a6-360">5</span><span class="sxs-lookup"><span data-stu-id="860a6-360">5</span></span>              | <span data-ttu-id="860a6-361">Текущие</span><span class="sxs-lookup"><span data-stu-id="860a6-361">Current</span></span> | <span data-ttu-id="860a6-362">Кредиторская задолженность</span><span class="sxs-lookup"><span data-stu-id="860a6-362">Accounts payable</span></span>    |          | <span data-ttu-id="860a6-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="860a6-363">1,008.00</span></span> |

<span data-ttu-id="860a6-364">Когда отчет выдается поставщику, вы следуете обычному процессу оплаты.</span><span class="sxs-lookup"><span data-stu-id="860a6-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="860a6-365">В ходе этого процесса создается следующая запись журнала.</span><span class="sxs-lookup"><span data-stu-id="860a6-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="860a6-366">Оплата наличными — 31.01.2020 — JE 120</span><span class="sxs-lookup"><span data-stu-id="860a6-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="860a6-367">Тип счета</span><span class="sxs-lookup"><span data-stu-id="860a6-367">Account type</span></span> | <span data-ttu-id="860a6-368">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="860a6-368">Account number</span></span> | <span data-ttu-id="860a6-369">Слой</span><span class="sxs-lookup"><span data-stu-id="860a6-369">Layer</span></span>   | <span data-ttu-id="860a6-370">Описание счета</span><span class="sxs-lookup"><span data-stu-id="860a6-370">Account description</span></span> | <span data-ttu-id="860a6-371">по дебету</span><span class="sxs-lookup"><span data-stu-id="860a6-371">Debit</span></span>    | <span data-ttu-id="860a6-372">По кредиту</span><span class="sxs-lookup"><span data-stu-id="860a6-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="860a6-373">Поставщик</span><span class="sxs-lookup"><span data-stu-id="860a6-373">Vendor</span></span>       | <span data-ttu-id="860a6-374">5</span><span class="sxs-lookup"><span data-stu-id="860a6-374">5</span></span>              | <span data-ttu-id="860a6-375">Текущие</span><span class="sxs-lookup"><span data-stu-id="860a6-375">Current</span></span> | <span data-ttu-id="860a6-376">Расчеты с поставщиками</span><span class="sxs-lookup"><span data-stu-id="860a6-376">Accounts Payable</span></span>    | <span data-ttu-id="860a6-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="860a6-377">1,008.00</span></span> |          |
| <span data-ttu-id="860a6-378">Денежные средства</span><span class="sxs-lookup"><span data-stu-id="860a6-378">Bank</span></span>         | <span data-ttu-id="860a6-379">9</span><span class="sxs-lookup"><span data-stu-id="860a6-379">9</span></span>              | <span data-ttu-id="860a6-380">Текущие</span><span class="sxs-lookup"><span data-stu-id="860a6-380">Current</span></span> | <span data-ttu-id="860a6-381">Касса</span><span class="sxs-lookup"><span data-stu-id="860a6-381">Cash</span></span>                |          | <span data-ttu-id="860a6-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="860a6-382">1,008.00</span></span> |

<span data-ttu-id="860a6-383">В этот момент вы полностью выполнили учет этой аренды в соответствии с регламентными требованиями к отчетности и можете создать пробный баланс с помощью текущего слоя.</span><span class="sxs-lookup"><span data-stu-id="860a6-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="860a6-384">Система возвращает пробный баланс со следующими показателями.</span><span class="sxs-lookup"><span data-stu-id="860a6-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="860a6-385">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="860a6-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="860a6-386">описание</span><span class="sxs-lookup"><span data-stu-id="860a6-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="860a6-387">Регламентная книга (текущий слой)</span><span class="sxs-lookup"><span data-stu-id="860a6-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="860a6-388">Текущий слой, итого</span><span class="sxs-lookup"><span data-stu-id="860a6-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="860a6-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="860a6-389">JE-100</span></span></th>
<th><span data-ttu-id="860a6-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="860a6-390">JE-110</span></span></th>
<th><span data-ttu-id="860a6-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="860a6-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="860a6-392">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="860a6-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="860a6-393">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="860a6-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="860a6-394">ДБ (КР)</span><span class="sxs-lookup"><span data-stu-id="860a6-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="860a6-395">1</span><span class="sxs-lookup"><span data-stu-id="860a6-395">1</span></span></td>
<td><span data-ttu-id="860a6-396">Расходы по аренде</span><span class="sxs-lookup"><span data-stu-id="860a6-396">Lease expense</span></span></td>
<td><span data-ttu-id="860a6-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-399">2</span><span class="sxs-lookup"><span data-stu-id="860a6-399">2</span></span></td>
<td><span data-ttu-id="860a6-400">Банковские сборы</span><span class="sxs-lookup"><span data-stu-id="860a6-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-401">3.00</span><span class="sxs-lookup"><span data-stu-id="860a6-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-402">3.00</span><span class="sxs-lookup"><span data-stu-id="860a6-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-403">3</span><span class="sxs-lookup"><span data-stu-id="860a6-403">3</span></span></td>
<td><span data-ttu-id="860a6-404">Расходы на НДС</span><span class="sxs-lookup"><span data-stu-id="860a6-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-405">5.00</span><span class="sxs-lookup"><span data-stu-id="860a6-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-406">5.00</span><span class="sxs-lookup"><span data-stu-id="860a6-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-407">4</span><span class="sxs-lookup"><span data-stu-id="860a6-407">4</span></span></td>
<td><span data-ttu-id="860a6-408">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="860a6-408">Clearing account</span></span></td>
<td><span data-ttu-id="860a6-409">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="860a6-409">-1,000.00</span></span></td>
<td><span data-ttu-id="860a6-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-411">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-412">5</span><span class="sxs-lookup"><span data-stu-id="860a6-412">5</span></span></td>
<td><span data-ttu-id="860a6-413">Кредиторская задолженность</span><span class="sxs-lookup"><span data-stu-id="860a6-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="860a6-414">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="860a6-414">-1,008.00</span></span></td>
<td><span data-ttu-id="860a6-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="860a6-415">1,008.00</span></span></td>
<td><span data-ttu-id="860a6-416">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-417">6</span><span class="sxs-lookup"><span data-stu-id="860a6-417">6</span></span></td>
<td><span data-ttu-id="860a6-418">Актив ФПП</span><span class="sxs-lookup"><span data-stu-id="860a6-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-419">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-420">7</span><span class="sxs-lookup"><span data-stu-id="860a6-420">7</span></span></td>
<td><span data-ttu-id="860a6-421">Обязательство по финансовой аренде</span><span class="sxs-lookup"><span data-stu-id="860a6-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-422">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-423">8</span><span class="sxs-lookup"><span data-stu-id="860a6-423">8</span></span></td>
<td><span data-ttu-id="860a6-424">Расходы на выплату процентов</span><span class="sxs-lookup"><span data-stu-id="860a6-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-425">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-426">9</span><span class="sxs-lookup"><span data-stu-id="860a6-426">9</span></span></td>
<td><span data-ttu-id="860a6-427">Касса</span><span class="sxs-lookup"><span data-stu-id="860a6-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-428">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="860a6-428">-1,008.00</span></span></td>
<td><span data-ttu-id="860a6-429">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="860a6-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-430">10</span><span class="sxs-lookup"><span data-stu-id="860a6-430">10</span></span></td>
<td><span data-ttu-id="860a6-431">Расходы на амортизацию</span><span class="sxs-lookup"><span data-stu-id="860a6-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-432">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="860a6-433">11</span><span class="sxs-lookup"><span data-stu-id="860a6-433">11</span></span></td>
<td><span data-ttu-id="860a6-434">Накопленная амортизация</span><span class="sxs-lookup"><span data-stu-id="860a6-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="860a6-435">0.00</span><span class="sxs-lookup"><span data-stu-id="860a6-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="860a6-436">Если вы хотите использовать цифры МСФО 16 для запуска того же пробного баланса, записи журнала регламентного учета должны быть реверсированы, а записи журнала МСФО 16 должны быть разнесены.</span><span class="sxs-lookup"><span data-stu-id="860a6-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="860a6-437">Для реверсирования записей регламентного журнала этот пример включает регламентную книгу сторнирования с той же настройкой, что и у регламентной книги, но с противоположным профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="860a6-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="860a6-438">Например, регламентная книга *дебетовала* на счет расходов на аренду, но книга сторнирования будет *кредитовать* этот счет.</span><span class="sxs-lookup"><span data-stu-id="860a6-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="860a6-439">Эти связи легко определить в счетах разноски аренды активов на странице **Параметры аренды активов** (**Аренда активов \> Настройка \> Параметры аренды активов**).</span><span class="sxs-lookup"><span data-stu-id="860a6-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="860a6-440">При использовании того же процесса, который использовался для регламентной книги, используется для книги сторнирования, будет создана следующая запись журнала.</span><span class="sxs-lookup"><span data-stu-id="860a6-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="860a6-441">Разница заключается в том, что книга сторнирования резервирует записи сторнирования из регламентной книги.</span><span class="sxs-lookup"><span data-stu-id="860a6-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="860a6-442">Операции сторнирования также выполняются в пользовательском слое.</span><span class="sxs-lookup"><span data-stu-id="860a6-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="860a6-443">Когда пробный баланс запускается на текущем слое, операции журнала сторнирования не включаются.</span><span class="sxs-lookup"><span data-stu-id="860a6-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="860a6-444">Арендный платеж — 31.01.2020 — JE 130</span><span class="sxs-lookup"><span data-stu-id="860a6-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="860a6-445">Тип счета</span><span class="sxs-lookup"><span data-stu-id="860a6-445">Account type</span></span> | <span data-ttu-id="860a6-446">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="860a6-446">Account number</span></span> | <span data-ttu-id="860a6-447">Слой</span><span class="sxs-lookup"><span data-stu-id="860a6-447">Layer</span></span>  | <span data-ttu-id="860a6-448">Описание счета</span><span class="sxs-lookup"><span data-stu-id="860a6-448">Account description</span></span> | <span data-ttu-id="860a6-449">по дебету</span><span class="sxs-lookup"><span data-stu-id="860a6-449">Debit</span></span>    | <span data-ttu-id="860a6-450">По кредиту</span><span class="sxs-lookup"><span data-stu-id="860a6-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="860a6-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-451">Ledger</span></span>       | <span data-ttu-id="860a6-452">4</span><span class="sxs-lookup"><span data-stu-id="860a6-452">4</span></span>              | <span data-ttu-id="860a6-453">Произвольная</span><span class="sxs-lookup"><span data-stu-id="860a6-453">Custom</span></span> | <span data-ttu-id="860a6-454">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="860a6-454">Clearing account</span></span>    | <span data-ttu-id="860a6-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-455">1,000.00</span></span> |          |
| <span data-ttu-id="860a6-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-456">Ledger</span></span>       | <span data-ttu-id="860a6-457">1</span><span class="sxs-lookup"><span data-stu-id="860a6-457">1</span></span>              | <span data-ttu-id="860a6-458">Произвольная</span><span class="sxs-lookup"><span data-stu-id="860a6-458">Custom</span></span> | <span data-ttu-id="860a6-459">Расходы по аренде</span><span class="sxs-lookup"><span data-stu-id="860a6-459">Lease expense</span></span>       |          | <span data-ttu-id="860a6-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-460">1,000.00</span></span> |

<span data-ttu-id="860a6-461">После того, как записи регламентного журнала удалены, будут учтены все записи журнала, необходимые для МСФО 16 в книге МСФО 16.</span><span class="sxs-lookup"><span data-stu-id="860a6-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="860a6-462">Эти записи включают первоначальное признание актива ФПП и его обязательства, а также запись процента и амортизации.</span><span class="sxs-lookup"><span data-stu-id="860a6-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="860a6-463">Первоначальное признание — 01.01.2020 — JE 140</span><span class="sxs-lookup"><span data-stu-id="860a6-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="860a6-464">Тип счета</span><span class="sxs-lookup"><span data-stu-id="860a6-464">Account type</span></span> | <span data-ttu-id="860a6-465">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="860a6-465">Account number</span></span> | <span data-ttu-id="860a6-466">Слой</span><span class="sxs-lookup"><span data-stu-id="860a6-466">Layer</span></span>  | <span data-ttu-id="860a6-467">Описание счета</span><span class="sxs-lookup"><span data-stu-id="860a6-467">Account description</span></span>      | <span data-ttu-id="860a6-468">по дебету</span><span class="sxs-lookup"><span data-stu-id="860a6-468">Debit</span></span>     | <span data-ttu-id="860a6-469">По кредиту</span><span class="sxs-lookup"><span data-stu-id="860a6-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="860a6-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-470">Ledger</span></span>       | <span data-ttu-id="860a6-471">6</span><span class="sxs-lookup"><span data-stu-id="860a6-471">6</span></span>              | <span data-ttu-id="860a6-472">Произвольная</span><span class="sxs-lookup"><span data-stu-id="860a6-472">Custom</span></span> | <span data-ttu-id="860a6-473">Актив ФПП</span><span class="sxs-lookup"><span data-stu-id="860a6-473">ROU Asset</span></span>                | <span data-ttu-id="860a6-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="860a6-474">22,793.90</span></span> |           |
| <span data-ttu-id="860a6-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-475">Ledger</span></span>       | <span data-ttu-id="860a6-476">7</span><span class="sxs-lookup"><span data-stu-id="860a6-476">7</span></span>              | <span data-ttu-id="860a6-477">Произвольная</span><span class="sxs-lookup"><span data-stu-id="860a6-477">Custom</span></span> | <span data-ttu-id="860a6-478">Обязательство по финансовой аренде</span><span class="sxs-lookup"><span data-stu-id="860a6-478">Finance lease obligation</span></span> |           | <span data-ttu-id="860a6-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="860a6-479">22,793.90</span></span> |

<span data-ttu-id="860a6-480">Арендный платеж разносится как другие платежи по аренде.</span><span class="sxs-lookup"><span data-stu-id="860a6-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="860a6-481">Причиной использования клирингового счета является обеспечение того, что наличные деньги кредитуются только один раз.</span><span class="sxs-lookup"><span data-stu-id="860a6-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="860a6-482">Арендный платеж — 31.01.2020 — JE 150</span><span class="sxs-lookup"><span data-stu-id="860a6-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="860a6-483">Тип счета</span><span class="sxs-lookup"><span data-stu-id="860a6-483">Account type</span></span> | <span data-ttu-id="860a6-484">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="860a6-484">Account number</span></span> | <span data-ttu-id="860a6-485">Слой</span><span class="sxs-lookup"><span data-stu-id="860a6-485">Layer</span></span>  | <span data-ttu-id="860a6-486">Описание счета</span><span class="sxs-lookup"><span data-stu-id="860a6-486">Account description</span></span>      | <span data-ttu-id="860a6-487">по дебету</span><span class="sxs-lookup"><span data-stu-id="860a6-487">Debit</span></span>    | <span data-ttu-id="860a6-488">По кредиту</span><span class="sxs-lookup"><span data-stu-id="860a6-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="860a6-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-489">Ledger</span></span>       | <span data-ttu-id="860a6-490">7</span><span class="sxs-lookup"><span data-stu-id="860a6-490">7</span></span>              | <span data-ttu-id="860a6-491">Произвольная</span><span class="sxs-lookup"><span data-stu-id="860a6-491">Custom</span></span> | <span data-ttu-id="860a6-492">Обязательство по финансовой аренде</span><span class="sxs-lookup"><span data-stu-id="860a6-492">Finance lease obligation</span></span> | <span data-ttu-id="860a6-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-493">1,000.00</span></span> |          |
| <span data-ttu-id="860a6-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-494">Ledger</span></span>       | <span data-ttu-id="860a6-495">4</span><span class="sxs-lookup"><span data-stu-id="860a6-495">4</span></span>              | <span data-ttu-id="860a6-496">Произвольная</span><span class="sxs-lookup"><span data-stu-id="860a6-496">Custom</span></span> | <span data-ttu-id="860a6-497">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="860a6-497">Clearing account</span></span>         |          | <span data-ttu-id="860a6-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="860a6-498">1,000.00</span></span> |

<span data-ttu-id="860a6-499">Запись журнала расходов по процентам создается на основе графика амортизации обязательств.</span><span class="sxs-lookup"><span data-stu-id="860a6-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="860a6-500">Расходы на выплату процентов — 31.01.2020 — JE 160</span><span class="sxs-lookup"><span data-stu-id="860a6-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="860a6-501">Тип счета</span><span class="sxs-lookup"><span data-stu-id="860a6-501">Account type</span></span> | <span data-ttu-id="860a6-502">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="860a6-502">Account number</span></span> | <span data-ttu-id="860a6-503">Слой</span><span class="sxs-lookup"><span data-stu-id="860a6-503">Layer</span></span>  | <span data-ttu-id="860a6-504">Описание счета</span><span class="sxs-lookup"><span data-stu-id="860a6-504">Account description</span></span>      | <span data-ttu-id="860a6-505">по дебету</span><span class="sxs-lookup"><span data-stu-id="860a6-505">Debit</span></span> | <span data-ttu-id="860a6-506">По кредиту</span><span class="sxs-lookup"><span data-stu-id="860a6-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="860a6-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-507">Ledger</span></span>       | <span data-ttu-id="860a6-508">8</span><span class="sxs-lookup"><span data-stu-id="860a6-508">8</span></span>              | <span data-ttu-id="860a6-509">Произвольная</span><span class="sxs-lookup"><span data-stu-id="860a6-509">Custom</span></span> | <span data-ttu-id="860a6-510">Расходы на выплату процентов</span><span class="sxs-lookup"><span data-stu-id="860a6-510">Interest expense</span></span>         | <span data-ttu-id="860a6-511">94.97</span><span class="sxs-lookup"><span data-stu-id="860a6-511">94.97</span></span> |        |
| <span data-ttu-id="860a6-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-512">Ledger</span></span>       | <span data-ttu-id="860a6-513">7</span><span class="sxs-lookup"><span data-stu-id="860a6-513">7</span></span>              | <span data-ttu-id="860a6-514">Произвольная</span><span class="sxs-lookup"><span data-stu-id="860a6-514">Custom</span></span> | <span data-ttu-id="860a6-515">Обязательство по финансовой аренде</span><span class="sxs-lookup"><span data-stu-id="860a6-515">Finance lease obligation</span></span> |       | <span data-ttu-id="860a6-516">94.97</span><span class="sxs-lookup"><span data-stu-id="860a6-516">94.97</span></span>  |

<span data-ttu-id="860a6-517">Запись журнала расходов по амортизации создается на основе графика амортизации активов.</span><span class="sxs-lookup"><span data-stu-id="860a6-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="860a6-518">Амортизационные расходы — 31.01.2020 — JE 170</span><span class="sxs-lookup"><span data-stu-id="860a6-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="860a6-519">Тип счета</span><span class="sxs-lookup"><span data-stu-id="860a6-519">Account type</span></span> | <span data-ttu-id="860a6-520">Расчетный счет</span><span class="sxs-lookup"><span data-stu-id="860a6-520">Account number</span></span> | <span data-ttu-id="860a6-521">Слой</span><span class="sxs-lookup"><span data-stu-id="860a6-521">Layer</span></span>  | <span data-ttu-id="860a6-522">Описание счета</span><span class="sxs-lookup"><span data-stu-id="860a6-522">Account description</span></span>      | <span data-ttu-id="860a6-523">по дебету</span><span class="sxs-lookup"><span data-stu-id="860a6-523">Debit</span></span>  | <span data-ttu-id="860a6-524">По кредиту</span><span class="sxs-lookup"><span data-stu-id="860a6-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="860a6-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-525">Ledger</span></span>       | <span data-ttu-id="860a6-526">10</span><span class="sxs-lookup"><span data-stu-id="860a6-526">10</span></span>             | <span data-ttu-id="860a6-527">Произвольная</span><span class="sxs-lookup"><span data-stu-id="860a6-527">Custom</span></span> | <span data-ttu-id="860a6-528">Расходы на амортизацию</span><span class="sxs-lookup"><span data-stu-id="860a6-528">Depreciation expense</span></span>     | <span data-ttu-id="860a6-529">949.75</span><span class="sxs-lookup"><span data-stu-id="860a6-529">949.75</span></span> |        |
| <span data-ttu-id="860a6-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="860a6-530">Ledger</span></span>       | <span data-ttu-id="860a6-531">11</span><span class="sxs-lookup"><span data-stu-id="860a6-531">11</span></span>             | <span data-ttu-id="860a6-532">Произвольная</span><span class="sxs-lookup"><span data-stu-id="860a6-532">Custom</span></span> | <span data-ttu-id="860a6-533">Накопленная амортизация</span><span class="sxs-lookup"><span data-stu-id="860a6-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="860a6-534">949.75</span><span class="sxs-lookup"><span data-stu-id="860a6-534">949.75</span></span> |

<span data-ttu-id="860a6-535">После создания и разноски всех этих записей журнала будут отображены следующие значения "пользовательского слоя 1".</span><span class="sxs-lookup"><span data-stu-id="860a6-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="860a6-536">Обратите внимание, что последний столбец включает банковские сборы, расход на налог на добавленную стоимость (НДС) и сокращение наличности из предыдущего слоя, но не включает записи журнала регламентной отчетности.</span><span class="sxs-lookup"><span data-stu-id="860a6-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="860a6-537">Таким образом, вы достигли истинных возможностей двойной отчетности.</span><span class="sxs-lookup"><span data-stu-id="860a6-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="860a6-538">На этом этапе компании просто требуется выполнить свой пробный баланс и объединить текущий слой и пользовательский слой для создания пробного баланса МСФО.</span><span class="sxs-lookup"><span data-stu-id="860a6-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="860a6-539">Номер счета</span><span class="sxs-lookup"><span data-stu-id="860a6-539">Account No</span></span> | <span data-ttu-id="860a6-540">описание</span><span class="sxs-lookup"><span data-stu-id="860a6-540">Description</span></span>              | <span data-ttu-id="860a6-541">Регламентная книга\-Текущий слой\-JE\-100\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="860a6-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="860a6-542">Регламентная книга\-Текущий слой\-JE\-110\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="860a6-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="860a6-543">Регламентная книга\-Текущий слой\-JE\-120\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="860a6-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="860a6-544">Текущий слой \- Итого</span><span class="sxs-lookup"><span data-stu-id="860a6-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="860a6-545">Книга сторнирования\-Пользовательский слой\-JE\-130\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="860a6-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="860a6-546">Книга МСФО 16\-Пользовательский слой\-JE\-140\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="860a6-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="860a6-547">Книга МСФО 16\-Пользовательский слой\-JE\-150\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="860a6-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="860a6-548">Книга МСФО 16\-Пользовательский слой\-JE\-160\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="860a6-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="860a6-549">Книга МСФО 16\-Пользовательский слой\-JE\-170\-ДБ \(КР\)</span><span class="sxs-lookup"><span data-stu-id="860a6-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="860a6-550">Текущий слой \+ Текущий слой \- Итого</span><span class="sxs-lookup"><span data-stu-id="860a6-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="860a6-551">1</span><span class="sxs-lookup"><span data-stu-id="860a6-551">1</span></span>          | <span data-ttu-id="860a6-552">Расходы по аренде</span><span class="sxs-lookup"><span data-stu-id="860a6-552">Lease expense</span></span>            | <span data-ttu-id="860a6-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="860a6-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-554">1,000\.00</span></span>               |   | <span data-ttu-id="860a6-555">\-1 000</span><span class="sxs-lookup"><span data-stu-id="860a6-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="860a6-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-556">0\.00</span></span>                                   |
| <span data-ttu-id="860a6-557">2</span><span class="sxs-lookup"><span data-stu-id="860a6-557">2</span></span>          | <span data-ttu-id="860a6-558">Банковские сборы</span><span class="sxs-lookup"><span data-stu-id="860a6-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="860a6-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="860a6-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="860a6-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-561">3\.00</span></span>                                   |
| <span data-ttu-id="860a6-562">3</span><span class="sxs-lookup"><span data-stu-id="860a6-562">3</span></span>          | <span data-ttu-id="860a6-563">Расходы на НДС</span><span class="sxs-lookup"><span data-stu-id="860a6-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="860a6-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="860a6-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="860a6-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-566">5\.00</span></span>                                   |
| <span data-ttu-id="860a6-567">4</span><span class="sxs-lookup"><span data-stu-id="860a6-567">4</span></span>          | <span data-ttu-id="860a6-568">Клиринговый счет</span><span class="sxs-lookup"><span data-stu-id="860a6-568">Clearing account</span></span>         | <span data-ttu-id="860a6-569">\-1 000\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="860a6-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="860a6-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-571">0\.00</span></span>                   |   | <span data-ttu-id="860a6-572">1000</span><span class="sxs-lookup"><span data-stu-id="860a6-572">1,000</span></span>                                           |                                                | <span data-ttu-id="860a6-573">\-1 000</span><span class="sxs-lookup"><span data-stu-id="860a6-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="860a6-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-574">0\.00</span></span>                                   |
| <span data-ttu-id="860a6-575">5</span><span class="sxs-lookup"><span data-stu-id="860a6-575">5</span></span>          | <span data-ttu-id="860a6-576">Кредиторская задолженность</span><span class="sxs-lookup"><span data-stu-id="860a6-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="860a6-577">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="860a6-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-578">1,008\.00</span></span>                                         | <span data-ttu-id="860a6-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="860a6-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-580">0\.00</span></span>                                   |
| <span data-ttu-id="860a6-581">6</span><span class="sxs-lookup"><span data-stu-id="860a6-581">6</span></span>          | <span data-ttu-id="860a6-582">Актив ФПП</span><span class="sxs-lookup"><span data-stu-id="860a6-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="860a6-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="860a6-584">22,794</span><span class="sxs-lookup"><span data-stu-id="860a6-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="860a6-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="860a6-585">22,793\.90</span></span>                              |
| <span data-ttu-id="860a6-586">7</span><span class="sxs-lookup"><span data-stu-id="860a6-586">7</span></span>          | <span data-ttu-id="860a6-587">Обязательство по финансовой аренде</span><span class="sxs-lookup"><span data-stu-id="860a6-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="860a6-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="860a6-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="860a6-589">\-22,794</span></span>                                       | <span data-ttu-id="860a6-590">1000</span><span class="sxs-lookup"><span data-stu-id="860a6-590">1,000</span></span>                                          | <span data-ttu-id="860a6-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="860a6-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="860a6-592">\-21 888\.87</span><span class="sxs-lookup"><span data-stu-id="860a6-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="860a6-593">8</span><span class="sxs-lookup"><span data-stu-id="860a6-593">8</span></span>          | <span data-ttu-id="860a6-594">Расходы на выплату процентов</span><span class="sxs-lookup"><span data-stu-id="860a6-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="860a6-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="860a6-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="860a6-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="860a6-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="860a6-597">94\.97</span></span>                                  |
| <span data-ttu-id="860a6-598">9</span><span class="sxs-lookup"><span data-stu-id="860a6-598">9</span></span>          | <span data-ttu-id="860a6-599">Касса</span><span class="sxs-lookup"><span data-stu-id="860a6-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="860a6-600">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="860a6-601">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="860a6-602">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="860a6-603">10</span><span class="sxs-lookup"><span data-stu-id="860a6-603">10</span></span>         | <span data-ttu-id="860a6-604">Расходы на амортизацию</span><span class="sxs-lookup"><span data-stu-id="860a6-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="860a6-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="860a6-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="860a6-606">949\.75</span></span>                                        | <span data-ttu-id="860a6-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="860a6-607">949\.75</span></span>                                 |
| <span data-ttu-id="860a6-608">11</span><span class="sxs-lookup"><span data-stu-id="860a6-608">11</span></span>         | <span data-ttu-id="860a6-609">Накопленная амортизация</span><span class="sxs-lookup"><span data-stu-id="860a6-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="860a6-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="860a6-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="860a6-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="860a6-611">\-949\.75</span></span>                                      | <span data-ttu-id="860a6-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="860a6-612">\-949\.75</span></span>                               |


