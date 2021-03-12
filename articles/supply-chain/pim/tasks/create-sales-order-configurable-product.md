---
title: Создание заказа на продажу для настраиваемого продукта
description: Эта процедура показывает, как применять шаблон конфигурации к продукту в заказе на продажу.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77404694b3426f9ef051721191b607f91c908cc4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992328"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="8fc38-103">Создание заказа на продажу для настраиваемого продукта</span><span class="sxs-lookup"><span data-stu-id="8fc38-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8fc38-104">Эта процедура показывает, как применять шаблон конфигурации к продукту в заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="8fc38-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="8fc38-105">В этом примере использует модель динамика D0006 в демонстрационных данных компании USMF.</span><span class="sxs-lookup"><span data-stu-id="8fc38-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="8fc38-106">Обычно эту процедуру используется сотрудник, обрабатывающий заказы на продажу.</span><span class="sxs-lookup"><span data-stu-id="8fc38-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="8fc38-107">Создать заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="8fc38-107">Create a sales order</span></span>
1. <span data-ttu-id="8fc38-108">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="8fc38-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="8fc38-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8fc38-109">Click New.</span></span>
3. <span data-ttu-id="8fc38-110">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="8fc38-110">Click Sales order.</span></span>
4. <span data-ttu-id="8fc38-111">В поле "Счет клиента" выберите US-001.</span><span class="sxs-lookup"><span data-stu-id="8fc38-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="8fc38-112">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8fc38-112">Click OK.</span></span>
6. <span data-ttu-id="8fc38-113">В поле "Код номенклатуры" выберите "D0006".</span><span class="sxs-lookup"><span data-stu-id="8fc38-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="8fc38-114">Для этой задачи необходимо выбрать конфигурируемый продукт.</span><span class="sxs-lookup"><span data-stu-id="8fc38-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="8fc38-115">Щелкните "Продукт и поставки".</span><span class="sxs-lookup"><span data-stu-id="8fc38-115">Click Product and supply.</span></span>
8. <span data-ttu-id="8fc38-116">Щелкните "Настроить строку".</span><span class="sxs-lookup"><span data-stu-id="8fc38-116">Click Configure line.</span></span>
    * <span data-ttu-id="8fc38-117">Обратите внимание, что цена была изменена, на основании конфигурации, которая была выбрана, и что в поле "Включая кабель" теперь установлено значение "Истина".</span><span class="sxs-lookup"><span data-stu-id="8fc38-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="8fc38-118">Заметьте цену по умолчанию и параметры, выбранные для кабеля.</span><span class="sxs-lookup"><span data-stu-id="8fc38-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="8fc38-119">Щелкните "Загрузить шаблон".</span><span class="sxs-lookup"><span data-stu-id="8fc38-119">Click Load template.</span></span>
    * <span data-ttu-id="8fc38-120">В этом примере показано, как можно применить шаблон для выбора предопределенной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8fc38-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="8fc38-121">Если эта процедура используется как проводник по задаче, и вы хотите видеть другие значения атрибутов, которые доступны, необходимо нажать на кнопку "Разблокировать".</span><span class="sxs-lookup"><span data-stu-id="8fc38-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="8fc38-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8fc38-122">Click OK.</span></span>
11. <span data-ttu-id="8fc38-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8fc38-123">Click OK.</span></span>
12. <span data-ttu-id="8fc38-124">Разверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="8fc38-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="8fc38-125">Перейдите на вкладку "Продукт".</span><span class="sxs-lookup"><span data-stu-id="8fc38-125">Click the Product tab.</span></span>
    * <span data-ttu-id="8fc38-126">Конфигурация номенклатуры теперь указана в аналитиках продукта.</span><span class="sxs-lookup"><span data-stu-id="8fc38-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="8fc38-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8fc38-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="8fc38-128">Выберите конфигурацию продукта.</span><span class="sxs-lookup"><span data-stu-id="8fc38-128">Select the product configuration</span></span>

