---
title: Расчет накладных TDS с использованием формы заказа на покупку и формы заказа на продажу
description: В этой теме перечислены шаги для расчета налога, удержанного в источнике (TDS), по различным типам накладных.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023528"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="a1513-103">Расчет накладных TDS с использованием формы заказа на покупку и формы заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="a1513-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1513-104">В этом разделе перечисляются шаги для расчета налога, удержанного в источнике (TDS), по различным типам накладных с помощью страниц **Заказ на покупку**, **Журнал покупок**, **Контракт** и **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="a1513-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="a1513-105">Создайте заказ на покупку, журнал покупок, контракт на покупку или заказ на продажу, используя указанную страницу.</span><span class="sxs-lookup"><span data-stu-id="a1513-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="a1513-106">Введите требуемую информацию.</span><span class="sxs-lookup"><span data-stu-id="a1513-106">Enter the required details.</span></span>

2. <span data-ttu-id="a1513-107">Перейдите на вкладку **Настройка**, чтобы просмотреть суть налогоплательщика поставщика или клиента.</span><span class="sxs-lookup"><span data-stu-id="a1513-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="a1513-108">Эта информация перечислена в поле **Суть налогоплательщика** в группе полей **Группа подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="a1513-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="a1513-109">В поле **Группа TDS** просмотрите или измените группу TDS по умолчанию, определенную для поставщика или клиента.</span><span class="sxs-lookup"><span data-stu-id="a1513-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a1513-110">Поле **Группа TCS** недоступно, если в поле **Группа TDS** выбрана группа TDS.</span><span class="sxs-lookup"><span data-stu-id="a1513-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="a1513-111">TDS вычисляется только в том случае, если установлен флажок **Рассчитать подоходный налог** для поставщика или клиента на странице **Все поставщики** или **Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="a1513-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="a1513-112">Создайте строки номенклатур на вкладке **Строки** и введите требуемые сведения.</span><span class="sxs-lookup"><span data-stu-id="a1513-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="a1513-113">Перейдите на вкладку **Настройка** (уровень строки), чтобы просмотреть или изменить группу TDS, определенную на уровне заголовка.</span><span class="sxs-lookup"><span data-stu-id="a1513-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="a1513-114">Группа TDS отображается в поле **Группа TDS**, которое находится в группе полей **Группа подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="a1513-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="a1513-115">Перейдите на вкладку **Информация по налогам** и выберите альтернативные адреса, которые настроены для названия компании, которое отображается в этом поле.</span><span class="sxs-lookup"><span data-stu-id="a1513-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="a1513-116">Название компании отображается в поле **Имя**, которое находится в группе полей **Данные о компании**.</span><span class="sxs-lookup"><span data-stu-id="a1513-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="a1513-117">TAN для выбранного названия компании отображается в поле **Номера счета налога** (**TAN**) в группе полей **Подоходный налог**.</span><span class="sxs-lookup"><span data-stu-id="a1513-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="a1513-118">Выберите **Подоходный налог**, чтобы открыть страницу **Временные проводки по подоходному налогу**.</span><span class="sxs-lookup"><span data-stu-id="a1513-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="a1513-119">Просмотрите следующие поля в верхней области страницы **Временные проводки по подоходному налогу**.</span><span class="sxs-lookup"><span data-stu-id="a1513-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="a1513-120">**Итоговая** **сумма** **подоходного** **налога** **—** итог TDS, рассчитанный для проводки для группы TDS.</span><span class="sxs-lookup"><span data-stu-id="a1513-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="a1513-121">**Значение** — итоговое процентное значение, используемое для расчета TDS для проводки.</span><span class="sxs-lookup"><span data-stu-id="a1513-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="a1513-122">Итоговое процентное значение основано на формуле, которая определена для кодов налогов TDS, прикрепленных к группе TDS.</span><span class="sxs-lookup"><span data-stu-id="a1513-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="a1513-123">**Скорректированная итоговая сумма подоходного налога** — итоговая скорректированная сумма TDS для всех налоговых кодов в группе TDS.</span><span class="sxs-lookup"><span data-stu-id="a1513-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="a1513-124">**TDS** — если выбрано, группа TDS присоединена к проводке.</span><span class="sxs-lookup"><span data-stu-id="a1513-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="a1513-125">В полях на вкладках **Обзор**, **Общее** и **Корректировка** на странице **Временные проводки по подоходному налогу** отображается рассчитанная сумма TDS и скорректированная сумма TDS для каждого налогового кода TDS, связанного с группой TDS.</span><span class="sxs-lookup"><span data-stu-id="a1513-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="a1513-126">Выберите **Порог**, чтобы открыть страницу **Порог**.</span><span class="sxs-lookup"><span data-stu-id="a1513-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="a1513-127">Просмотр лимита порога, определенного для компонента налогов TDS, присоединенных к конкретному налоговому коду TDS на данной странице.</span><span class="sxs-lookup"><span data-stu-id="a1513-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="a1513-128">Выберите **Конструктор формул**, чтобы открыть форму страницу **Конструктор формул**.</span><span class="sxs-lookup"><span data-stu-id="a1513-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="a1513-129">Просмотр формулы, которая определена для конкретного налогового кода TDS на данной странице.</span><span class="sxs-lookup"><span data-stu-id="a1513-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="a1513-130">Разноска накладной.</span><span class="sxs-lookup"><span data-stu-id="a1513-130">Post the invoice.</span></span> <span data-ttu-id="a1513-131">Сумма TDS, рассчитанная в накладных по покупке, разносится на счет расчетов с поставщиками, а сумма TDS, рассчитанная в накладных на продажу, разносится на счет, который определен для каждого налогового кода TDS в группе TDS.</span><span class="sxs-lookup"><span data-stu-id="a1513-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="a1513-132">Счета расчетов с поставщиками или счета дебиторской задолженности для налоговых кодов TDS определяются на странице **Коды подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="a1513-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="a1513-133">Нажмите кнопку **Запрос** **> Накладная > Разнесенный подоходный налог**, чтобы открыть страницу **Проводки подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="a1513-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="a1513-134">Общее процентное значение, используемое для расчета TDS для проводки, можно просмотреть в поле **Значение**.</span><span class="sxs-lookup"><span data-stu-id="a1513-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="a1513-135">В полях на вкладках **Обзор**, **Общее** и **Сумма** на странице **Проводки по подоходному налогу** содержат сведения о TDS, рассчитанном для проводки.</span><span class="sxs-lookup"><span data-stu-id="a1513-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="a1513-136">Просмотрите информацию о расчете TDS для каждого налогового кода TDS, связанного с группой TDS.</span><span class="sxs-lookup"><span data-stu-id="a1513-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
