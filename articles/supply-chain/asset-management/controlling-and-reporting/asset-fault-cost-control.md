---
title: Управление стоимостью для ошибки актива
description: В этом разделе описывается контроль затрат на неисправности активов в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c25b3efbd0f2f0ec22a08aeac54ffb7fd9398c83
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253838"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="58ca2-103">Управление стоимостью для ошибки актива</span><span class="sxs-lookup"><span data-stu-id="58ca2-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="58ca2-104">В управлении активами можно рассчитать затраты на регистрации неисправностей активов, чтобы получить обзор фактических затрат по сравнению с бюджетными затратами.</span><span class="sxs-lookup"><span data-stu-id="58ca2-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="58ca2-105">Фактические затраты основываются на разнесенных проводках.</span><span class="sxs-lookup"><span data-stu-id="58ca2-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="58ca2-106">Датой является дата неисправности, в которую был записан признак неисправности.</span><span class="sxs-lookup"><span data-stu-id="58ca2-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="58ca2-107">Щелкните **Управление активами** > **Запросы** > **Ошибка актива** > **Управление стоимостью для ошибки актива**.</span><span class="sxs-lookup"><span data-stu-id="58ca2-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="58ca2-108">В диалоговом окне **Управление стоимостью для ошибки актива** выберите набор финансовых аналитик, который должен быть включен в расчет, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="58ca2-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="58ca2-109">Если не требуется показывать результаты, содержащие нулевые затраты, выберите "Да" для переключателя **Исключать нули**.</span><span class="sxs-lookup"><span data-stu-id="58ca2-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="58ca2-110">Можно использовать поле **Уровень**, чтобы указать, насколько подробными должны быть строки контроля затрат относительно функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="58ca2-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="58ca2-111">Например, если вставить число "1" в это поле, и имеется структура функциональных местоположений с несколькими уровнями, все строки контроля затрат на неисправности активов для функционального местоположения будут показаны на верхнем уровне, и поэтому часы по строке могут быть добавлены из функциональных местоположений, расположенных на более низком уровне.</span><span class="sxs-lookup"><span data-stu-id="58ca2-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="58ca2-112">Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки контроля затрат на неисправности активов на всех уровнях функциональных местоположений, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="58ca2-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="58ca2-113">Если требуется ограничить поиск, можно выбрать отдельные активы, даты сбоя и причины неисправности на экспресс-вкладке **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="58ca2-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="58ca2-114">Нажмите **ОК**, чтобы начать расчет.</span><span class="sxs-lookup"><span data-stu-id="58ca2-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="58ca2-115">Щелкните кнопки **Группировать по...**, чтобы отобразить необходимый уровень детализации для расчета.</span><span class="sxs-lookup"><span data-stu-id="58ca2-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="58ca2-116">Выбранные кнопки **Группировать по...** выделяются.</span><span class="sxs-lookup"><span data-stu-id="58ca2-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="58ca2-117">Нажимайте кнопку, чтобы активировать или деактивировать ее.</span><span class="sxs-lookup"><span data-stu-id="58ca2-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="58ca2-118">Пример</span><span class="sxs-lookup"><span data-stu-id="58ca2-118">Example</span></span>

<span data-ttu-id="58ca2-119">В этом примере показан расчет контроля затрат на ошибки в активах.</span><span class="sxs-lookup"><span data-stu-id="58ca2-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="58ca2-120">В поле **Исходный бюджет** отображаются бюджетные затраты из прогноза заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="58ca2-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="58ca2-121">В поле **Фактические затраты** отображаются разнесенные затраты по заказам на работу.</span><span class="sxs-lookup"><span data-stu-id="58ca2-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="58ca2-122">В поле **Подтвержденные затраты** отображается общая сумма затрат, которые подтверждены компанией в связи с заказами на работу.</span><span class="sxs-lookup"><span data-stu-id="58ca2-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![Рисунок 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="58ca2-124">Сведения о настройке неисправностей см. в разделе [Управление неисправностями](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="58ca2-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]