---
title: Настройка компонентов налога для типа налога TDS
description: В этой теме объясняется, как настроить компоненты подоходного налога для типа налога, удерживаемого в источнике (TDS). Здесь также объясняется, как определить предельный порог, используемый для расчета TDS для каждого компонента TDS.
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
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023533"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="50402-104">Настройка компонентов налога для типа налога TDS</span><span class="sxs-lookup"><span data-stu-id="50402-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50402-105">В этой теме объясняется, как настроить компоненты подоходного налога для типа налога, удерживаемого в источнике (TDS).</span><span class="sxs-lookup"><span data-stu-id="50402-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="50402-106">Компонентами TDS являются TDS, надбавка, PE-Cess и SHE Cess.</span><span class="sxs-lookup"><span data-stu-id="50402-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="50402-107">В этой теме также объясняется, как определить предел, используемый для расчета TDS для каждого компонента TDS.</span><span class="sxs-lookup"><span data-stu-id="50402-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="50402-108">Кроме того, можно определить пороговое значение исключения, используемое для расчета TDS для каждого компонента TDS.</span><span class="sxs-lookup"><span data-stu-id="50402-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="50402-109">Чтобы настроить компоненты TDS, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="50402-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="50402-110">Перейдите **Налог \> Настройка \> Подоходный налог \> Компоненты подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="50402-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="50402-111">[![Страница "Компоненты подоходного налога"](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="50402-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="50402-112">В поле **Тип налога** выберите **TDS**, чтобы настроить компоненты подоходного налога для типа налога TDS.</span><span class="sxs-lookup"><span data-stu-id="50402-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="50402-113">На панели операций выберите **Создать** для создания строки.</span><span class="sxs-lookup"><span data-stu-id="50402-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="50402-114">В поле **Компонент подоходного налога** введите имя компонента TDS.</span><span class="sxs-lookup"><span data-stu-id="50402-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="50402-115">В поле **Группа компонентов подоходного налога** выберите группу компонентов подоходного налога TDS, с которой связан компонент TDS.</span><span class="sxs-lookup"><span data-stu-id="50402-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="50402-116">На экспресс-вкладке **Общие** в поле **Описание** введите описание компонента TDS.</span><span class="sxs-lookup"><span data-stu-id="50402-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="50402-117">На панели операций выберите **Порог** для открытия страницы **Порог**, чтобы можно было определить пороговое значение, используемое для расчета TDS для компонента TDS.</span><span class="sxs-lookup"><span data-stu-id="50402-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="50402-118">Поля **Начальная дата** и **Конечная дата** используются для определения периода, к которому применяется пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="50402-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="50402-119">На экспресс-вкладке **Общие** в поле **Порог** введите сумму порога, используемую для расчета TDS для компонента TDS.</span><span class="sxs-lookup"><span data-stu-id="50402-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="50402-120">Налог вычитается в источнике, только когда суммарная сумма накладной пересекает пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="50402-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="50402-121">Например, если пороговое значение — 10 000, то TDS вычисляется после того, как общая сумма по накладной превышает 10 000 (иными словами, когда это 10 001 или более).</span><span class="sxs-lookup"><span data-stu-id="50402-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="50402-122">В поле **Порог исключения** введите сумму порога исключения, используемую для расчета TDS для компонента TDS.</span><span class="sxs-lookup"><span data-stu-id="50402-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="50402-123">Налог в строке накладной будет вычтен в источнике, только когда сумма пересекает значение исключения.</span><span class="sxs-lookup"><span data-stu-id="50402-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="50402-124">Например, если пороговое значение исключения — 5000, то TDS рассчитывается для конкретной строки накладной, если сумма по строке накладной превышает 5000 (иными словами, если это 5001 или более).</span><span class="sxs-lookup"><span data-stu-id="50402-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="50402-125">[![Страница «Порог»](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="50402-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="50402-126">Сумма порога исключения должна быть меньше или равна сумме порога.</span><span class="sxs-lookup"><span data-stu-id="50402-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="50402-127">Налог вычитается для проводки, если сумма проводки пересекает порог исключения, даже если суммарная сумма накладной не пересекает пороговое значение, указанное в поле **Порог**.</span><span class="sxs-lookup"><span data-stu-id="50402-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="50402-128">Закройте страницу **Порог**, чтобы вернуться на страницу **Компоненты подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="50402-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="50402-129">На панели операций выберите **Копировать**, чтобы открыть диалоговое окно **Копирование компонентов подоходного налога**, чтобы можно было скопировать компоненты TDS, которые были настроены для одной группы компонентов TDS, в другую группу компонентов TDS.</span><span class="sxs-lookup"><span data-stu-id="50402-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="50402-130">В поле **Из** выберите группу компонентов TDS, из которой будут копироваться компоненты TDS.</span><span class="sxs-lookup"><span data-stu-id="50402-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="50402-131">В поле **Куда** выберите группу компонентов подоходного налога, в которую необходимо скопировать компоненты TDS.</span><span class="sxs-lookup"><span data-stu-id="50402-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="50402-132">Общие компоненты TDS, присоединенные к обеим группам компонентов TDS, не копируются.</span><span class="sxs-lookup"><span data-stu-id="50402-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="50402-133">Нажмите **ОК**, чтобы скопировать и создать компоненты TDS для другой группы компонентов TDS на странице **Компоненты подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="50402-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="50402-134">[![Диалоговое окно "Копирование компонентов подоходного налога"](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="50402-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="50402-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="50402-135">Close the page.</span></span>
