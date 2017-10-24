---
title: "Номерные серии"
description: "Номерные серии используются для создания четких уникальных кодов для записей справочника и записей проводок, для которых требуются коды."
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bd1f4d383848e6205d64be160da4c529adeaccf2
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="number-sequences"></a><span data-ttu-id="f8052-103">Номерные серии</span><span class="sxs-lookup"><span data-stu-id="f8052-103">Number sequences</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f8052-104">Номерные серии используются для создания четких уникальных кодов для записей справочника и записей проводок, для которых требуются коды.</span><span class="sxs-lookup"><span data-stu-id="f8052-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="f8052-105">Запись основных данных или запись проводки, для которой требуется идентификатор, называется *образцом*.</span><span class="sxs-lookup"><span data-stu-id="f8052-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="f8052-106">Перед созданием новых записей для ссылки необходимо настроить номерную серию и связать ее со ссылкой.</span><span class="sxs-lookup"><span data-stu-id="f8052-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="f8052-107">Рекомендуется использовать страницы в **Управление организацией** для настройки номерных серий.</span><span class="sxs-lookup"><span data-stu-id="f8052-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="f8052-108">Если для модуля требуются особые параметры, можно использовать страницу параметров модуля, чтобы задать номерные серии для ссылок в этом модуле.</span><span class="sxs-lookup"><span data-stu-id="f8052-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="f8052-109">Например, в **Расчеты с клиентами** и **Расчеты с поставщиками** можно настроить группы номерных серий для распределения номерных серий по конкретным клиентам или поставщикам.</span><span class="sxs-lookup"><span data-stu-id="f8052-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span> 

<span data-ttu-id="f8052-110">При настройке номерной серии необходимо указать область, которая определяет, какая организация использует номерную серию.</span><span class="sxs-lookup"><span data-stu-id="f8052-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="f8052-111">Область может быть **Общая**, **Компания**, **Юридическое лицо** или **Операционная единица**.</span><span class="sxs-lookup"><span data-stu-id="f8052-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="f8052-112">Области **юридического лица** и **компании** также можно объединять с **Периодом финансового календаря** для создания еще более конкретных номерных серий.</span><span class="sxs-lookup"><span data-stu-id="f8052-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span> 

<span data-ttu-id="f8052-113">Форматы номерной серии состоят из сегментов.</span><span class="sxs-lookup"><span data-stu-id="f8052-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="f8052-114">Номерные серии с областью, отличной от **Общая**, могут содержать сегментов, которые соответствуют области.</span><span class="sxs-lookup"><span data-stu-id="f8052-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="f8052-115">Например, номерная серия с областью **Юридическое лицо** может содержать сегмент юридического лица.</span><span class="sxs-lookup"><span data-stu-id="f8052-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="f8052-116">Путем включения сегмента области в формат номерной серии можно определить область определенной записи, посмотрев на ее номер.</span><span class="sxs-lookup"><span data-stu-id="f8052-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span> 

<span data-ttu-id="f8052-117">В дополнение к сегментам, соответствующим областям, форматы номерной серии могут содержать сегменты **Константа** и **Буквенно-цифровые сегменты**.</span><span class="sxs-lookup"><span data-stu-id="f8052-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="f8052-118">Сегмент **Константа** содержит набор букв, цифр или символов, которые не изменяются.</span><span class="sxs-lookup"><span data-stu-id="f8052-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="f8052-119">Сегмент **Буквенно-цифровой** содержит набор букв или цифр, которые пошагово изменяются при каждом использовании номера.</span><span class="sxs-lookup"><span data-stu-id="f8052-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="f8052-120">Используйте знак решетки (\#), чтобы представлять пошаговые номера, и амперсанд (&), чтобы представлять пошаговые буквы.</span><span class="sxs-lookup"><span data-stu-id="f8052-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="f8052-121">Например, формат \#\#\#\#\#\_2017 создает последовательность 00001\_2017, 00002\_2017 и т. д.</span><span class="sxs-lookup"><span data-stu-id="f8052-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

<a name="number-sequence-examples"></a><span data-ttu-id="f8052-122">Примеры номерной серии</span><span class="sxs-lookup"><span data-stu-id="f8052-122">Number sequence examples</span></span>
------------------------

