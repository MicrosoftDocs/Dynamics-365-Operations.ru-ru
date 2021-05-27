---
title: Расчет TDS по накладным на странице накладной с произвольным текстом
description: В этой теме объясняется, как рассчитать налог, удерживаемый в источнике (TDS), по накладным, используя страницу накладной с произвольным текстом.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023544"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="f549e-103">Расчет TDS по накладным на странице накладной с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="f549e-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f549e-104">В этой теме объясняется, как рассчитать налог, удерживаемый в источнике (TDS), по накладным, используя страницу **Накладная с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="f549e-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="f549e-105">Перейдите в раздел **Расчеты с клиентами \> Накладные \> Все накладные с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="f549e-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="f549e-106">[![Страница накладной с произвольным текстом](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="f549e-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="f549e-107">Выберите **Создать**, чтобы создать накладную с произвольным текстом, затем введите требуемые сведения.</span><span class="sxs-lookup"><span data-stu-id="f549e-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="f549e-108">Выберите вкладку **Накладная**. В разделе **Группа подоходного налога** в поле **Суть налогоплательщика** показана суть категории налогоплательщика для клиента.</span><span class="sxs-lookup"><span data-stu-id="f549e-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="f549e-109">В поле **Группа TDS** просмотрите или измените группу TDS по умолчанию, определенную для клиента.</span><span class="sxs-lookup"><span data-stu-id="f549e-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f549e-110">Когда выбрано значение в поле **Группа TDS**, поле **Группа TKS** становится недоступным.</span><span class="sxs-lookup"><span data-stu-id="f549e-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="f549e-111">TDS вычисляется только в том случае, если установлен параметр **Рассчитать подоходный налог** задан как **Да** для клиента на странице **Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="f549e-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="f549e-112">На вкладке **Сведения о налоге** в разделе **Данные о компании** в поле **Имя** выберите название компании для альтернативного адреса, который был настроен для компании.</span><span class="sxs-lookup"><span data-stu-id="f549e-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="f549e-113">В разделе **Подоходный налог** в поле **Номер налогового счета (TAN)** отображается номер налогового счета (TAN) для выбранной компании.</span><span class="sxs-lookup"><span data-stu-id="f549e-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="f549e-114">На вкладке **Строки накладной** создайте строки накладной и введите требуемые сведения.</span><span class="sxs-lookup"><span data-stu-id="f549e-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="f549e-115">В разделе **Группа подоходного налога** в поле **Номер налогового счета (TAN)** отображается значение TAN, а в поле **Группа TDS** отображается группа TDS.</span><span class="sxs-lookup"><span data-stu-id="f549e-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="f549e-116">Выберите **Подоходный налог**, чтобы открыть страницу **Временные проводки по подоходному налогу**.</span><span class="sxs-lookup"><span data-stu-id="f549e-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="f549e-117">Верхняя часть страницы содержит следующие поля:</span><span class="sxs-lookup"><span data-stu-id="f549e-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="f549e-118">**Итоговая сумма подоходного налога** — итог TDS, рассчитанный для проводки для группы TDS.</span><span class="sxs-lookup"><span data-stu-id="f549e-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="f549e-119">**Значение** — итоговое процентное значение, используемое для расчета TDS для проводки.</span><span class="sxs-lookup"><span data-stu-id="f549e-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="f549e-120">Итоговое процентное значение основано на формуле, которая определена для кодов налогов TDS, прикрепленных к группе TDS.</span><span class="sxs-lookup"><span data-stu-id="f549e-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="f549e-121">**Скорректированная итоговая сумма подоходного налога** — итоговая скорректированная сумма TDS для всех налоговых кодов в группе TDS.</span><span class="sxs-lookup"><span data-stu-id="f549e-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="f549e-122">**TDS** — установленный флажок указывает на то, что с проводкой связана группа TDS.</span><span class="sxs-lookup"><span data-stu-id="f549e-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="f549e-123">В полях на вкладках **Обзор**, **Общее** и **Корректировка** отображается рассчитанная сумма TDS и сведения по скорректированной сумме TDS для каждого налогового кода TDS, связанного с группой TDS.</span><span class="sxs-lookup"><span data-stu-id="f549e-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="f549e-124">Выберите **Порог**, чтобы открыть страницу **Порог**, на которой можно просмотреть лимит порога, который определен для компонента налога TDS, присоединенного к конкретному налоговому коду TDS.</span><span class="sxs-lookup"><span data-stu-id="f549e-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="f549e-125">Выберите **Конструктор формул**, чтобы открыть страницу **Конструктор формул**, на которой можно просмотреть формулу, которая определена для конкретного налогового кода TDS.</span><span class="sxs-lookup"><span data-stu-id="f549e-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="f549e-126">Разнесите накладную с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="f549e-126">Post the free text invoice.</span></span> <span data-ttu-id="f549e-127">Сумма TDS, рассчитанная для накладных с произвольным текстом, разносится на счет дебиторской задолженности, определенный для каждого налогового кода TDS в группе TDS.</span><span class="sxs-lookup"><span data-stu-id="f549e-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="f549e-128">Счета расчетов с клиентами для налоговых кодов TDS определяются на странице **Коды подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="f549e-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="f549e-129">Выберите **Разнесенный подоходный налог**, чтобы открыть страницу **Проводки по подоходному налогу**.</span><span class="sxs-lookup"><span data-stu-id="f549e-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="f549e-130">В поле **Значение** содержится итоговое процентное значение, используемое для расчета TDS для проводки.</span><span class="sxs-lookup"><span data-stu-id="f549e-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="f549e-131">В полях на вкладках **Обзор**, **Общие** и **Сумма** показаны суммы TDS, рассчитанные по строкам накладной.</span><span class="sxs-lookup"><span data-stu-id="f549e-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="f549e-132">Просмотрите информацию о расчете TDS для каждого налогового кода TDS, связанного с группой TDS.</span><span class="sxs-lookup"><span data-stu-id="f549e-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
