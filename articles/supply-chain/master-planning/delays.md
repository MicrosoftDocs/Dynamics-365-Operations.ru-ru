---
title: Задержки
description: В этом разделе представлена информация о задержанных датах в сводном планировании. Задержанная дата — это реалистичный срок выполнения, который проводка получает, если самая ранняя дата выполнения, которую сводное планирование вычисляет, более запрошенной даты.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c26fedf15118a304469604527c33a25871356be
ms.sourcegitcommit: 8eac5eee94bb32143df44c82a2dfdbe903967af8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2019
ms.locfileid: "878318"
---
# <a name="delays"></a><span data-ttu-id="81d73-104">Задержки</span><span class="sxs-lookup"><span data-stu-id="81d73-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81d73-105">В этом разделе представлена информация о задержанных датах в сводном планировании.</span><span class="sxs-lookup"><span data-stu-id="81d73-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="81d73-106">Задержанная дата — это реалистичный срок выполнения, который проводка получает, если самая ранняя дата выполнения, которую сводное планирование вычисляет, более запрошенной даты.</span><span class="sxs-lookup"><span data-stu-id="81d73-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="81d73-107">Сводное планирование может высчитать самую раннюю дату выполнения для проводки, основанной на временах упреждения, наличия материалов, доступной производительности и различных параметрах планирования.</span><span class="sxs-lookup"><span data-stu-id="81d73-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="81d73-108">Если сводное планирование высчитывает дату заказа, которая предшествует текущей дате, заказ нельзя выполнить в срок.</span><span class="sxs-lookup"><span data-stu-id="81d73-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="81d73-109">Поэтому заказ задерживается.</span><span class="sxs-lookup"><span data-stu-id="81d73-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="81d73-110">В этом случае сводное планирование заранее планирует заказ от настоящей даты и включает времена упреждения.</span><span class="sxs-lookup"><span data-stu-id="81d73-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="81d73-111">Эти времена упреждения начинаются с любых номенклатур компонентов более низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="81d73-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="81d73-112">Затем заказ получает отсроченную дату.</span><span class="sxs-lookup"><span data-stu-id="81d73-112">The order then receives a delayed date.</span></span> <span data-ttu-id="81d73-113">Отсроченная дата — это реалистичный срок выполнения, рассчитанный на основе текущей даты.</span><span class="sxs-lookup"><span data-stu-id="81d73-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="81d73-114">Сводное планирование также высчитывает число дней задержки.</span><span class="sxs-lookup"><span data-stu-id="81d73-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="81d73-115">В некоторых ситуациях необходимо не высчитывать отсрочки, например, когда пользователи знают, что они смогут ускорить времена упреждения, выбрав альтернативные способы поставки.</span><span class="sxs-lookup"><span data-stu-id="81d73-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="81d73-116">Вы можете настроить, как отсрочки высчитываются для группы покрытия.</span><span class="sxs-lookup"><span data-stu-id="81d73-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="81d73-117">Затем можно прикрепить группу покрытия к номенклатуре позднее.</span><span class="sxs-lookup"><span data-stu-id="81d73-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="81d73-118">На странице **Параметры сводного планирования** вы можете установить время начала для вычисления отсрочек.</span><span class="sxs-lookup"><span data-stu-id="81d73-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="81d73-119">Если заказ заполняется после этого времени, тогда один день задержки добавляется к дате отсрочки заказа.</span><span class="sxs-lookup"><span data-stu-id="81d73-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> <span data-ttu-id="81d73-120">[!ПРИМЕЧАНИЕ} В предыдущих версиях высчитанные отсрочки назывались *сообщениями по фьючерсам*, дата отсрочки называлась *датой фьючерса*, а отсроченная проводки называлась *проводкой с заданным фьючерсом*.</span><span class="sxs-lookup"><span data-stu-id="81d73-120">[!NOTE} In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="desired-date"></a><span data-ttu-id="81d73-121">Желаемая дата</span><span class="sxs-lookup"><span data-stu-id="81d73-121">Desired date</span></span>

<span data-ttu-id="81d73-122">На странице **Спланированный заказ** на вкладке **Задержки** имеется **Желаемая дата** для спланированного заказа.</span><span class="sxs-lookup"><span data-stu-id="81d73-122">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="81d73-123">Требуемая дата спланированного заказа является базовой датой для задержек, которая является вычисляемой датой, которая равна значению **Запрошенная дата**, рассчитанному из значения **Чистые потребности**.</span><span class="sxs-lookup"><span data-stu-id="81d73-123">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="81d73-124">Если спланированный заказ является строкой спецификации, строкой производства или строкой канбана, требуемая дата основывается на значении **Дата потребности**, и желаемая дата не будет отображаться на странице **Спланированный заказ**.</span><span class="sxs-lookup"><span data-stu-id="81d73-124">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="81d73-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="81d73-125">Additional resources</span></span>
--------

[<span data-ttu-id="81d73-126">Параметры покрытия</span><span class="sxs-lookup"><span data-stu-id="81d73-126">Coverage settings</span></span>](coverage-settings.md)