<span data-ttu-id="f8052-123">Следующие примеры иллюстрируют использование сегментов для создания форматов номерной серии.</span><span class="sxs-lookup"><span data-stu-id="f8052-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="f8052-124">В частности, примеры демонстрируют результаты использования сегментов области.</span><span class="sxs-lookup"><span data-stu-id="f8052-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="f8052-125">Номера отчетов по расходам</span><span class="sxs-lookup"><span data-stu-id="f8052-125">Expense report numbers</span></span>

<span data-ttu-id="f8052-126">В следующем примере показана настройка номеров отчета по расходам для юридического лица с заголовком **CS**.</span><span class="sxs-lookup"><span data-stu-id="f8052-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span> 

- <span data-ttu-id="f8052-127">**Область:** Командировки и расходы</span><span class="sxs-lookup"><span data-stu-id="f8052-127">**Area:** Travel and expense</span></span> 
- <span data-ttu-id="f8052-128">**Ссылка:** Номер отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="f8052-128">**Reference:** Expense report number</span></span> 
- <span data-ttu-id="f8052-129">**Область действия:** Юридическое лицо</span><span class="sxs-lookup"><span data-stu-id="f8052-129">**Scope:** Legal entity</span></span> 
- <span data-ttu-id="f8052-130">**Юридическое лицо:** CS</span><span class="sxs-lookup"><span data-stu-id="f8052-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="f8052-131">Сегменты</span><span class="sxs-lookup"><span data-stu-id="f8052-131">Segments</span></span>  | <span data-ttu-id="f8052-132">Тип сегмента</span><span class="sxs-lookup"><span data-stu-id="f8052-132">Segment type</span></span> | <span data-ttu-id="f8052-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f8052-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="f8052-134">Сегмент 1</span><span class="sxs-lookup"><span data-stu-id="f8052-134">Segment 1</span></span> | <span data-ttu-id="f8052-135">Информация о компании</span><span class="sxs-lookup"><span data-stu-id="f8052-135">Legal entity</span></span> | <span data-ttu-id="f8052-136">CS</span><span class="sxs-lookup"><span data-stu-id="f8052-136">CS</span></span>        |
| <span data-ttu-id="f8052-137">Сегмент 2</span><span class="sxs-lookup"><span data-stu-id="f8052-137">Segment 2</span></span> | <span data-ttu-id="f8052-138">Константа</span><span class="sxs-lookup"><span data-stu-id="f8052-138">Constant</span></span>     | <span data-ttu-id="f8052-139">-РАСХОД-</span><span class="sxs-lookup"><span data-stu-id="f8052-139">-EXPENSE-</span></span> |
| <span data-ttu-id="f8052-140">Сегмент 3</span><span class="sxs-lookup"><span data-stu-id="f8052-140">Segment 3</span></span> | <span data-ttu-id="f8052-141">Буквенно-цифровой</span><span class="sxs-lookup"><span data-stu-id="f8052-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="f8052-142">**Пример форматированного номера**: CS-EXPENSE-0039</span><span class="sxs-lookup"><span data-stu-id="f8052-142">**Example of formatted number**: CS-EXPENSE-0039</span></span> 

<span data-ttu-id="f8052-143">Можно настроить сходный формат номерной серии для других юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="f8052-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="f8052-144">Например, если для юридического лица с именем **RW** изменяется только значение сегмента юридического лица, форматированный номер выглядит как RW-EXPENSE-0039.</span><span class="sxs-lookup"><span data-stu-id="f8052-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="f8052-145">Можно также изменить весь формат номерной серии для других юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="f8052-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="f8052-146">Например, можно пропустить сегмент области юридического лица для создания форматированное номера, например Exp-0001.</span><span class="sxs-lookup"><span data-stu-id="f8052-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="f8052-147">Номера заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="f8052-147">Sales order numbers</span></span>

<span data-ttu-id="f8052-148">В следующем примере показана настройка номеров заказа на продажу для кода компании **CEU**.</span><span class="sxs-lookup"><span data-stu-id="f8052-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span> 

- <span data-ttu-id="f8052-149">**Область:** Продажи</span><span class="sxs-lookup"><span data-stu-id="f8052-149">**Area:** Sales</span></span> 
- <span data-ttu-id="f8052-150">**Ссылка:** Заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="f8052-150">**Reference:** Sales order</span></span> 
- <span data-ttu-id="f8052-151">**Область действия:** Компания</span><span class="sxs-lookup"><span data-stu-id="f8052-151">**Scope:** Company</span></span> 
- <span data-ttu-id="f8052-152">**Компания:** CEU</span><span class="sxs-lookup"><span data-stu-id="f8052-152">**Company:** CEU</span></span>

