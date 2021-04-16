---
title: Вложение складируемых номенклатур в объекты сервисного обслуживания
description: В этом разделе описывается, как вложить складируемую номенклатуру в объект сервисного обслуживания.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d85124eba19a7b4a0338b0ba7d0fcf616945c48f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824614"
---
# <a name="attach-inventory-items-to-service-objects"></a><span data-ttu-id="46d90-103">Вложение складируемых номенклатур в объекты сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="46d90-103">Attach inventory items to service objects</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="46d90-104">В этом разделе описывается, как вложить складируемую номенклатуру в объект сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="46d90-104">This topic explains how to attach an inventory item to a service object.</span></span> <span data-ttu-id="46d90-105">При вложении номенклатуры в объект сервисного обслуживания можно управлять действиями сервиса, которые выполняются для номенклатуры, и сообщать о них.</span><span class="sxs-lookup"><span data-stu-id="46d90-105">When you attach an item to a service object, you can control and report the service activities that are performed for the item.</span></span>

<span data-ttu-id="46d90-106">Прежде чем присоединять номенклатуры к объектам обслуживания, необходимо создать номенклатуры в форме **Сведения об используемом продукте**.</span><span class="sxs-lookup"><span data-stu-id="46d90-106">Before you can attach items to service objects, you must create the items in the **Released product details** form.</span></span> 

<span data-ttu-id="46d90-107">Чтобы вложить складируемую номенклатуру в объект сервисного обслуживания, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="46d90-107">Use the following steps to attach an inventory item to a service object:</span></span>

1.  <span data-ttu-id="46d90-108">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Объекты обслуживания** \> **Объекты обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="46d90-108">Click **Service management** \> **Setup** \> **Service objects** \> **Service objects**.</span></span>

2.  <span data-ttu-id="46d90-109">В поле **Код номенклатуры** выберите номенклатуру для вложения в объект сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="46d90-109">In the **Item number** field, select the item to attach to the service object.</span></span>

3.  <span data-ttu-id="46d90-110">Сохранение объекта обслуживания.</span><span class="sxs-lookup"><span data-stu-id="46d90-110">Save the service object.</span></span>

<span data-ttu-id="46d90-111">Номенклатура присоединена к объекту обслуживания, при этом любые складские аналитики, заданные для номенклатуры, также копируются в объект обслуживания.</span><span class="sxs-lookup"><span data-stu-id="46d90-111">The item is now attached to the service object, and any inventory dimensions specified for the item are also copied to the service object.</span></span>

## <a name="see-also"></a><span data-ttu-id="46d90-112">См. также</span><span class="sxs-lookup"><span data-stu-id="46d90-112">See also</span></span>

[<span data-ttu-id="46d90-113">Обзор объектов сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="46d90-113">Service objects overview</span></span>](service-objects.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]