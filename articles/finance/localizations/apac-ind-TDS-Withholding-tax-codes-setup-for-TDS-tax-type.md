---
title: Настройка налоговых кодов по подоходному налогу для налогов типа TDS
description: В этой теме объясняется, как настроить налоговые коды для налога, который удерживается в источнике (TDS).
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023550"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="75b32-103">Настройка налоговых кодов по подоходному налогу для налогов типа TDS</span><span class="sxs-lookup"><span data-stu-id="75b32-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75b32-104">В этой теме объясняется, как настроить налоговые коды для налога, который удерживается в источнике (TDS).</span><span class="sxs-lookup"><span data-stu-id="75b32-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="75b32-105">Перейдите в раздел **Налог \> Косвенные налоги \> Подоходный налог \> Коды подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="75b32-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="75b32-106">[![Страница "Коды подоходного налога"](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="75b32-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="75b32-107">В области действий выберите **Создать**, чтобы создать код подоходного налога для TDS, и введите требуемые сведения.</span><span class="sxs-lookup"><span data-stu-id="75b32-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="75b32-108">На экспресс-вкладке **Общие** в поле **Тип налога** выберите **TDS** для классификации налогового кода как налогового кода TDS.</span><span class="sxs-lookup"><span data-stu-id="75b32-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="75b32-109">В поле **Период сопоставления** выберите период сопоставления TDS для налогового кода TDS.</span><span class="sxs-lookup"><span data-stu-id="75b32-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="75b32-110">В поле **Счет ГК** выберите счет учета, на который разносится сумма TDS.</span><span class="sxs-lookup"><span data-stu-id="75b32-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="75b32-111">В поле **Счет дебиторской задолженности** выберите счет, на который должны быть разнесены суммы TDS, вычитаемые в проводках по продаже.</span><span class="sxs-lookup"><span data-stu-id="75b32-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="75b32-112">Поле **Исходный** автоматически устанавливается как **Процент от валовой суммы**, и значение не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="75b32-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="75b32-113">Невозможно установить источник как **Процент от чистой суммы** для налоговых кодов типа TDS.</span><span class="sxs-lookup"><span data-stu-id="75b32-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="75b32-114">В поле **Компонент подоходного налога** выберите компонент налога TDS для налогового кода TDS.</span><span class="sxs-lookup"><span data-stu-id="75b32-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="75b32-115">Выберите **Значения** на панели операций, чтобы открыть страницу **Значения подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="75b32-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="75b32-116">В поле **Начальная дата** введите дату начала для значения TDS.</span><span class="sxs-lookup"><span data-stu-id="75b32-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="75b32-117">В поле **Конечная дата** введите дату окончания.</span><span class="sxs-lookup"><span data-stu-id="75b32-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="75b32-118">Поля **Минимальный лимит**, **Верхний лимит** и **Процент исключения** недоступны для налоговых кодов типа налога TDS.</span><span class="sxs-lookup"><span data-stu-id="75b32-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="75b32-119">В поле **Значение** введите значение процента TDS для кода налога TDS.</span><span class="sxs-lookup"><span data-stu-id="75b32-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="75b32-120">Закройте страницу **Значения подоходного налога**, чтобы вернуться на страницу **Коды подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="75b32-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="75b32-121">Кнопка **Лимиты** на странице **Коды подоходного налога** недоступна для налоговых кодов типа налога TDS.</span><span class="sxs-lookup"><span data-stu-id="75b32-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="75b32-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="75b32-122">Close the page.</span></span>