| <span data-ttu-id="f8052-153">Сегменты</span><span class="sxs-lookup"><span data-stu-id="f8052-153">Segments</span></span>  | <span data-ttu-id="f8052-154">Тип сегмента</span><span class="sxs-lookup"><span data-stu-id="f8052-154">Segment type</span></span> | <span data-ttu-id="f8052-155">Стоимость</span><span class="sxs-lookup"><span data-stu-id="f8052-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="f8052-156">Сегмент 1</span><span class="sxs-lookup"><span data-stu-id="f8052-156">Segment 1</span></span> | <span data-ttu-id="f8052-157">Константа</span><span class="sxs-lookup"><span data-stu-id="f8052-157">Constant</span></span>     | <span data-ttu-id="f8052-158">SO-</span><span class="sxs-lookup"><span data-stu-id="f8052-158">SO-</span></span>      |
| <span data-ttu-id="f8052-159">Сегмент 2</span><span class="sxs-lookup"><span data-stu-id="f8052-159">Segment 2</span></span> | <span data-ttu-id="f8052-160">Буквенно-цифровой</span><span class="sxs-lookup"><span data-stu-id="f8052-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="f8052-161">**Пример форматированного номера**: SO-0029</span><span class="sxs-lookup"><span data-stu-id="f8052-161">**Example of formatted number**: SO-0029</span></span> 

<span data-ttu-id="f8052-162">Даже если сегмент области не включен в формат, нумерация продолжается для каждого кода компании</span><span class="sxs-lookup"><span data-stu-id="f8052-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="f8052-163">При использовании одного формата для всех кодов компании в каждой компании используется одни и те же номера.</span><span class="sxs-lookup"><span data-stu-id="f8052-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="f8052-164">Например, номер заказа на продажу SO-0029 используется в каждой компании.</span><span class="sxs-lookup"><span data-stu-id="f8052-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="f8052-165">Можно также изменить весь формат номерной серии для других кодов компании.</span><span class="sxs-lookup"><span data-stu-id="f8052-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="f8052-166">Номера заявки на покупку</span><span class="sxs-lookup"><span data-stu-id="f8052-166">Purchase requisition numbers</span></span>

<span data-ttu-id="f8052-167">В следующем примере показаны номера заявок на покупку на уровне организации.</span><span class="sxs-lookup"><span data-stu-id="f8052-167">In the following example, purchase requisition numbers are organization-wide.</span></span> 

- <span data-ttu-id="f8052-168">**Область:** Покупка</span><span class="sxs-lookup"><span data-stu-id="f8052-168">**Area:** Purchase</span></span> 
- <span data-ttu-id="f8052-169">**Ссылка:** Заявка на покупку</span><span class="sxs-lookup"><span data-stu-id="f8052-169">**Reference:** Purchase requisition</span></span> 
- <span data-ttu-id="f8052-170">**Область действия:** Общая</span><span class="sxs-lookup"><span data-stu-id="f8052-170">**Scope:** Shared</span></span>

| <span data-ttu-id="f8052-171">Сегменты</span><span class="sxs-lookup"><span data-stu-id="f8052-171">Segments</span></span>  | <span data-ttu-id="f8052-172">Тип сегмента</span><span class="sxs-lookup"><span data-stu-id="f8052-172">Segment type</span></span> | <span data-ttu-id="f8052-173">Стоимость</span><span class="sxs-lookup"><span data-stu-id="f8052-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="f8052-174">Сегмент 1</span><span class="sxs-lookup"><span data-stu-id="f8052-174">Segment 1</span></span> | <span data-ttu-id="f8052-175">Константа</span><span class="sxs-lookup"><span data-stu-id="f8052-175">Constant</span></span>     | <span data-ttu-id="f8052-176">Треб.</span><span class="sxs-lookup"><span data-stu-id="f8052-176">Req</span></span>      |
| <span data-ttu-id="f8052-177">Сегмент 2</span><span class="sxs-lookup"><span data-stu-id="f8052-177">Segment 2</span></span> | <span data-ttu-id="f8052-178">Буквенно-цифровой</span><span class="sxs-lookup"><span data-stu-id="f8052-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="f8052-179">**Пример форматированного номера**: Req0052</span><span class="sxs-lookup"><span data-stu-id="f8052-179">**Example of formatted number**: Req0052</span></span> 

