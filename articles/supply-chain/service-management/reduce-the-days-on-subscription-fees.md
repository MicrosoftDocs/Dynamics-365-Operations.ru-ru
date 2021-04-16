---
title: Уменьшение дней в сборах по подписке
description: Чтобы уменьшить количество дней существующего платежа по подписке, можно создать новую проводку, в которой следует удалить период времени, исключаемый из интервала платежа по подписке.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e8158c99d2447835f3656027fd73d7c22121536
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836094"
---
# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="e4a41-103">Уменьшение дней в сборах по подписке</span><span class="sxs-lookup"><span data-stu-id="e4a41-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e4a41-104">Чтобы уменьшить количество дней существующего платежа по подписке, можно создать новую проводку, в которой следует удалить период времени, исключаемый из интервала платежа по подписке.</span><span class="sxs-lookup"><span data-stu-id="e4a41-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="e4a41-105">Уменьшение дней в платеже по подписке</span><span class="sxs-lookup"><span data-stu-id="e4a41-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="e4a41-106">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Подписки на сервисное обслуживание** \> **Все подписки на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="e4a41-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="e4a41-107">Выберите подписку на обслуживание и на панели операций щелкните **Взносы по подписке**.</span><span class="sxs-lookup"><span data-stu-id="e4a41-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="e4a41-108">В поле **Тип подписки** выберите **Дни сокращения**.</span><span class="sxs-lookup"><span data-stu-id="e4a41-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="e4a41-109">Используйте поля **Дата начала** и **Дата окончания**, чтобы определить интервал дат подписки, который требуется удалить из периода платежа по подписке, а затем щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4a41-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="e4a41-110">Для просмотра созданной проводки в форме **Подписка** щелкните **Проводки по сборам**.</span><span class="sxs-lookup"><span data-stu-id="e4a41-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="e4a41-111">Пример</span><span class="sxs-lookup"><span data-stu-id="e4a41-111">Example</span></span>

<span data-ttu-id="e4a41-112">Если период проводки по подписке начинается 1 января и заканчивается 31 января, и требуется уменьшить период на 10 дней, создайте новую проводку с периодом сокращения с 1 января по 10 января.</span><span class="sxs-lookup"><span data-stu-id="e4a41-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="e4a41-113">(Период сокращения может также быть с 5 января по 15 января или любой другой десятидневный период.)</span><span class="sxs-lookup"><span data-stu-id="e4a41-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="e4a41-114">Кроме того, если **Дата начала** периода сокращения — 21 января (31 минус 10), можно установить для поля **Дата окончания** любую дату после 31 января, и 10 дней будут удалены из периода проводки по сборам.</span><span class="sxs-lookup"><span data-stu-id="e4a41-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4a41-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e4a41-115">See also</span></span>

[<span data-ttu-id="e4a41-116">Пример дней сокращения</span><span class="sxs-lookup"><span data-stu-id="e4a41-116">Reduction days example</span></span>](reduction-days-example.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]