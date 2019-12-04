---
title: Типы атрибутов обслуживания
description: В этом разделе объясняется, как создавать типы атрибуты в «Управлении активами».
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 625e2c6a6b385c69d33ec4325a462310a37f1eed
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812199"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="37d83-103">Типы атрибутов обслуживания</span><span class="sxs-lookup"><span data-stu-id="37d83-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="37d83-104">В этом разделе объясняется, как создавать типы атрибуты в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="37d83-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="37d83-105">Атрибуты используются для описания свойств различных элементов.</span><span class="sxs-lookup"><span data-stu-id="37d83-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="37d83-106">Можно настроить атрибуты по следующим элементам:</span><span class="sxs-lookup"><span data-stu-id="37d83-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="37d83-107">Типы функциональных местоположений</span><span class="sxs-lookup"><span data-stu-id="37d83-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="37d83-108">Создание функциональных местоположений</span><span class="sxs-lookup"><span data-stu-id="37d83-108">Create functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="37d83-109">Типы активов</span><span class="sxs-lookup"><span data-stu-id="37d83-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="37d83-110">Активы</span><span class="sxs-lookup"><span data-stu-id="37d83-110">Assets</span></span>

<span data-ttu-id="37d83-111">Атрибуты, которые можно настроить, варьируются в зависимости от элемента.</span><span class="sxs-lookup"><span data-stu-id="37d83-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="37d83-112">Например, для функционального местоположения можно настроить атрибуты для конфигурации и физического размера местоположения.</span><span class="sxs-lookup"><span data-stu-id="37d83-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="37d83-113">Для типа актива или актива можно настроить атрибуты для объема двигателя, энергопотребления и максимальной емкости нагрузки при различных условиях.</span><span class="sxs-lookup"><span data-stu-id="37d83-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="37d83-114">Создание типов атрибутов</span><span class="sxs-lookup"><span data-stu-id="37d83-114">Create attribute types</span></span>

<span data-ttu-id="37d83-115">Можно создавать собственные типа атрибутов.</span><span class="sxs-lookup"><span data-stu-id="37d83-115">You can create your own attribute types.</span></span> <span data-ttu-id="37d83-116">Кроме того, можно перенести аналитики продуктов на страницу **Типы атрибутов**.</span><span class="sxs-lookup"><span data-stu-id="37d83-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="37d83-117">Выберите **Управление активами** \> **Настройка** \> **Типы атрибутов**.</span><span class="sxs-lookup"><span data-stu-id="37d83-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="37d83-118">При первой настройке типов атрибута выберите **Создать аналитики продукта** для автоматической передачи стандартных аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="37d83-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="37d83-119">Выберите **Создать** для создания нового типа атрибута.</span><span class="sxs-lookup"><span data-stu-id="37d83-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="37d83-120">В поле **Тип атрибута** введите название для типа атрибута.</span><span class="sxs-lookup"><span data-stu-id="37d83-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="37d83-121">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="37d83-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="37d83-122">В поле **Единица измерения**, по мере необходимости, выберите соответствующую единицу измерения атрибута.</span><span class="sxs-lookup"><span data-stu-id="37d83-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="37d83-123">В поле **Тип данных** выберите тип данных для единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="37d83-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="37d83-124">Если вы выбрали **Строка** в качестве типа данных, выполните следующие действия, чтобы создать значения для типа атрибута:</span><span class="sxs-lookup"><span data-stu-id="37d83-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="37d83-125">Выберите тип атрибута, а затем выберите **Значения**.</span><span class="sxs-lookup"><span data-stu-id="37d83-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="37d83-126">В поле **Значения атрибута** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="37d83-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="37d83-127">В поле **Тип атрибута** выберите тип атрибута (аналитика).</span><span class="sxs-lookup"><span data-stu-id="37d83-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="37d83-128">В поле **Значение** введите связанное значение.</span><span class="sxs-lookup"><span data-stu-id="37d83-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="37d83-129">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="37d83-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="37d83-130">Сохранение записи.</span><span class="sxs-lookup"><span data-stu-id="37d83-130">Save the record.</span></span>
    7. <span data-ttu-id="37d83-131">Вернитесь на страницу **Типы атрибута**.</span><span class="sxs-lookup"><span data-stu-id="37d83-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="37d83-132">Сохранение записи.</span><span class="sxs-lookup"><span data-stu-id="37d83-132">Save the record.</span></span>

    <span data-ttu-id="37d83-133">Поле **Типы функционального местоположения** показывает количество функциональных местоположений, которые используют тип атрибута.</span><span class="sxs-lookup"><span data-stu-id="37d83-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="37d83-134">Поле **Типы актива** показывает количество типов актива, которые используют это.</span><span class="sxs-lookup"><span data-stu-id="37d83-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
