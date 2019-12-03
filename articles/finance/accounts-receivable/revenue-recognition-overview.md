---
title: Обзор процедуры признания выручки
description: В этом разделе содержится информация о функции признания выручки. Эта функция предоставляет гибкие возможности для определения правил определения цены и графика для признания выручки в заказах, состоящих из нескольких элементов.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8743183c46463395cad3138261860442701e0178
ms.sourcegitcommit: 0138b6c108a10f2bcb90c91205da8092917160d8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/11/2019
ms.locfileid: "2781904"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="4ee63-104">Обзор процедуры признания выручки</span><span class="sxs-lookup"><span data-stu-id="4ee63-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="4ee63-105">Функцию признания выручки невозможно включить через механизм управления функциями.</span><span class="sxs-lookup"><span data-stu-id="4ee63-105">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="4ee63-106">В данный момент это можно сделать только с помощью конфигурационных ключей.</span><span class="sxs-lookup"><span data-stu-id="4ee63-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="4ee63-107">Компаниям, продажи которых состоят из нескольких элементов, например из товаров, услуг и подписок, нужна возможность делить составные заказы и признавать выручку на основе определенных зависящих от конкретной компании или отрасли правил.</span><span class="sxs-lookup"><span data-stu-id="4ee63-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="4ee63-108">В общем случае процесс признания выручки позволяет выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="4ee63-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="4ee63-109">Распределите выручку, чтобы гарантировать, что соответствующая цена в выручке признается на основе значении компонентов в заказах, состоящих из нескольких элементов.</span><span class="sxs-lookup"><span data-stu-id="4ee63-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="4ee63-110">Отложите выручку на основе графика признания выручки, определяющего сроки исполнения контракта и проценты для признания выручки с течением времени.</span><span class="sxs-lookup"><span data-stu-id="4ee63-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE44iER]

<span data-ttu-id="4ee63-111">Видео [Порядок признания выручки в Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (см. выше) можно найти в [плейлисте Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) на YouTube.</span><span class="sxs-lookup"><span data-stu-id="4ee63-111">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="4ee63-112">Функция признания выручки предоставляет гибкие возможности для определения правил определения цен и графиков для признания выручки, действующих на уровне компании.</span><span class="sxs-lookup"><span data-stu-id="4ee63-112">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="4ee63-113">Для выпущенных продуктов признание выручки поддерживается в документах заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="4ee63-113">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="4ee63-114">В выпущенных продуктах имеются параметры, необходимые для определения цены в выручке и графика признания выручки.</span><span class="sxs-lookup"><span data-stu-id="4ee63-114">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="4ee63-115">Заказ на продажу может быть создан в проекте "Время и расходы".</span><span class="sxs-lookup"><span data-stu-id="4ee63-115">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="4ee63-116">Компании могут использовать только функцию графика признания выручки без использования функции цены в выручке.</span><span class="sxs-lookup"><span data-stu-id="4ee63-116">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="4ee63-117">Поэтому цена в строках заказа на продажу будет использоваться как выручка или как отложенная выручка.</span><span class="sxs-lookup"><span data-stu-id="4ee63-117">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="4ee63-118">Если имеется график признания выручки для строки заказа на продажу, цена в строке заказа на продажу будет отложена.</span><span class="sxs-lookup"><span data-stu-id="4ee63-118">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="4ee63-119">Если для строки заказа на продажу график признания выручки отсутствует, цена в строке заказа на продажу будет разнесена на счет выручки в момент выставления счета.</span><span class="sxs-lookup"><span data-stu-id="4ee63-119">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="4ee63-120">Цена в выручке рассчитывается либо при подтверждении заказа на продажу либо при разноске счета.</span><span class="sxs-lookup"><span data-stu-id="4ee63-120">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="4ee63-121">Чтобы посмотреть цену в выручке до разноски счета, необходимо подтвердить заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="4ee63-121">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="4ee63-122">При подтверждении заказа на продажу также создается ожидаемый график признания выручки, если какая-либо из строк заказа на продажу содержит график признания выручки.</span><span class="sxs-lookup"><span data-stu-id="4ee63-122">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="4ee63-123">Когда по заказу на продажу выставляется счет, ожидаемый график признания выручки удаляется и заменяется фактическим графиком признания выручки.</span><span class="sxs-lookup"><span data-stu-id="4ee63-123">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="4ee63-124">Подробные сведения о графике признания выручки сохраняются для каждой строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="4ee63-124">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="4ee63-125">Поэтому менеджер по признанию выручки может видеть подробные сведения и выпустить соответствующие строки, когда контрактное обязательство будет исполнено.</span><span class="sxs-lookup"><span data-stu-id="4ee63-125">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="4ee63-126">В конце каждого периода менеджер по признанию выручки может создать журнал выручки, чтобы выпустить все строки графика со сроком исполнения на дату, которую установит менеджер, или до нее.</span><span class="sxs-lookup"><span data-stu-id="4ee63-126">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date that he or she defines.</span></span> <span data-ttu-id="4ee63-127">Этот журнал выручки не разносится сразу.</span><span class="sxs-lookup"><span data-stu-id="4ee63-127">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="4ee63-128">Это позволяет менеджеру по признанию выручки проверить правильность сумм, выпускаемых из отложенной выручки в фактическую выручку.</span><span class="sxs-lookup"><span data-stu-id="4ee63-128">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="4ee63-129">Если в связи с изменением контракта нужно добавить строку в существующий заказ на продажу или создать новый заказ на продажу, можно с помощью процесса перераспределения скорректировать цену в выручке по всем строкам по заказам на продажу.</span><span class="sxs-lookup"><span data-stu-id="4ee63-129">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
