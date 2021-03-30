---
title: Разноска журнала прихода возвращенных продуктов
description: Разноска журнала прихода возвращенных продуктов.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14619069c0e984060f67fc4536b311c6802bfec7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214306"
---
# <a name="post-arrival-journal-for-returned-products"></a><span data-ttu-id="15d96-103">Разноска журнала прихода возвращенных продуктов</span><span class="sxs-lookup"><span data-stu-id="15d96-103">Post arrival journal for returned products</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="15d96-104">Чтобы обработать возврат, сначала проверьте количество возврата, обновите поле количества в журнале прибытия номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="15d96-104">To process a return, first validate the return quantity, update the quantity field in the item arrival journal.</span></span> <span data-ttu-id="15d96-105">Затем выберите код расстановки или укажите, что возвращенные номенклатуры должны быть проверены.</span><span class="sxs-lookup"><span data-stu-id="15d96-105">Then select a disposition code or indicate that the returned items have to be inspected.</span></span> <span data-ttu-id="15d96-106">После завершения этих шагов можно разнести журнал прибытия номенклатуры для этого заказа на возврат.</span><span class="sxs-lookup"><span data-stu-id="15d96-106">After completing these steps, you can post the item arrival journal for the return order.</span></span>

1.  <span data-ttu-id="15d96-107">Щелкните **Управление запасами** \> **Периодические операции** \> **Обзор прибытия**.</span><span class="sxs-lookup"><span data-stu-id="15d96-107">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="15d96-108">В фильтре **Имя настройки** выберите **Заказ на возврат**.</span><span class="sxs-lookup"><span data-stu-id="15d96-108">In the **Setup name** filter, select **Return order**.</span></span>

3.  <span data-ttu-id="15d96-109">Если список приходов длинный, используйте поля в области **Диапазон**, чтобы сузить список.</span><span class="sxs-lookup"><span data-stu-id="15d96-109">If the list of receipts is long, use the fields in the **Range** area to narrow the list.</span></span>

4.  <span data-ttu-id="15d96-110">Найдите строку заказа на возврат, которую необходимо разнести, установите для нее флажок **Выбрать для прибытия**, а затем щелкните **Начать прибытие**.</span><span class="sxs-lookup"><span data-stu-id="15d96-110">Locate the line of the return order that you want to post, select its **Select for arrival** box, and then click **Start arrival**.</span></span>

5.  <span data-ttu-id="15d96-111">Щелкните **Журналы** \> **Показать прибытия по приходам**, чтобы открыть форму **Журнал местоположений**.</span><span class="sxs-lookup"><span data-stu-id="15d96-111">Click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="15d96-112">Для просмотра подобной информации выберите журнал, а затем щелкните <STRONG>Строки</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="15d96-112">To view detailed information, select a journal, and then click <STRONG>Lines</STRONG>.</span></span></P>


6.  <span data-ttu-id="15d96-113">Выполните все необходимые обновления, а затем нажмите кнопку **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="15d96-113">Make any necessary updates, and then click **Post**.</span></span>

<span data-ttu-id="15d96-114">После разноски журнала возвращенные номенклатуры регистрируются в запасах, а форма **Заказы на возврат** показывает, что номенклатуры прибыли на склад.</span><span class="sxs-lookup"><span data-stu-id="15d96-114">After the journal is posted, the returned items are registered in inventory, and the **Return orders** form indicates that the items have arrived at the warehouse.</span></span>

## <a name="see-also"></a><span data-ttu-id="15d96-115">См. также</span><span class="sxs-lookup"><span data-stu-id="15d96-115">See also</span></span>

<span data-ttu-id="15d96-116">[Журнал местоположений (форма)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="15d96-116">[Location journal (form)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]