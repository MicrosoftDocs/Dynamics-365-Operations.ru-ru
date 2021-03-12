---
title: Изменение спецификации обслуживания
description: Изменение спецификации обслуживания.
author: ShylaThompson
manager: tfehr
ms.date: 05/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c69f575dae369350e3191c31f961a861dea0fb07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996559"
---
# <a name="modify-a-service-bom"></a><span data-ttu-id="aaaa6-103">Изменение спецификации обслуживания</span><span class="sxs-lookup"><span data-stu-id="aaaa6-103">Modify a Service BOM</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="aaaa6-104">Можно записать историю элемента в спецификации обслуживания.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-104">You can record the history of an element in a service BOM.</span></span> <span data-ttu-id="aaaa6-105">Каждый раз при обновлении строки спецификации в области **История** создается строка истории.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-105">Every time that you update a BOM line, a history line is created in the **History** pane.</span></span> <span data-ttu-id="aaaa6-106">В строке истории указывается текущее состояние строки спецификации.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-106">The history line shows the current state of the BOM line.</span></span>

## <a name="update-a-service-bom-element"></a><span data-ttu-id="aaaa6-107">Обновление элемента спецификации обслуживания</span><span class="sxs-lookup"><span data-stu-id="aaaa6-107">Update a service BOM element</span></span>

1.  <span data-ttu-id="aaaa6-108">Щелкните **Управление сервисным обслуживанием** \> **Общее** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="aaaa6-109">Щелкните **Изменить**, чтобы открыть форму сведений **Соглашения о сервисном обслуживании**.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-109">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="aaaa6-110">В разделе **Панель операций** щелкните **Объекты сервисного обслуживания**, чтобы открыть форму **Объекты сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-110">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="aaaa6-111">Выберите объект, для которого требуется обновить строку спецификации, а затем щелкните **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-111">Select the object to update a BOM line for, and then click **Designer**.</span></span>

5.  <span data-ttu-id="aaaa6-112">В форме **Конструктор** выберите обновляемую строку спецификации, а затем нажмите кнопку **Редактировать строку спецификации**.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-112">In the **Designer** form, select the BOM line to update, and then click **Edit BOM line**.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="aaaa6-113">На вкладке <STRONG>Настройка</STRONG> установите флажок <STRONG>Редактир. при добавл.</STRONG>, если требуется открыть форму <STRONG>Редактирование строки спецификации</STRONG> при перетаскивании строки в спецификацию обслуживания.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-113">On the <STRONG>Setup</STRONG> tab, select the <STRONG>Edit when adding</STRONG> check box if you want the <STRONG>Edit BOM line</STRONG> form to open when you drag a line into the service BOM.</span></span></P>

6.  <span data-ttu-id="aaaa6-114">В поле **Количество** введите количество.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-114">In the **Quantity** field, enter the quantity.</span></span>

7.  <span data-ttu-id="aaaa6-115">Установите флажок **Создать строку заказа на обслуживание**, если необходимо создать строку заказа на обслуживание для элемента замены, по которой затем можно выставить накладную.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-115">If you want to create a service order line for the replacement item, which can then be invoiced, select the **Create service order line** check box.</span></span>

8.  <span data-ttu-id="aaaa6-116">Щелкните **OK**, чтобы закрыть форму.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-116">Click **OK** to close the form.</span></span>

## <a name="delete-a-service-bom-line"></a><span data-ttu-id="aaaa6-117">Удаление строки спецификации обслуживания</span><span class="sxs-lookup"><span data-stu-id="aaaa6-117">Delete a service BOM line</span></span>

1.  <span data-ttu-id="aaaa6-118">Щелкните **Управление сервисным обслуживанием** \> **Общее** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="aaaa6-119">Щелкните **Изменить**, чтобы открыть форму сведений **Соглашения о сервисном обслуживании**.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-119">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="aaaa6-120">В разделе **Панель операций** щелкните **Объекты сервисного обслуживания**, чтобы открыть форму **Объекты сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-120">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="aaaa6-121">Выберите объект, из которого требуется удалить строку спецификации обслуживания, а затем щелкните **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-121">Select the object to delete a service BOM line from, and then click **Designer**.</span></span>

5.  <span data-ttu-id="aaaa6-122">В форме **Конструктор** выберите удаляемую строку спецификации, а затем нажмите кнопку **Удалить строку спецификации**.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-122">In the **Designer** form, select the BOM line to delete, and then click **Delete BOM line**.</span></span>

## <a name="see-also"></a><span data-ttu-id="aaaa6-123">См. также</span><span class="sxs-lookup"><span data-stu-id="aaaa6-123">See also</span></span>

[<span data-ttu-id="aaaa6-124">Шаблоны спецификаций</span><span class="sxs-lookup"><span data-stu-id="aaaa6-124">Template BOMs</span></span>](template-boms.md)

  


