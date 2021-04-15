---
title: Передача возврата на проверку
description: При регистрации возвращенной номенклатуры имеется возможность определить, что номенклатуру следует отправить для инвентаризации перед возвращением на склад или списать ее другим способом.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdee1ed2c7e98843e5dcfe9669e6a7c1eb11173c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810686"
---
# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="279a2-103">Передача возврата на проверку</span><span class="sxs-lookup"><span data-stu-id="279a2-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="279a2-104">При регистрации возврата имеется возможность определить, что номенклатуру следует отправить для инвентаризации перед возвращением на склад или списать ее другим способом.</span><span class="sxs-lookup"><span data-stu-id="279a2-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="279a2-105">Щелкните **Управление запасами** \> **Журналы** \> **Прибытие номенклатуры** \> **Прибытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="279a2-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="279a2-106">\-или-</span><span class="sxs-lookup"><span data-stu-id="279a2-106">\-or-</span></span>
    
    <span data-ttu-id="279a2-107">Щелкните **Управление запасами** \> **Журналы** \> **Прибытие номенклатуры** \> **Получение из производства**.</span><span class="sxs-lookup"><span data-stu-id="279a2-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="279a2-108">Регистрация прихода номенклатуры выполняется обычным способом в форме **Журнал местоположений**.</span><span class="sxs-lookup"><span data-stu-id="279a2-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="279a2-109">Для получения дополнительных сведений о регистрации прихода возврата см. раздел <A href="register-the-receipt-of-returned-items.md">Регистрация прихода возврата</A>.</span><span class="sxs-lookup"><span data-stu-id="279a2-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="279a2-110">На вкладке **Значения по умолчанию**, в области **Режим обработки** выберите поле **Управление карантином**.</span><span class="sxs-lookup"><span data-stu-id="279a2-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="279a2-111">Это приведет к созданию в системе карантинного заказа, и человек или подразделение, выполняющие инвентаризации, ответит на этот заказ с помощью формы **Карантинный заказ**.</span><span class="sxs-lookup"><span data-stu-id="279a2-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="279a2-112">См. также</span><span class="sxs-lookup"><span data-stu-id="279a2-112">See also</span></span>

[<span data-ttu-id="279a2-113">Прохождение возвратом процедуры проверки</span><span class="sxs-lookup"><span data-stu-id="279a2-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="279a2-114">Определение порядка списания возврата</span><span class="sxs-lookup"><span data-stu-id="279a2-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]