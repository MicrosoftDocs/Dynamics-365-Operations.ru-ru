---
title: Создание нового продукта
description: В этой теме описывается создание нового общего продукта.
author: ShylaThompson
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6d33a13920e1881cdc69ad7c100180d3b3b441d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820042"
---
# <a name="create-a-new-product"></a><span data-ttu-id="166a1-103">Создание нового продукта</span><span class="sxs-lookup"><span data-stu-id="166a1-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="166a1-104">В этой теме описывается создание нового общего продукта.</span><span class="sxs-lookup"><span data-stu-id="166a1-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="166a1-105">Она обычно выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="166a1-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="166a1-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="166a1-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="166a1-107">Создание продукта</span><span class="sxs-lookup"><span data-stu-id="166a1-107">Create a product</span></span>
1. <span data-ttu-id="166a1-108">В области переходов выберите **Модули > Управление сведениями о продукте > Продукты > Продукты**.</span><span class="sxs-lookup"><span data-stu-id="166a1-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="166a1-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="166a1-109">Select **New**.</span></span>
3. <span data-ttu-id="166a1-110">В поле **Номер продукта** введите значение.</span><span class="sxs-lookup"><span data-stu-id="166a1-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="166a1-111">Если номерная серия не настроена для номера продуктов, ее необходимо ввести вручную.</span><span class="sxs-lookup"><span data-stu-id="166a1-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="166a1-112">В поле **Имя продукта** введите значение.</span><span class="sxs-lookup"><span data-stu-id="166a1-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="166a1-113">В качестве имени продукта по умолчанию используется имя поиска.</span><span class="sxs-lookup"><span data-stu-id="166a1-113">The product name defaults to the search name.</span></span> <span data-ttu-id="166a1-114">Это значение можно изменить при необходимости.</span><span class="sxs-lookup"><span data-stu-id="166a1-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="166a1-115">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="166a1-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="166a1-116">Настройка групп аналитик</span><span class="sxs-lookup"><span data-stu-id="166a1-116">Set up dimension groups</span></span>
1. <span data-ttu-id="166a1-117">Выберите **Группы аналитики**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="166a1-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="166a1-118">В поле **Группа аналитик хранения** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="166a1-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="166a1-119">Группа аналитик хранения определяет, какие аналитики хранения необходимо ввести в каждой проводке по продукту и как он будет отслеживается в запасах.</span><span class="sxs-lookup"><span data-stu-id="166a1-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="166a1-120">В поле **Группа аналитик отслеживания** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="166a1-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="166a1-121">Группа аналитик отслеживания определяет, какие аналитики отслеживания необходимо ввести для каждой проводки по продукту и как он будет обрабатываться в запасах.</span><span class="sxs-lookup"><span data-stu-id="166a1-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="166a1-122">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="166a1-122">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]