---
title: Настройка периодов сопоставления подоходного налога для налогов типа TDS
description: В этой теме объясняется, как настроить периоды сопоставления для периодов сопоставления по налогу, который удерживается в источнике (TDS).
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023525"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="72180-103">Настройка периодов сопоставления подоходного налога для налогов типа TDS</span><span class="sxs-lookup"><span data-stu-id="72180-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72180-104">В этой теме объясняется, как настроить периоды сопоставления для периодов сопоставления по налогу, который удерживается в источнике (TDS).</span><span class="sxs-lookup"><span data-stu-id="72180-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="72180-105">Перейдите в раздел **Налог \> Косвенные налоги \> Подоходный налог \> Периоды сопоставления подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="72180-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="72180-106">[![Страница периодов сопоставления подоходного налога](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="72180-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="72180-107">В поле **Тип налога** выберите **TDS**, чтобы настроить периоды сопоставления подоходного налога для типа налога TDS.</span><span class="sxs-lookup"><span data-stu-id="72180-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="72180-108">Выберите **Создать**, чтобы создать строку.</span><span class="sxs-lookup"><span data-stu-id="72180-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="72180-109">В поле **Период сопоставления** введите имя периода сопоставления TDS.</span><span class="sxs-lookup"><span data-stu-id="72180-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="72180-110">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="72180-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="72180-111">В поле **Налоговый орган по подоходному налогу** выберите орган TDS, для которого определяется период сопоставления TDS.</span><span class="sxs-lookup"><span data-stu-id="72180-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="72180-112">На экспресс-вкладке **Общие** в поле **Интервал периода** выберите тип интервала периода для периода сопоставления TDS.</span><span class="sxs-lookup"><span data-stu-id="72180-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="72180-113">В поле **Число единиц** укажите число единиц измерения для типа интервала периодов.</span><span class="sxs-lookup"><span data-stu-id="72180-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="72180-114">На экспресс-вкладке **Периоды** в поле **Начальная дата** выберите начальную дату для периода сопоставления TDS.</span><span class="sxs-lookup"><span data-stu-id="72180-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="72180-115">В поле **Конечная дата** выберите дату окончания.</span><span class="sxs-lookup"><span data-stu-id="72180-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="72180-116">Чтобы создать последующий период сопоставления TDS для существующего периода на основе интервала периода и единиц периода, выберите **Создать период**.</span><span class="sxs-lookup"><span data-stu-id="72180-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="72180-117">Для просмотра подробных сведений о периодическом выполнении сопоставления TDS, который запускается для определенного периода сопоставления, выберите **Платежи подоходного налога**, чтобы открыть страницу **Платеж по подоходному налогу**.</span><span class="sxs-lookup"><span data-stu-id="72180-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72180-118">Чтобы выполнить периодическое сопоставление TDS, перейдите **Главная книга \> Периодически \> Подоходный налог \> Платеж подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="72180-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="72180-119">[![Страница платежа подоходного налога](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="72180-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="72180-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="72180-120">Close the page.</span></span>
