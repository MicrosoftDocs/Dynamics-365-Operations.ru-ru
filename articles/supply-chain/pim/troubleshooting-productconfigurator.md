---
title: Устранение неполадок конфигуратора продуктов
description: В этом разделе описывается устранение проблем, которые могут встретиться при работе с конфигуратором продуктов.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 77d0c21fbb5a8479ca5e7bdb759c1373b6b255a4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841559"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="3adec-103">Устранение неполадок конфигуратора продуктов</span><span class="sxs-lookup"><span data-stu-id="3adec-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="3adec-104">В этом разделе описывается устранение проблем, которые могут встретиться при работе с конфигуратором продуктов.</span><span class="sxs-lookup"><span data-stu-id="3adec-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="3adec-105">Текст номенклатуры перезаписывается при настройке продукта в строке заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="3adec-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3adec-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="3adec-106">Issue description</span></span>

<span data-ttu-id="3adec-107">Эта проблема возникает при создании строки заказа на продажу для настраиваемой номенклатуры и последующем изменении текста номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3adec-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="3adec-108">При настройке номенклатуры и последующем выборе **ОК** текст переписывается стандартным текстом.</span><span class="sxs-lookup"><span data-stu-id="3adec-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3adec-109">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="3adec-109">Issue resolution</span></span>

<span data-ttu-id="3adec-110">Это поведение является ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="3adec-110">This behavior is expected.</span></span> <span data-ttu-id="3adec-111">Текстовое поле включает имя варианта, которое заполняется только после настройки строки.</span><span class="sxs-lookup"><span data-stu-id="3adec-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="3adec-112">Поэтому необходимо изменить текст после того, как вы настроили строку, но не ранее.</span><span class="sxs-lookup"><span data-stu-id="3adec-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="3adec-113">Целочисленные атрибуты неправильно округляются при расчете моделей конфигурации продуктов.</span><span class="sxs-lookup"><span data-stu-id="3adec-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3adec-114">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="3adec-114">Issue description</span></span>

<span data-ttu-id="3adec-115">Эта проблема может возникнуть при выполнении следующей последовательности действий:</span><span class="sxs-lookup"><span data-stu-id="3adec-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="3adec-116">Настройте следующие атрибуты в модели конфигурации производства:</span><span class="sxs-lookup"><span data-stu-id="3adec-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="3adec-117">Ввод (целое число)</span><span class="sxs-lookup"><span data-stu-id="3adec-117">Input (integer)</span></span>
    - <span data-ttu-id="3adec-118">Процент (десятичное число)</span><span class="sxs-lookup"><span data-stu-id="3adec-118">Percent (decimal)</span></span>
    - <span data-ttu-id="3adec-119">Результат (целое число)</span><span class="sxs-lookup"><span data-stu-id="3adec-119">Result (integer)</span></span>

2. <span data-ttu-id="3adec-120">Создайте расчет со следующим выражением:</span><span class="sxs-lookup"><span data-stu-id="3adec-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="3adec-121">*Результат* = *Ввод* × *Процент* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="3adec-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="3adec-122">В этом случае целочисленный результат не всегда правильно округляется.</span><span class="sxs-lookup"><span data-stu-id="3adec-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="3adec-123">Например, введено значение 1 000, а процентное значение — 2,40.</span><span class="sxs-lookup"><span data-stu-id="3adec-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="3adec-124">Таким образом, ожидается, что целочисленное значение равно 24, поскольку 2,40 процента от 1 000 равно 24 (или 24,00 в десятичном формате).</span><span class="sxs-lookup"><span data-stu-id="3adec-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="3adec-125">Вместо этого результат отображается как 23.</span><span class="sxs-lookup"><span data-stu-id="3adec-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="3adec-126">Однако если процент равен 2,39, вычисление округляется до 24 вместо 23.</span><span class="sxs-lookup"><span data-stu-id="3adec-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="3adec-127">Если процент равен 2,50, вычисление округляется до 25, как и ожидается.</span><span class="sxs-lookup"><span data-stu-id="3adec-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3adec-128">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="3adec-128">Issue resolution</span></span>

<span data-ttu-id="3adec-129">Эта проблема возникает из-за того, что внутри Microsoft Solver Foundation числа представляются с использованием дробей.</span><span class="sxs-lookup"><span data-stu-id="3adec-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="3adec-130">В предыдущем примере результат вычисления с процентом 2,40 представляется как 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375.</span><span class="sxs-lookup"><span data-stu-id="3adec-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="3adec-131">Когда платформа .NET приводит это значение к целому числу, она возвращает 23.</span><span class="sxs-lookup"><span data-stu-id="3adec-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="3adec-132">Это поведение не будет изменено, так как от него зависят другие сценарии.</span><span class="sxs-lookup"><span data-stu-id="3adec-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="3adec-133">В предыдущем примере можно устранить проблему, введя дополнительный десятичный атрибут и расчет.</span><span class="sxs-lookup"><span data-stu-id="3adec-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="3adec-134">Например, можно настроить следующие атрибуты в модели конфигурации производства:</span><span class="sxs-lookup"><span data-stu-id="3adec-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="3adec-135">Ввод (целое число)</span><span class="sxs-lookup"><span data-stu-id="3adec-135">Input (integer)</span></span>
- <span data-ttu-id="3adec-136">Процент (десятичное число)</span><span class="sxs-lookup"><span data-stu-id="3adec-136">Percent (decimal)</span></span>
- <span data-ttu-id="3adec-137">ResultDecimal (десятичное число)</span><span class="sxs-lookup"><span data-stu-id="3adec-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="3adec-138">ResultInteger (целое число)</span><span class="sxs-lookup"><span data-stu-id="3adec-138">ResultInteger (integer)</span></span>

<span data-ttu-id="3adec-139">Можно затем добавить следующие расчеты:</span><span class="sxs-lookup"><span data-stu-id="3adec-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="3adec-140">*ResultDecimal* = *Ввод* × *Процент* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="3adec-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="3adec-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="3adec-141">*ResultInteger* = *ResultDecimal*</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]