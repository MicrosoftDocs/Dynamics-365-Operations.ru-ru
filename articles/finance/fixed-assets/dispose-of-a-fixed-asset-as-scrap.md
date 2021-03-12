---
title: Списание основного средства в утиль
description: В разделе описывается процесс удаления проводок для основного средства, которое было списано в утиль.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 4dee4468079a9ad500f513900cec090acf6026ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969136"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="a413e-103">Списание основного средства в утиль</span><span class="sxs-lookup"><span data-stu-id="a413e-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a413e-104">В разделе описывается процесс удаления проводок для основного средства, которое было списано в утиль.</span><span class="sxs-lookup"><span data-stu-id="a413e-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="a413e-105">Типы проводок, которые могут быть удалены, включают в себя проводки приобретения и накопленной амортизации основного средства, а также другие проводки с основными средствами.</span><span class="sxs-lookup"><span data-stu-id="a413e-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="a413e-106">Удаление этих проводок влияет на счета балансового отчета, такие как счета корректировки ввода в эксплуатацию, корректировки амортизации, переоценки, повышения стоимости и понижения стоимости.</span><span class="sxs-lookup"><span data-stu-id="a413e-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="a413e-107">Проводка</span><span class="sxs-lookup"><span data-stu-id="a413e-107">Transaction</span></span>                                         | <span data-ttu-id="a413e-108">Дебет (Дб.)</span><span class="sxs-lookup"><span data-stu-id="a413e-108">Debit (Dr.)</span></span> | <span data-ttu-id="a413e-109">Кредит (Кр.)</span><span class="sxs-lookup"><span data-stu-id="a413e-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="a413e-110">Дб. Накопленная амортизация</span><span class="sxs-lookup"><span data-stu-id="a413e-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="a413e-111">Х</span><span class="sxs-lookup"><span data-stu-id="a413e-111">X</span></span>           |              |
| <span data-ttu-id="a413e-112">Кр. Прибыли/убытки по ОС</span><span class="sxs-lookup"><span data-stu-id="a413e-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="a413e-113">Х</span><span class="sxs-lookup"><span data-stu-id="a413e-113">X</span></span>            |
| <span data-ttu-id="a413e-114">Дб. Прибыли/убытки по ОС</span><span class="sxs-lookup"><span data-stu-id="a413e-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="a413e-115">Х</span><span class="sxs-lookup"><span data-stu-id="a413e-115">X</span></span>           |              |
| <span data-ttu-id="a413e-116">Кр. Счет приобретения ОС</span><span class="sxs-lookup"><span data-stu-id="a413e-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="a413e-117">Х</span><span class="sxs-lookup"><span data-stu-id="a413e-117">X</span></span>            |
| <span data-ttu-id="a413e-118">Дб. Прибыли/убытки по ОС (остаточная стоимость \[NBV\])</span><span class="sxs-lookup"><span data-stu-id="a413e-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="a413e-119">Х</span><span class="sxs-lookup"><span data-stu-id="a413e-119">X</span></span>           |              |
| <span data-ttu-id="a413e-120">Кр. Прибыли/убытки по ОС (остаточная стоимость)</span><span class="sxs-lookup"><span data-stu-id="a413e-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="a413e-121">Х</span><span class="sxs-lookup"><span data-stu-id="a413e-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="a413e-122">Рекомендуется тесно работать с финансовым директором компании или с контроллером, чтобы определить правильные счета, которые должны использоваться для каждого типа проводок, а также проверить, что процесс выбытия и созданные им проводки правильно обновляют эти счета.</span><span class="sxs-lookup"><span data-stu-id="a413e-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="a413e-123">Перед списанием ОС в утиль необходимо создать счета учета, связанные со стоимостью приобретения актива, амортизацией за текущий год, амортизацией за прошлый годы и остаточной стоимостью актива.</span><span class="sxs-lookup"><span data-stu-id="a413e-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="a413e-124">Типы проводок с основными средствами перечисляются на странице **Профиль разноски основных средств**.</span><span class="sxs-lookup"><span data-stu-id="a413e-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="a413e-125">Перейдите в раздел **Основные средства \> Настройка \> Профили разноски по ОС**, затем на экспресс-вкладке **Выбытие** выберите **Отходы** в поле над сеткой.</span><span class="sxs-lookup"><span data-stu-id="a413e-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="a413e-126">На следующем рисунке показан список типов проводок с основными средствами на странице **Профили разноски по ОС**.</span><span class="sxs-lookup"><span data-stu-id="a413e-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="a413e-127">[![Списание актива в утиль, рис. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="a413e-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="a413e-128">В следующем примере основное средство было приобретено 1 января 2018 г. и будет списано в утиль 31 марта 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a413e-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="a413e-129">**Цена приобретения:** 24 000,00 долларов США (USD)</span><span class="sxs-lookup"><span data-stu-id="a413e-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="a413e-130">**Срок службы:** два года</span><span class="sxs-lookup"><span data-stu-id="a413e-130">**Service life:** Two years</span></span>
- <span data-ttu-id="a413e-131">**Метод амортизации:** срок службы (прямолинейный метод)</span><span class="sxs-lookup"><span data-stu-id="a413e-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="a413e-132">**Сумма амортизации:** 1 000,00 долларов США в месяц</span><span class="sxs-lookup"><span data-stu-id="a413e-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="a413e-133">Остаточная стоимость основного средства рассчитывается по следующей формуле:</span><span class="sxs-lookup"><span data-stu-id="a413e-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="a413e-134">Остаточная стоимость = Цена приобретения – Амортизация</span><span class="sxs-lookup"><span data-stu-id="a413e-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="a413e-135">В этом примере основное средство было приобретено и амортизировалось в течение 15 месяцев, с января 2018 г, по март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a413e-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="a413e-136">Таким образом, остаточная стоимость актива равна 9 000,00 долларов США (24 000,00 – 15 000,00 долларов США).</span><span class="sxs-lookup"><span data-stu-id="a413e-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="a413e-137">[![Пример амортизации основного средства](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="a413e-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="a413e-138">Для создания журнала выбытия перейдите в раздел **Основные средства \> Записи журнала \> Журнал "Основные средства"**, затем на панели операций выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="a413e-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="a413e-139">Выберите **Выбытие - демонтаж**, затем выберите код ОС.</span><span class="sxs-lookup"><span data-stu-id="a413e-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="a413e-140">Для полного выбытия актива не вводите никакие значения в поле **Дебет** или **Кредит**.</span><span class="sxs-lookup"><span data-stu-id="a413e-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="a413e-141">[![Журнал "Основные средства"](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="a413e-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="a413e-142">Проводка по списанию в утиль основного средства изменяет значения полей журнала основных средств следующими способами:</span><span class="sxs-lookup"><span data-stu-id="a413e-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="a413e-143">В разделе **Сальдо** значение поля **Статус** изменяется на **Списано**.</span><span class="sxs-lookup"><span data-stu-id="a413e-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="a413e-144">В разделе **Расход** в поле **Дата выбытия** устанавливается дата, когда актив был списан в утиль.</span><span class="sxs-lookup"><span data-stu-id="a413e-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="a413e-145">[![Сведения из журнала ОС](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="a413e-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="a413e-146">На следующем рисунке показано сальдо основного средства.</span><span class="sxs-lookup"><span data-stu-id="a413e-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="a413e-147">[![Сальдо основного средства](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="a413e-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="a413e-148">На следующем рисунке показан разнесенный ваучер.</span><span class="sxs-lookup"><span data-stu-id="a413e-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="a413e-149">[![Остаточная стоимость](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="a413e-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>
