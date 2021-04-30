---
title: Наборы финансовых аналитик
description: В этом разделе описываются наборы финансовых аналитик и даются некоторые советы по оптимизации их использования.
author: yukonpeegs
manager: AnnBe
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b719d8eb868cb1722b470be4443d01181078ce21
ms.sourcegitcommit: 97ada5d52ed1829dcf030dad254096cd8df25da8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/06/2021
ms.locfileid: "5864420"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="bcf37-103">Наборы финансовых аналитик</span><span class="sxs-lookup"><span data-stu-id="bcf37-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcf37-104">В этом разделе описываются наборы финансовых аналитик и даются некоторые советы по оптимизации их использования.</span><span class="sxs-lookup"><span data-stu-id="bcf37-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="bcf37-105">Набор аналитик представляет собой упорядоченный список финансовых аналитик, который может использоваться для суммирования данных главной книги в определенном пользователем виде.</span><span class="sxs-lookup"><span data-stu-id="bcf37-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="bcf37-106">Наборы аналитик в основном используются для определения оборотно-сальдовая ведомости.</span><span class="sxs-lookup"><span data-stu-id="bcf37-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="bcf37-107">Единственным стандартным набором аналитик является набор аналитик, содержащий только счет ГК.</span><span class="sxs-lookup"><span data-stu-id="bcf37-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="bcf37-108">Страница **Наборы финансовых аналитик** используется для создания наборов финансовых аналитик и управления ими.</span><span class="sxs-lookup"><span data-stu-id="bcf37-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="bcf37-109">Сальдо набора аналитик</span><span class="sxs-lookup"><span data-stu-id="bcf37-109">Dimension set balances</span></span>

<span data-ttu-id="bcf37-110">Набор аналитик может иметь сальдо на основе финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="bcf37-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="bcf37-111">Сальдо существуют в главной книге и основаны на определении набора аналитик.</span><span class="sxs-lookup"><span data-stu-id="bcf37-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="bcf37-112">Сальдо суммируются в данных главной книги для повышения производительности при их получении (например, при создании оборотно-сальдовая ведомости).</span><span class="sxs-lookup"><span data-stu-id="bcf37-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="bcf37-113">Создать сальдо</span><span class="sxs-lookup"><span data-stu-id="bcf37-113">Create balances</span></span>

<span data-ttu-id="bcf37-114">Используйте кнопку **Создать сальдо**, чтобы инициализировать сальдо для набора аналитик, в данный момент не имеющих сальдо.</span><span class="sxs-lookup"><span data-stu-id="bcf37-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="bcf37-115">Рекомендуется ограничивать количество наборов аналитик, имеющих сальдо, поскольку обновления сальдо влияют на все действия разноски главной книги.</span><span class="sxs-lookup"><span data-stu-id="bcf37-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="bcf37-116">Обновить сальдо</span><span class="sxs-lookup"><span data-stu-id="bcf37-116">Update balances</span></span>

<span data-ttu-id="bcf37-117">Используйте кнопку **Обновить сальдо**, чтобы включить в сальдо самую последнюю операцию разноски главной книги.</span><span class="sxs-lookup"><span data-stu-id="bcf37-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="bcf37-118">Обновления сальдо — это легкие операции.</span><span class="sxs-lookup"><span data-stu-id="bcf37-118">Balance updates are light operations.</span></span> <span data-ttu-id="bcf37-119">Они должны обработать только операцию разноски главной книги, которая произошла с момента последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="bcf37-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="bcf37-120">Отображение оборотно-сальдовой ведомости приводит к принудительному обновлению, чтобы гарантировать, что отображаемые сальдо являются текущими.</span><span class="sxs-lookup"><span data-stu-id="bcf37-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="bcf37-121">Рассмотрите возможность использования повторяющегося пакетного задания, чтобы обновления наиболее часто используемых наборов аналитик были быстрыми.</span><span class="sxs-lookup"><span data-stu-id="bcf37-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="bcf37-122">Таким образом, можно сократить время ожидания пользователями оборотно-сальдовой ведомости.</span><span class="sxs-lookup"><span data-stu-id="bcf37-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="bcf37-123">Повторно создать сальдо</span><span class="sxs-lookup"><span data-stu-id="bcf37-123">Rebuild balances</span></span>

<span data-ttu-id="bcf37-124">Используйте кнопку **Пересчитать сальдо** для повторного создания сальдо с нуля.</span><span class="sxs-lookup"><span data-stu-id="bcf37-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="bcf37-125">Таким образом, можно гарантировать, что они будут соответствовать данным в главной книге.</span><span class="sxs-lookup"><span data-stu-id="bcf37-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="bcf37-126">Пересчет сальдо требует большого количества обработки и, как правило, не требуется.</span><span class="sxs-lookup"><span data-stu-id="bcf37-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="bcf37-127">Если имеется сценарий, который регулярно нуждается в пересчете сальдо, рекомендуется обратиться в службу поддержки клиентов.</span><span class="sxs-lookup"><span data-stu-id="bcf37-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="bcf37-128">Служба поддержки клиентов может помочь определить, почему сальдо не соответствует данным в главной книге.</span><span class="sxs-lookup"><span data-stu-id="bcf37-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="bcf37-129">Очистить сальдо</span><span class="sxs-lookup"><span data-stu-id="bcf37-129">Clear balances</span></span>

<span data-ttu-id="bcf37-130">Используйте кнопку **Сбросить сальдо**, чтобы удалить сальдо и остановить все дальнейшие обновления.</span><span class="sxs-lookup"><span data-stu-id="bcf37-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="bcf37-131">Набор аналитик больше не будет влиять на действия разноски главной книги.</span><span class="sxs-lookup"><span data-stu-id="bcf37-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="bcf37-132">Дополнительные сведения см. в [Финансовые аналитики](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="bcf37-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
