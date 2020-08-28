---
title: Расширение сущностей данных по запасам в наличии
description: В этом разделе приводится пример, в котором показано, как добавлять расширенные поля в представления INVENTORSITEONHANDENTITY и INVENTWAREHOUSEONHANDENTITY, чтобы возможности сущностей данных по запасам в наличии могли работать с этими расширениями.
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e3bf3a7d48b0aa3e48845882be0ee86da17ed040
ms.sourcegitcommit: e276348a63bfdb9e712c0ea86e6c2a68c50872c0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665412"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="027ab-103">Расширение сущностей данных по запасам в наличии</span><span class="sxs-lookup"><span data-stu-id="027ab-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="027ab-104">Microsoft Dynamics 365 Supply Chain Management предоставляет функции [расширяемости](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md), позволяющие [добавлять поля в таблицы посредством расширения](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span><span class="sxs-lookup"><span data-stu-id="027ab-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span></span> <span data-ttu-id="027ab-105">В этом разделе приводится пример, в котором показано, как добавлять расширенные поля в представления `INVENTORSITEONHANDENTITY` и `INVENTWAREHOUSEONHANDENTITY`, чтобы возможности сущностей данных по запасам в наличии могли работать с этими расширениями.</span><span class="sxs-lookup"><span data-stu-id="027ab-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="027ab-106">Дополнительные сведения о сущностях данных см. в разделе [Обзор управления данными](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="027ab-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="027ab-107">Ниже приводится список некоторых сущностей данных по запасам в наличии:</span><span class="sxs-lookup"><span data-stu-id="027ab-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="027ab-108">Запасы в наличии по сайту</span><span class="sxs-lookup"><span data-stu-id="027ab-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="027ab-109">Запасы в наличии по сайту V2</span><span class="sxs-lookup"><span data-stu-id="027ab-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="027ab-110">Запасы в наличии по складам</span><span class="sxs-lookup"><span data-stu-id="027ab-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="027ab-111">Запасы в наличии по складам v2</span><span class="sxs-lookup"><span data-stu-id="027ab-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="027ab-112">После добавления полей в таблицы, используемые представлением `inventSiteOnHandView`, необходимо синхронизировать механизм, чтобы расширения были правильно распознаны.</span><span class="sxs-lookup"><span data-stu-id="027ab-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="027ab-113">Расширьте представление `InventSiteOnHandView`, добавив поле расширения.</span><span class="sxs-lookup"><span data-stu-id="027ab-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="027ab-114">Расширьте представление `InventSiteOnHandAggregatedView` с помощью полей расширения.</span><span class="sxs-lookup"><span data-stu-id="027ab-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="027ab-115">Расширение класса viewBuilder `InventSiteOnHandAggregatedViewBuilder` путем изменения метода `getExtensionFields()`.</span><span class="sxs-lookup"><span data-stu-id="027ab-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="027ab-116">Таким образом, поля старого представления сопоставляются с новыми полями просмотра при выполнении синхронизации viewBuilder.</span><span class="sxs-lookup"><span data-stu-id="027ab-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="027ab-117">Например, к таблице `InventTable` добавлены следующие четыре поля с помощью расширения:</span><span class="sxs-lookup"><span data-stu-id="027ab-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="027ab-118">Настраиваемое поле 1</span><span class="sxs-lookup"><span data-stu-id="027ab-118">Custom field 1</span></span>
- <span data-ttu-id="027ab-119">Настраиваемое поле 2</span><span class="sxs-lookup"><span data-stu-id="027ab-119">Custom field 2</span></span>
- <span data-ttu-id="027ab-120">Настраиваемое поле 3</span><span class="sxs-lookup"><span data-stu-id="027ab-120">Custom field 3</span></span>
- <span data-ttu-id="027ab-121">Настраиваемое поле 4</span><span class="sxs-lookup"><span data-stu-id="027ab-121">Custom field 4</span></span>

<span data-ttu-id="027ab-122">В таком случае метод `getExtensionFields()` необходимо изменить следующим образом.</span><span class="sxs-lookup"><span data-stu-id="027ab-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

<span data-ttu-id="027ab-123">После выполнения этих шагов можно расширить сущности данных по запасам в наличии по сайту и запасам в наличии по складу, добавив новые поля.</span><span class="sxs-lookup"><span data-stu-id="027ab-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="027ab-124">Таким образом можно гарантировать, что расширенные поля будут распознаны и включены во время переноса данных, использующего эти сущности данных.</span><span class="sxs-lookup"><span data-stu-id="027ab-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>
