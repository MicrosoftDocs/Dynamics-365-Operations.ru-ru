---
title: Утверждение модели конфигурации продукта
description: Выполнение этой процедуры требует наличия не менее одной модели конфигурации продукта.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c945756997b0580ac7ffb19261f9184e53a1c10
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920515"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="66734-103">Утверждение модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="66734-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="66734-104">Выполнение этой процедуры требует наличия не менее одной модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="66734-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="66734-105">Эта процедура использует модель динамика класса Hi-End в компании USMF с демонстрационными данными.</span><span class="sxs-lookup"><span data-stu-id="66734-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="66734-106">Обратите внимание, что эта модель уже была утверждена, но процедура описывает весь процесс.</span><span class="sxs-lookup"><span data-stu-id="66734-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="66734-107">Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Модели конфигурации продукта**.</span><span class="sxs-lookup"><span data-stu-id="66734-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="66734-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="66734-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="66734-109">Выберите модель динамика класса Hi--End для этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="66734-109">Select the High end speaker model for this procedure.</span></span>  
1. <span data-ttu-id="66734-110">Выберите **Версии**.</span><span class="sxs-lookup"><span data-stu-id="66734-110">Select **Versions**.</span></span>
1. <span data-ttu-id="66734-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="66734-111">Select **New**.</span></span>
1. <span data-ttu-id="66734-112">В поле **Номер продукта** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="66734-112">In the **Product number** field, enter or select a value.</span></span>
    * <span data-ttu-id="66734-113">Ссылка на продукт, представляет версию модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="66734-113">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="66734-114">Только шаблоны продуктов с технологией конфигурации на основе ограничений появятся в данном списке.</span><span class="sxs-lookup"><span data-stu-id="66734-114">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
1. <span data-ttu-id="66734-115">В поле **Дата начала** введите дату.</span><span class="sxs-lookup"><span data-stu-id="66734-115">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="66734-116">Выберите, когда версия модели продукта будет доступна.</span><span class="sxs-lookup"><span data-stu-id="66734-116">Select when the product model version will be available.</span></span>  
1. <span data-ttu-id="66734-117">В поле **Дата окончания** введите дату.</span><span class="sxs-lookup"><span data-stu-id="66734-117">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="66734-118">Выберите дату окончания, когда истечет срок действия данной версии модели продукта, или выберите "Никогда".</span><span class="sxs-lookup"><span data-stu-id="66734-118">Select an end date when this product model version will expire, or select Never.</span></span>  
1. <span data-ttu-id="66734-119">Выберите **Утвердить**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="66734-119">Select **Approve** to open the drop dialog.</span></span>
1. <span data-ttu-id="66734-120">В поле **Кем утверждено** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="66734-120">In the **Approved by** field, enter or select a value.</span></span>
    * <span data-ttu-id="66734-121">Выберите лицо, ответственное за утверждение модели продукта для эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="66734-121">Select the person who is responsible for approving product models for use in operations.</span></span>  
1. <span data-ttu-id="66734-122">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="66734-122">Select **OK**.</span></span>
1. <span data-ttu-id="66734-123">В поле **Метод ценообразования** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="66734-123">In the **Pricing method** field, select an option.</span></span>
    * <span data-ttu-id="66734-124">Активируйте версию модели продукта.</span><span class="sxs-lookup"><span data-stu-id="66734-124">Activate the product model version.</span></span> <span data-ttu-id="66734-125">Возможен только один активный продукт для одной модели продукта одновременно.</span><span class="sxs-lookup"><span data-stu-id="66734-125">It is only possible to have one product active for one product model at a time.</span></span>  
1. <span data-ttu-id="66734-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="66734-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]