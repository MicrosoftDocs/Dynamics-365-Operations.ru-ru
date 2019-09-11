---
title: Типы заказов на работу
description: В этом разделе описываются типы заказов на работу в модуле "Управление активами".
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 57120b51c069e49697f8ec4357265974a0d3afb4
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874586"
---
# <a name="work-order-types"></a><span data-ttu-id="d60fc-103">Типы заказов на работу</span><span class="sxs-lookup"><span data-stu-id="d60fc-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="d60fc-104">Типы заказов на работу используются для классификации заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="d60fc-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="d60fc-105">Например, могут быть заказы на работу, связанные с профилактическим обслуживанием или корректирующим обслуживанием.</span><span class="sxs-lookup"><span data-stu-id="d60fc-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="d60fc-106">Тип заказа на работу определяет принадлежность к модели жизненного цикла заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="d60fc-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="d60fc-107">Модель жизненного цикла заказов на работу определяет статусы жизненного цикла заказов на работу, которые могут быть настроены в заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="d60fc-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="d60fc-108">(Примеры состояний жизненного цикла заказов на работу включают в себя **Создан**, **Выполняется** и **Завершен**.)</span><span class="sxs-lookup"><span data-stu-id="d60fc-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="d60fc-109">Дополнительные сведения о состояниях жизненного цикла заказов на работу и этапах проекта см . в разделе [Состояния жизненного цикла заказов на работу](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="d60fc-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="d60fc-110">Выберите **Управление активами** \> **Настройка** \> **Заказы на работу** \> **Типы заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="d60fc-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="d60fc-111">Выберите **Создать**, чтобы создать тип заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="d60fc-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="d60fc-112">В поле **Тип заказов на работу** введите идентификатор для типа заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="d60fc-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="d60fc-113">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="d60fc-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="d60fc-114">В поле **Модель жизненного цикла заказа на работу** выберите модель жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="d60fc-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="d60fc-115">Задайте для параметра **Один специалист по обслуживанию** значение **Да**, если все задания по заказу на работу, которые относятся к заказу на работу данного типа, должны быть запланированы для одного и того же специалиста по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="d60fc-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="d60fc-116">В поле **Тип затрат** выберите **Корректирующее**, **Профилактическое** или **Инвестиционное**, как требуется.</span><span class="sxs-lookup"><span data-stu-id="d60fc-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="d60fc-117">Все задания заказа на работу в заказе на работу должны иметь одинаковый тип затрат.</span><span class="sxs-lookup"><span data-stu-id="d60fc-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="d60fc-118">В разделе **Обязательные** задайте для соответствующих параметров значение **Да**, чтобы указать, какие сведения о неисправности или простое из-за обслуживания будут добавляться в заказ на работу данного типа.</span><span class="sxs-lookup"><span data-stu-id="d60fc-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d60fc-119">Параметры в разделе **Обязательные** связаны с параметрами на экспресс-вкладке **Проверить** страницы **Состояния жизненного цикла заказов на работу** (**Управление активами** \> **Настройка** \> **Заказы на работу** \> **Состояния жизненного цикла**).</span><span class="sxs-lookup"><span data-stu-id="d60fc-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="d60fc-120">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d60fc-120">Select **Save**.</span></span>

![Рисунок 1](media/16-setup-for-work-orders.png)