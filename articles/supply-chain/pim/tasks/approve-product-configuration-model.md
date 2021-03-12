---
title: Утверждение модели конфигурации продукта
description: Выполнение этой процедуры требует наличия не менее одной модели конфигурации продукта.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b548e2369f30e998ecde45408ff45893b88f9a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987112"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="8ff29-103">Утверждение модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="8ff29-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8ff29-104">Выполнение этой процедуры требует наличия не менее одной модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="8ff29-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="8ff29-105">Эта процедура использует модель динамика класса Hi-End в компании USMF с демонстрационными данными.</span><span class="sxs-lookup"><span data-stu-id="8ff29-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="8ff29-106">Обратите внимание, что эта модель уже была утверждена, но процедура описывает весь процесс.</span><span class="sxs-lookup"><span data-stu-id="8ff29-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="8ff29-107">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="8ff29-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="8ff29-108">Щелкните "Модели конфигурации продукта".</span><span class="sxs-lookup"><span data-stu-id="8ff29-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="8ff29-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8ff29-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8ff29-110">Выберите модель динамика класса Hi--End для этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="8ff29-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="8ff29-111">Щелкните "Версии".</span><span class="sxs-lookup"><span data-stu-id="8ff29-111">Click Versions.</span></span>
5. <span data-ttu-id="8ff29-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8ff29-112">Click New.</span></span>
6. <span data-ttu-id="8ff29-113">В поле "Номер продукта" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8ff29-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="8ff29-114">Ссылка на продукт, представляет версию модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="8ff29-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="8ff29-115">Только шаблоны продуктов с технологией конфигурации на основе ограничений появятся в данном списке.</span><span class="sxs-lookup"><span data-stu-id="8ff29-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="8ff29-116">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="8ff29-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="8ff29-117">Выберите, когда версия модели продукта будет доступна.</span><span class="sxs-lookup"><span data-stu-id="8ff29-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="8ff29-118">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="8ff29-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="8ff29-119">Выберите дату окончания, когда истечет срок действия данной версии модели продукта, или выберите "Никогда".</span><span class="sxs-lookup"><span data-stu-id="8ff29-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="8ff29-120">Щелкните "Утвердить", чтобы открыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8ff29-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="8ff29-121">В поле "Кем утверждено" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8ff29-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="8ff29-122">Выберите лицо, ответственное за утверждение модели продукта для эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="8ff29-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="8ff29-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8ff29-123">Click OK.</span></span>
12. <span data-ttu-id="8ff29-124">В поле "Метод ценообразования" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="8ff29-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="8ff29-125">Активируйте версию модели продукта.</span><span class="sxs-lookup"><span data-stu-id="8ff29-125">Activate the product model version.</span></span> <span data-ttu-id="8ff29-126">Возможен только один активный продукт для одной модели продукта одновременно.</span><span class="sxs-lookup"><span data-stu-id="8ff29-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="8ff29-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8ff29-127">Close the page.</span></span>

