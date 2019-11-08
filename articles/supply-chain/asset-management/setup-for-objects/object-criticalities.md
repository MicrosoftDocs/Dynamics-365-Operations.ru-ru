---
title: Типы критичности активов
description: В этом разделе объясняются типы критичности актива в «Управлении активами».
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f96fcc7ebb8928c6d6b17b30465ad1625d9b5be4
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571078"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="8983b-103">Типы критичности активов</span><span class="sxs-lookup"><span data-stu-id="8983b-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8983b-104">В этом разделе объясняются типы критичности актива в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="8983b-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="8983b-105">Критичность активов связана с активами и передается в заказы на работу.</span><span class="sxs-lookup"><span data-stu-id="8983b-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="8983b-106">Она не может быть изменена в заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="8983b-106">It can't be changed on a work order.</span></span> <span data-ttu-id="8983b-107">Критичность активов используется для расчета критичности заказа на работу при планировании заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="8983b-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="8983b-108">Другими словами, она используется для расчета степени, в которой задание обслуживания по активу влияет на план производства и производительность в вашей компании.</span><span class="sxs-lookup"><span data-stu-id="8983b-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="8983b-109">Для получения дополнительной информации о настройке, связанной с расчетом рейтинговых оценок для планирования заказа на работу, см. раздел [Параметры управления активами](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8983b-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="8983b-110">Для настройки критичности сначала создаются типы критичности, которые следует использовать в настройке актива.</span><span class="sxs-lookup"><span data-stu-id="8983b-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="8983b-111">Затем вы настраиваете критичности активов.</span><span class="sxs-lookup"><span data-stu-id="8983b-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="8983b-112">Настройка типов критичности</span><span class="sxs-lookup"><span data-stu-id="8983b-112">Set up criticality types</span></span>

1. <span data-ttu-id="8983b-113">Выберите **Управление активами** \> **Настройка** \> **Активы** \> **Типы критичности**.</span><span class="sxs-lookup"><span data-stu-id="8983b-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="8983b-114">Выберите **Создать**, чтобы создать запись.</span><span class="sxs-lookup"><span data-stu-id="8983b-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="8983b-115">В поле **Критичность** введите число, указывавщее критичность.</span><span class="sxs-lookup"><span data-stu-id="8983b-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="8983b-116">В поле **Имя** введите имя типа критичности.</span><span class="sxs-lookup"><span data-stu-id="8983b-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="8983b-117">В поле **Коэффициент** введите коэффициент.</span><span class="sxs-lookup"><span data-stu-id="8983b-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="8983b-118">Этот коэффициент используется при расчете планировании заказа на работу для определения записи критичности, которая должна быть использована.</span><span class="sxs-lookup"><span data-stu-id="8983b-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="8983b-119">(Всегда используется запись с самым высоким коэффициентом). Этот параметр актуален, если, как показано на следующем рисунке, создаются строки критичности, которые имеют одинаковое значение критичности.</span><span class="sxs-lookup"><span data-stu-id="8983b-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![Страница типов критичности](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="8983b-121">Настройка критичностей актива</span><span class="sxs-lookup"><span data-stu-id="8983b-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="8983b-122">Выберите **Управление активами** \> **Настройка** \> **Критичности активов**.</span><span class="sxs-lookup"><span data-stu-id="8983b-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="8983b-123">Выберите **Создать**, чтобы создать запись.</span><span class="sxs-lookup"><span data-stu-id="8983b-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="8983b-124">В зависимости от требуемого уровня детализации для критичности актива сделайте соответствующие выборы в полях **Функциональное местоположение**, **Тип актива**, **Производитель**, **Модель**, **Актив**, **Категория типа задания**, **Тип задания**, **Вариант типа задания**, и **Потребность в задании**.</span><span class="sxs-lookup"><span data-stu-id="8983b-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8983b-125">При выборе критичности актива «Управление активами» проходит все записи критичности актива, чтобы проверить возможное соответствие.</span><span class="sxs-lookup"><span data-stu-id="8983b-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="8983b-126">Она всегда проверяет наиболее конкретные комбинации в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="8983b-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="8983b-127">Другими словами, «Управление активами» сначала проверяет **Потребность в задании**.</span><span class="sxs-lookup"><span data-stu-id="8983b-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="8983b-128">Если совпадение не найдено, оно проверяет **Вариант типа задания**.</span><span class="sxs-lookup"><span data-stu-id="8983b-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="8983b-129">Если совпадение не найдено, оно проверяет **Тип задания** и т.д.</span><span class="sxs-lookup"><span data-stu-id="8983b-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="8983b-130">Как вы можете видеть в макете страницы, это поведение означает, что, чтобы найти наиболее конкретную комбинацию, «Управление активами» проверяет каждую запись справа налево на совпадение.</span><span class="sxs-lookup"><span data-stu-id="8983b-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="8983b-131">Если совпадение не найдено, используется запись "по умолчанию", которая не имеет выбора.</span><span class="sxs-lookup"><span data-stu-id="8983b-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="8983b-132">В поле **Критичность** выберите один из значений критичности, созданных в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="8983b-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="8983b-133">Заметки о настройке критичности</span><span class="sxs-lookup"><span data-stu-id="8983b-133">Notes about criticality setup</span></span>

- <span data-ttu-id="8983b-134">Если вы измените критичность актива в этой настройке после того, как вы уже использовали ее в заказе на работу, критичность в заказе на работу не обновляется соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="8983b-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="8983b-135">Критичность в заказе на работу пересчитывается каждый раз при добавлении или удалении строки в заказ на работу или удаления из заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="8983b-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="8983b-136">Если заказ на работу содержит несколько заданий заказа на работу, наивысшая критичность, согласно полю **Коэффициент** на странице **Типы критичности**, всегда используется в заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="8983b-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="8983b-137">Как правило, критичность активв может меняться в течение определенного периода.</span><span class="sxs-lookup"><span data-stu-id="8983b-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="8983b-138">На критичность может повлиять покупка нового оборудования, реконструкции и так далее.</span><span class="sxs-lookup"><span data-stu-id="8983b-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="8983b-139">Рассмотрите возможность переоценки критичностей актива через регулярные промежутки времени (например, один раз в год или каждые два года), чтобы убедиться, что ваши определения критичности соответствуют текущей настройке производства.</span><span class="sxs-lookup"><span data-stu-id="8983b-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>
