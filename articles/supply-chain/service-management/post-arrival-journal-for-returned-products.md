---
title: Разноска журнала прихода возвращенных продуктов
description: Разноска журнала прихода возвращенных продуктов.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75f37ce016acb4b479a9cf4dff205562ce00f02c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545321"
---
# <a name="post-arrival-journal-for-returned-products"></a><span data-ttu-id="a606e-103">Разноска журнала прихода возвращенных продуктов</span><span class="sxs-lookup"><span data-stu-id="a606e-103">Post arrival journal for returned products</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a606e-104">Чтобы обработать возврат, сначала проверьте количество возврата, обновите поле количества в журнале прибытия номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a606e-104">To process a return, first validate the return quantity, update the quantity field in the item arrival journal.</span></span> <span data-ttu-id="a606e-105">Затем выберите код расстановки или укажите, что возвращенные номенклатуры должны быть проверены.</span><span class="sxs-lookup"><span data-stu-id="a606e-105">Then select a disposition code or indicate that the returned items have to be inspected.</span></span> <span data-ttu-id="a606e-106">После завершения этих шагов можно разнести журнал прибытия номенклатуры для этого заказа на возврат.</span><span class="sxs-lookup"><span data-stu-id="a606e-106">After completing these steps, you can post the item arrival journal for the return order.</span></span>

1.  <span data-ttu-id="a606e-107">Щелкните **Управление запасами** \> **Периодические операции** \> **Обзор прибытия**.</span><span class="sxs-lookup"><span data-stu-id="a606e-107">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="a606e-108">В фильтре **Имя настройки** выберите **Заказ на возврат**.</span><span class="sxs-lookup"><span data-stu-id="a606e-108">In the **Setup name** filter, select **Return order**.</span></span>

3.  <span data-ttu-id="a606e-109">Если список приходов длинный, используйте поля в области **Диапазон**, чтобы сузить список.</span><span class="sxs-lookup"><span data-stu-id="a606e-109">If the list of receipts is long, use the fields in the **Range** area to narrow the list.</span></span>

4.  <span data-ttu-id="a606e-110">Найдите строку заказа на возврат, которую необходимо разнести, установите для нее флажок **Выбрать для прибытия**, а затем щелкните **Начать прибытие**.</span><span class="sxs-lookup"><span data-stu-id="a606e-110">Locate the line of the return order that you want to post, select its **Select for arrival** box, and then click **Start arrival**.</span></span>

5.  <span data-ttu-id="a606e-111">Щелкните **Журналы** \> **Показать прибытия по приходам**, чтобы открыть форму **Журнал местоположений**.</span><span class="sxs-lookup"><span data-stu-id="a606e-111">Click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="a606e-112">Для просмотра подобной информации выберите журнал, а затем щелкните <STRONG>Строки</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a606e-112">To view detailed information, select a journal, and then click <STRONG>Lines</STRONG>.</span></span></P>


6.  <span data-ttu-id="a606e-113">Выполните все необходимые обновления, а затем нажмите кнопку **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="a606e-113">Make any necessary updates, and then click **Post**.</span></span>

<span data-ttu-id="a606e-114">После разноски журнала возвращенные номенклатуры регистрируются в запасах, а форма **Заказы на возврат** показывает, что номенклатуры прибыли на склад.</span><span class="sxs-lookup"><span data-stu-id="a606e-114">After the journal is posted, the returned items are registered in inventory, and the **Return orders** form indicates that the items have arrived at the warehouse.</span></span>

## <a name="see-also"></a><span data-ttu-id="a606e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a606e-115">See also</span></span>

<span data-ttu-id="a606e-116">[Журнал местоположений (форма)](https://technet.microsoft.com/en-us/library/aa584822\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="a606e-116">[Location journal (form)](https://technet.microsoft.com/en-us/library/aa584822\(v=ax.60\))</span></span>

  


