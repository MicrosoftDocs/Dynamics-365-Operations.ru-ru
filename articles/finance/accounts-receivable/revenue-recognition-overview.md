---
title: Обзор процедуры признания выручки
description: В этом разделе содержится информация о функции признания выручки. Эта функция предоставляет гибкие возможности для определения правил определения цены и графика для признания выручки в заказах, состоящих из нескольких элементов.
author: kweekley
manager: aolson
ms.date: 08/24/2018
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
ms.openlocfilehash: d1aeb0cf556582ff53ca00c6bb8d863a088950b9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184125"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="b0edb-104">Обзор процедуры признания выручки</span><span class="sxs-lookup"><span data-stu-id="b0edb-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!NOTE]
> <span data-ttu-id="b0edb-105">Функцию признания выручки пока невозможно включить через механизм управления функциями.</span><span class="sxs-lookup"><span data-stu-id="b0edb-105">The Revenue recognition feature can't yet be turned on through Feature management.</span></span> <span data-ttu-id="b0edb-106">В данный момент это можно сделать только с помощью конфигурационных ключей.</span><span class="sxs-lookup"><span data-stu-id="b0edb-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="b0edb-107">Компаниям, продажи которых состоят из нескольких элементов, например из товаров, услуг и подписок, нужна возможность делить составные заказы и признавать выручку на основе определенных зависящих от конкретной компании или отрасли правил.</span><span class="sxs-lookup"><span data-stu-id="b0edb-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="b0edb-108">В общем случае процесс признания выручки позволяет выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="b0edb-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="b0edb-109">Распределите выручку, чтобы гарантировать, что соответствующая цена в выручке признается на основе значении компонентов в заказах, состоящих из нескольких элементов.</span><span class="sxs-lookup"><span data-stu-id="b0edb-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="b0edb-110">Отложите выручку на основе графика признания выручки, определяющего сроки исполнения контракта и проценты для признания выручки с течением времени.</span><span class="sxs-lookup"><span data-stu-id="b0edb-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

<span data-ttu-id="b0edb-111">Функция признания выручки предоставляет гибкие возможности для определения правил определения цен и графиков для признания выручки, действующих на уровне компании.</span><span class="sxs-lookup"><span data-stu-id="b0edb-111">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="b0edb-112">Для выпущенных продуктов признание выручки поддерживается в документах заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="b0edb-112">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="b0edb-113">В выпущенных продуктах имеются параметры, необходимые для определения цены в выручке и графика признания выручки.</span><span class="sxs-lookup"><span data-stu-id="b0edb-113">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="b0edb-114">Заказ на продажу может быть создан в проекте "Время и расходы".</span><span class="sxs-lookup"><span data-stu-id="b0edb-114">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="b0edb-115">Компании могут использовать только функцию графика признания выручки без использования функции цены в выручке.</span><span class="sxs-lookup"><span data-stu-id="b0edb-115">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="b0edb-116">Поэтому цена в строках заказа на продажу будет использоваться как выручка или как отложенная выручка.</span><span class="sxs-lookup"><span data-stu-id="b0edb-116">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="b0edb-117">Если имеется график признания выручки для строки заказа на продажу, цена в строке заказа на продажу будет отложена.</span><span class="sxs-lookup"><span data-stu-id="b0edb-117">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="b0edb-118">Если для строки заказа на продажу график признания выручки отсутствует, цена в строке заказа на продажу будет разнесена на счет выручки в момент выставления счета.</span><span class="sxs-lookup"><span data-stu-id="b0edb-118">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="b0edb-119">Цена в выручке рассчитывается либо при подтверждении заказа на продажу либо при разноске счета.</span><span class="sxs-lookup"><span data-stu-id="b0edb-119">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="b0edb-120">Чтобы посмотреть цену в выручке до разноски счета, необходимо подтвердить заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="b0edb-120">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="b0edb-121">При подтверждении заказа на продажу также создается ожидаемый график признания выручки, если какая-либо из строк заказа на продажу содержит график признания выручки.</span><span class="sxs-lookup"><span data-stu-id="b0edb-121">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="b0edb-122">Когда по заказу на продажу выставляется счет, ожидаемый график признания выручки удаляется и заменяется фактическим графиком признания выручки.</span><span class="sxs-lookup"><span data-stu-id="b0edb-122">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="b0edb-123">Подробные сведения о графике признания выручки сохраняются для каждой строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="b0edb-123">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="b0edb-124">Поэтому менеджер по признанию выручки может видеть подробные сведения и выпустить соответствующие строки, когда контрактное обязательство будет исполнено.</span><span class="sxs-lookup"><span data-stu-id="b0edb-124">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="b0edb-125">В конце каждого периода менеджер по признанию выручки может создать журнал выручки, чтобы выпустить все строки графика со сроком исполнения на дату, которую установит менеджер, или до нее.</span><span class="sxs-lookup"><span data-stu-id="b0edb-125">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date that he or she defines.</span></span> <span data-ttu-id="b0edb-126">Этот журнал выручки не разносится сразу.</span><span class="sxs-lookup"><span data-stu-id="b0edb-126">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="b0edb-127">Это позволяет менеджеру по признанию выручки проверить правильность сумм, выпускаемых из отложенной выручки в фактическую выручку.</span><span class="sxs-lookup"><span data-stu-id="b0edb-127">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="b0edb-128">Если в связи с изменением контракта нужно добавить строку в существующий заказ на продажу или создать новый заказ на продажу, можно с помощью процесса перераспределения скорректировать цену в выручке по всем строкам по заказам на продажу.</span><span class="sxs-lookup"><span data-stu-id="b0edb-128">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
