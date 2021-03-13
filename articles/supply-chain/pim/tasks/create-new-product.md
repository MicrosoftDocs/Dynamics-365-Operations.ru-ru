---
title: Создание нового продукта
description: В этой теме описывается создание нового общего продукта.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d313d76d40476bec5c8bc9c8ea5fc93b217e7e87
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007574"
---
# <a name="create-a-new-product"></a><span data-ttu-id="d6005-103">Создание нового продукта</span><span class="sxs-lookup"><span data-stu-id="d6005-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6005-104">В этой теме описывается создание нового общего продукта.</span><span class="sxs-lookup"><span data-stu-id="d6005-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="d6005-105">Она обычно выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="d6005-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="d6005-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="d6005-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="d6005-107">Создание продукта</span><span class="sxs-lookup"><span data-stu-id="d6005-107">Create a product</span></span>
1. <span data-ttu-id="d6005-108">В области переходов выберите **Модули > Управление сведениями о продукте > Продукты > Продукты**.</span><span class="sxs-lookup"><span data-stu-id="d6005-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="d6005-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d6005-109">Select **New**.</span></span>
3. <span data-ttu-id="d6005-110">В поле **Номер продукта** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d6005-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="d6005-111">Если номерная серия не настроена для номера продуктов, ее необходимо ввести вручную.</span><span class="sxs-lookup"><span data-stu-id="d6005-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="d6005-112">В поле **Имя продукта** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d6005-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="d6005-113">В качестве имени продукта по умолчанию используется имя поиска.</span><span class="sxs-lookup"><span data-stu-id="d6005-113">The product name defaults to the search name.</span></span> <span data-ttu-id="d6005-114">Это значение можно изменить при необходимости.</span><span class="sxs-lookup"><span data-stu-id="d6005-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="d6005-115">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d6005-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="d6005-116">Настройка групп аналитик</span><span class="sxs-lookup"><span data-stu-id="d6005-116">Set up dimension groups</span></span>
1. <span data-ttu-id="d6005-117">Выберите **Группы аналитики**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d6005-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="d6005-118">В поле **Группа аналитик хранения** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6005-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="d6005-119">Группа аналитик хранения определяет, какие аналитики хранения необходимо ввести в каждой проводке по продукту и как он будет отслеживается в запасах.</span><span class="sxs-lookup"><span data-stu-id="d6005-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="d6005-120">В поле **Группа аналитик отслеживания** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6005-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="d6005-121">Группа аналитик отслеживания определяет, какие аналитики отслеживания необходимо ввести для каждой проводки по продукту и как он будет обрабатываться в запасах.</span><span class="sxs-lookup"><span data-stu-id="d6005-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="d6005-122">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d6005-122">Select **OK**.</span></span>