<span data-ttu-id="f8052-180">Поскольку область действия — **Общая**, формат номерной серии используется во всей организации.</span><span class="sxs-lookup"><span data-stu-id="f8052-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="f8052-181">Нельзя настроить разные форматы номерной серии для разных частей организации.</span><span class="sxs-lookup"><span data-stu-id="f8052-181">You cannot set up different number sequence formats for different parts of the organization.</span></span> 

<a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="f8052-182">Анализ производительности для номерных серий</span><span class="sxs-lookup"><span data-stu-id="f8052-182">Performance considerations for number sequences</span></span>
-----------------------------------------------

<span data-ttu-id="f8052-183">Рассмотрим следующую информацию о том, как конфигурация номерных серий может повлиять на производительность системы до начала настройки номерных серий.</span><span class="sxs-lookup"><span data-stu-id="f8052-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="f8052-184">Непрерывные и прерывистые номерные серии</span><span class="sxs-lookup"><span data-stu-id="f8052-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="f8052-185">Номерные серии могут быть непрерывными или прерывистыми.</span><span class="sxs-lookup"><span data-stu-id="f8052-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="f8052-186">Непрерывная номерная серия не пропускает номера, и при этом нельзя использовать последовательные номера.</span><span class="sxs-lookup"><span data-stu-id="f8052-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="f8052-187">Номера из прерывистой номерной серии используются последовательно, однако номерная серия может пропускать номера.</span><span class="sxs-lookup"><span data-stu-id="f8052-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="f8052-188">Например, если пользователь отменяет проводку, номер создается, но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8052-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="f8052-189">В непрерывной номерной серии этот номер обрабатывается позднее.</span><span class="sxs-lookup"><span data-stu-id="f8052-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="f8052-190">В прерывистой номерной серии номер не используется.</span><span class="sxs-lookup"><span data-stu-id="f8052-190">In a non-continuous number sequence, the number is not used.</span></span> 

<span data-ttu-id="f8052-191">Непрерывные номерные серии обычно необходимы для внешних документов, таких как заказы на покупку, заказы на продажу и накладные.</span><span class="sxs-lookup"><span data-stu-id="f8052-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="f8052-192">Однако непрерывные номерные серии могут неблагоприятно повлиять на время отклика системы, так как система должна запрашивать номер из базы данных при каждом создании нового документа или записи.</span><span class="sxs-lookup"><span data-stu-id="f8052-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span> 

<span data-ttu-id="f8052-193">При использовании прерывистой номерной серии можно включить **Предварительное выделение** на экспресс-вкладке **Производительность** страницы **Номерные серии**.</span><span class="sxs-lookup"><span data-stu-id="f8052-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="f8052-194">При указании количества номеров для предварительного выделения система выбирает данные номера и сохраняет их в памяти.</span><span class="sxs-lookup"><span data-stu-id="f8052-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="f8052-195">Новые номера поступают из базы данных только после использования предварительно выделенного количества.</span><span class="sxs-lookup"><span data-stu-id="f8052-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span> 

<span data-ttu-id="f8052-196">При отсутствии нормативного требования по использованию номерных серий рекомендуется использовать прерывистые номерные серии для лучшей производительности системы.</span><span class="sxs-lookup"><span data-stu-id="f8052-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="f8052-197">Автоматическая очистка номерных серий</span><span class="sxs-lookup"><span data-stu-id="f8052-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="f8052-198">В случае сбоя питания, ошибки приложения или другого непредвиденного сбоя система не может автоматически обрабатывать номера из непрерывных номерных серий.</span><span class="sxs-lookup"><span data-stu-id="f8052-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="f8052-199">Можно запустить процесс очистки вручную или автоматически восстановить потерянные номера.</span><span class="sxs-lookup"><span data-stu-id="f8052-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span> 

<span data-ttu-id="f8052-200">При планировании процесса очистки необходимо тщательно изучить ситуацию с серверами.</span><span class="sxs-lookup"><span data-stu-id="f8052-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="f8052-201">Очистку рекомендуется выполнять как пакетное задание в нерабочее время.</span><span class="sxs-lookup"><span data-stu-id="f8052-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>





