---
title: Определение баллов поощрения по программе лояльности
description: Эта процедура содержит инструкции по определению баллов поощрения лояльности.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85ae26123d41fa74d32b102ddb7f021e9846a676
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564325"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="12367-103">Определение баллов поощрения по программе лояльности</span><span class="sxs-lookup"><span data-stu-id="12367-103">Define loyalty reward points</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="12367-104">Эта процедура содержит инструкции по определению баллов поощрения лояльности.</span><span class="sxs-lookup"><span data-stu-id="12367-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="12367-105">Необходимо настроить баллы поощрения лояльности перед настройкой программы лояльности.</span><span class="sxs-lookup"><span data-stu-id="12367-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="12367-106">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="12367-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="12367-107">Перейдите в раздел "Розничная торговля и коммерция" > "Клиенты" > "Лояльность" > "Баллы поощрения по программе лояльности".</span><span class="sxs-lookup"><span data-stu-id="12367-107">Go to Retail and commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="12367-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="12367-108">Click New.</span></span>
3. <span data-ttu-id="12367-109">В поле "Код точки вознаграждения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="12367-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="12367-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="12367-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="12367-111">В поле "Тип точки вознаграждения" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="12367-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="12367-112">Выберите количество, если вы хотите, чтобы баллы поощрения округлялись до ближайшего целого числа.</span><span class="sxs-lookup"><span data-stu-id="12367-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="12367-113">Выберите "Сумма", если вы хотите, чтобы баллы поощрения округлялись в соответствии с правилами округления валюты.</span><span class="sxs-lookup"><span data-stu-id="12367-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="12367-114">При выборе варианта "Количество" пропустите следующий шаг этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="12367-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="12367-115">В поле "Валюта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="12367-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="12367-116">В случае выбора варианта "Сумма" для баллов поощрения все начисленные баллы поощрения будут иметь выбранную валюту.</span><span class="sxs-lookup"><span data-stu-id="12367-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="12367-117">В случае выбора для баллов поощрения типа "Количество" это поле неприменимо, пропустите данный шаг.</span><span class="sxs-lookup"><span data-stu-id="12367-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="12367-118">Снимите или установите флажок "Погашаемо".</span><span class="sxs-lookup"><span data-stu-id="12367-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="12367-119">В поле "Классификация погашения" введите число.</span><span class="sxs-lookup"><span data-stu-id="12367-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="12367-120">Классификация погашения используется, если два или более подлежащих погашению набора баллов поощрения могут быть использованы для оплаты продуктов.</span><span class="sxs-lookup"><span data-stu-id="12367-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="12367-121">Если два набора баллов поощрения имеют одинаковый класс погашения, будет использоваться тот из них, который требует меньшего числа баллов.</span><span class="sxs-lookup"><span data-stu-id="12367-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="12367-122">В поле "Значение срока действия" введите число.</span><span class="sxs-lookup"><span data-stu-id="12367-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="12367-123">Срок действия баллов поощрения истекает через определенное количество дней, месяцев или лет после даты начисления баллов.</span><span class="sxs-lookup"><span data-stu-id="12367-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="12367-124">Значение "0" означает, что срок действия баллов поощрения лояльности никогда не истечет.</span><span class="sxs-lookup"><span data-stu-id="12367-124">A value of ‘0’ means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="12367-125">В поле "Единица измерения срока действия" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="12367-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="12367-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="12367-126">Click Save.</span></span>

