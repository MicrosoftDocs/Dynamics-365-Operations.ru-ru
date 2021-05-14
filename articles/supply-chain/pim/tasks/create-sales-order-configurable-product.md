---
title: Создание заказа на продажу для настраиваемого продукта
description: Эта процедура показывает, как применять шаблон конфигурации к продукту в заказе на продажу.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921297"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="5fc68-103">Создание заказа на продажу для настраиваемого продукта</span><span class="sxs-lookup"><span data-stu-id="5fc68-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5fc68-104">Эта процедура показывает, как применять шаблон конфигурации к продукту в заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="5fc68-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="5fc68-105">В этом примере использует модель динамика D0006 в демонстрационных данных компании USMF.</span><span class="sxs-lookup"><span data-stu-id="5fc68-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="5fc68-106">Обычно эту процедуру используется сотрудник, обрабатывающий заказы на продажу.</span><span class="sxs-lookup"><span data-stu-id="5fc68-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="5fc68-107">Создать заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="5fc68-107">Create a sales order</span></span>

1. <span data-ttu-id="5fc68-108">Перейдите **Продажи и маркетинг \> Рабочие области \> Обработка и запрос заказов на продажу**.</span><span class="sxs-lookup"><span data-stu-id="5fc68-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="5fc68-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="5fc68-109">Select **New**.</span></span>
1. <span data-ttu-id="5fc68-110">Выберите **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="5fc68-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="5fc68-111">В поле **Счет клиента** выберите *US-001*.</span><span class="sxs-lookup"><span data-stu-id="5fc68-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="5fc68-112">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5fc68-112">Select **OK**.</span></span>
1. <span data-ttu-id="5fc68-113">В поле **Код номенклатуры** выберите *D0006*.</span><span class="sxs-lookup"><span data-stu-id="5fc68-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="5fc68-114">Для этой задачи необходимо выбрать конфигурируемый продукт.</span><span class="sxs-lookup"><span data-stu-id="5fc68-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="5fc68-115">Выберите **Продукт и поставки**.</span><span class="sxs-lookup"><span data-stu-id="5fc68-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="5fc68-116">Выберите **Настроить строку**.</span><span class="sxs-lookup"><span data-stu-id="5fc68-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="5fc68-117">Обратите внимание, что цена была изменена, на основании конфигурации, которая была выбрана, и что в поле **Включая кабель** теперь установлено значение *Истина*.</span><span class="sxs-lookup"><span data-stu-id="5fc68-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="5fc68-118">Заметьте цену по умолчанию и параметры, выбранные для кабеля.</span><span class="sxs-lookup"><span data-stu-id="5fc68-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="5fc68-119">Выберите **Загрузить шаблон**.</span><span class="sxs-lookup"><span data-stu-id="5fc68-119">Select **Load template**.</span></span>
    * <span data-ttu-id="5fc68-120">В этом примере показано, как можно применить шаблон для выбора предопределенной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5fc68-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="5fc68-121">Если эта процедура используется как проводник по задаче, и вы хотите видеть другие значения атрибутов, которые доступны, необходимо нажать кнопку **Разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="5fc68-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="5fc68-122">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5fc68-122">Select **OK**.</span></span>
1. <span data-ttu-id="5fc68-123">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5fc68-123">Select **OK**.</span></span>
1. <span data-ttu-id="5fc68-124">Разверните раздел **Сведения о строке**.</span><span class="sxs-lookup"><span data-stu-id="5fc68-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="5fc68-125">Выберите вкладку **Продукт**.</span><span class="sxs-lookup"><span data-stu-id="5fc68-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="5fc68-126">Конфигурация номенклатуры теперь указана в аналитиках продукта.</span><span class="sxs-lookup"><span data-stu-id="5fc68-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="5fc68-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5fc68-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]