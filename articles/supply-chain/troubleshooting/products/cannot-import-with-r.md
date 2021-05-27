---
title: Невозможно импортировать номенклатуру, используя сущность выпущенных продуктов версии V2
description: Невозможно импортировать номенклатуру, используя сущность выпущенных продуктов версии V2.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026839"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="22428-103">Невозможно импортировать номенклатуру, используя сущность выпущенных продуктов версии V2</span><span class="sxs-lookup"><span data-stu-id="22428-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="22428-104">Номер статьи базы знаний: 4611825</span><span class="sxs-lookup"><span data-stu-id="22428-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="22428-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="22428-105">Symptoms</span></span>

<span data-ttu-id="22428-106">При попытке импорта номенклатуры с использованием сущности *Выпущенные продукты V2* выводится сообщение об ошибке, как в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="22428-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="22428-107">Невозможно создать запись в группах аналитик отслеживания номенклатур (EcoResTrackingDimensionGroupItem).</span><span class="sxs-lookup"><span data-stu-id="22428-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="22428-108">Номер номенклатуры: 2040663, партия.</span><span class="sxs-lookup"><span data-stu-id="22428-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="22428-109">Запись уже существует.</span><span class="sxs-lookup"><span data-stu-id="22428-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="22428-110">Приказ</span><span class="sxs-lookup"><span data-stu-id="22428-110">Resolution</span></span>

<span data-ttu-id="22428-111">Для импорта новых выпущенных продуктов необходимо использовать сущность *Создание выпущенного продукта V2* вместо сущности *Выпущенные продукты V2*.</span><span class="sxs-lookup"><span data-stu-id="22428-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>
