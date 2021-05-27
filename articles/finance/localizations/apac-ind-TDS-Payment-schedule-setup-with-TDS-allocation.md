---
title: Настройка графиков оплаты с распределением TDS
description: В этой теме объясняется, как настроить графики оплаты с распределением налогов, которые удерживаются в источнике (TDS).
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023546"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="8a222-103">Настройка графиков оплаты с распределением TDS</span><span class="sxs-lookup"><span data-stu-id="8a222-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a222-104">В этой теме объясняется, как настроить графики оплаты с распределением налогов, которые удерживаются в источнике (TDS).</span><span class="sxs-lookup"><span data-stu-id="8a222-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="8a222-105">Перейдите в раздел **Расчеты с поставщиками \> Настройка платежей \> Графики платежей**.</span><span class="sxs-lookup"><span data-stu-id="8a222-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="8a222-106">[![Страница графиков оплаты](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="8a222-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="8a222-107">В области действий выберите **Создать**, чтобы создать график оплаты, и введите требуемые сведения.</span><span class="sxs-lookup"><span data-stu-id="8a222-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="8a222-108">В поле **Распределение** выберите способ, который будет использоваться для распределения оплаты для графика оплаты:</span><span class="sxs-lookup"><span data-stu-id="8a222-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="8a222-109">Итоговый</span><span class="sxs-lookup"><span data-stu-id="8a222-109">Total</span></span>
    - <span data-ttu-id="8a222-110">Фиксированная сумма</span><span class="sxs-lookup"><span data-stu-id="8a222-110">Fixed amount</span></span>
    - <span data-ttu-id="8a222-111">Фиксированное количество</span><span class="sxs-lookup"><span data-stu-id="8a222-111">Fixed quantity</span></span>
    - <span data-ttu-id="8a222-112">Задано</span><span class="sxs-lookup"><span data-stu-id="8a222-112">Specified</span></span>

    <span data-ttu-id="8a222-113">В поле **Распределение подоходного налога** отображается метод распределения TDS для графика оплаты.</span><span class="sxs-lookup"><span data-stu-id="8a222-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="8a222-114">Если выбрано **Итого** в поле **Распределение**, в поле **Распределение подоходного налога** автоматически устанавливается значение **Итого**.</span><span class="sxs-lookup"><span data-stu-id="8a222-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="8a222-115">При выборе **Фиксированная сумма**, **Фиксированное количество** или **Указано** в поле **Распределение** в поле **Распределение подоходного налога** автоматически устанавливается значение **Пропорционально**.</span><span class="sxs-lookup"><span data-stu-id="8a222-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a222-116">Если для поля **Распределение подоходного налога** установлено значение **Итого**, платежные взносы рассчитываются на основе валовой суммы, которая включает сумму TDS.</span><span class="sxs-lookup"><span data-stu-id="8a222-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="8a222-117">Если для поля **Распределение подоходного налога** установлено значение **Пропорционально**, платежные взносы рассчитываются на основе валовой суммы накладной после удержания суммы TDS.</span><span class="sxs-lookup"><span data-stu-id="8a222-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="8a222-118">Введите остальные необходимые данные и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8a222-118">Enter the other required details, and then close the page.</span></span>
