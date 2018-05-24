---
title: "Задержки"
description: "В Этой статье представлена информация о задержанных датах в сводном планировании. Задержанная дата — это реалистичный срок выполнения, который проводка получает, если самая ранняя дата выполнения, которую сводное планирование вычисляет, более запрошенной даты."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fed78a7eba16d286a81b1e9ad709142422298c91
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="delays"></a><span data-ttu-id="7df23-104">Задержки</span><span class="sxs-lookup"><span data-stu-id="7df23-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7df23-105">В Этой статье представлена информация о задержанных датах в сводном планировании.</span><span class="sxs-lookup"><span data-stu-id="7df23-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="7df23-106">Задержанная дата — это реалистичный срок выполнения, который проводка получает, если самая ранняя дата выполнения, которую сводное планирование вычисляет, более запрошенной даты.</span><span class="sxs-lookup"><span data-stu-id="7df23-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="7df23-107">Сводное планирование может высчитать самую раннюю дату выполнения для проводки, основанной на временах упреждения, наличия материалов, доступной производительности и различных параметрах планирования.</span><span class="sxs-lookup"><span data-stu-id="7df23-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="7df23-108">Если сводное планирование высчитывает дату заказа, которая предшествует текущей дате, заказ нельзя выполнить в срок.</span><span class="sxs-lookup"><span data-stu-id="7df23-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="7df23-109">Поэтому заказ задерживается.</span><span class="sxs-lookup"><span data-stu-id="7df23-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="7df23-110">В этом случае сводное планирование заранее планирует заказ от настоящей даты и включает времена упреждения.</span><span class="sxs-lookup"><span data-stu-id="7df23-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="7df23-111">Эти времена упреждения начинаются с любых номенклатур компонентов более низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="7df23-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="7df23-112">Затем заказ получает отсроченную дату.</span><span class="sxs-lookup"><span data-stu-id="7df23-112">The order then receives a delayed date.</span></span> <span data-ttu-id="7df23-113">Отсроченная дата — это реалистичный срок выполнения, рассчитанный на основе текущей даты.</span><span class="sxs-lookup"><span data-stu-id="7df23-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="7df23-114">Сводное планирование также высчитывает число дней задержки.</span><span class="sxs-lookup"><span data-stu-id="7df23-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="7df23-115">В некоторых ситуациях необходимо не высчитывать отсрочки, например, когда пользователи знают, что они смогут ускорить времена упреждения, выбрав альтернативные способы поставки.</span><span class="sxs-lookup"><span data-stu-id="7df23-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="7df23-116">Вы можете настроить, как отсрочки высчитываются для группы покрытия.</span><span class="sxs-lookup"><span data-stu-id="7df23-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="7df23-117">Затем можно прикрепить группу покрытия к номенклатуре позднее.</span><span class="sxs-lookup"><span data-stu-id="7df23-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="7df23-118">На странице **Параметры сводного планирования** вы можете установить время начала для вычисления отсрочек.</span><span class="sxs-lookup"><span data-stu-id="7df23-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="7df23-119">Если заказ заполняется после этого времени, тогда один день задержки добавляется к дате отсрочки заказа.</span><span class="sxs-lookup"><span data-stu-id="7df23-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="7df23-120">**Примечание.** В предыдущих версиях высчитанные отсрочки назывались *сообщениями по фьючерсам*, дата отсрочки называлась *датой фьючерса*, а отсроченная проводки называлась *проводкой с заданным фьючерсом*.</span><span class="sxs-lookup"><span data-stu-id="7df23-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="additional-resources"></a><span data-ttu-id="7df23-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7df23-121">Additional resources</span></span>
--------

[<span data-ttu-id="7df23-122">Параметры покрытия</span><span class="sxs-lookup"><span data-stu-id="7df23-122">Coverage settings</span></span>](coverage-settings.md)




