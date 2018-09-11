--- 
title: "Создание нового продукта"
description: "Эта задача показывает, как создать новый общий продукт."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c214ffaabfd0d185d46b9d80a514f589cc612050
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-new-product"></a><span data-ttu-id="40868-103">Создание нового продукта</span><span class="sxs-lookup"><span data-stu-id="40868-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40868-104">Эта задача показывает, как создать новый общий продукт.</span><span class="sxs-lookup"><span data-stu-id="40868-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="40868-105">Она обычно выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="40868-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="40868-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="40868-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="40868-107">Перейдите в раздел "Управление сведениями о продукте" > "Продукты" > "Продукты".</span><span class="sxs-lookup"><span data-stu-id="40868-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="40868-108">Создание продукта</span><span class="sxs-lookup"><span data-stu-id="40868-108">Create a product</span></span>
1. <span data-ttu-id="40868-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="40868-109">Click New.</span></span>
2. <span data-ttu-id="40868-110">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="40868-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="40868-111">Если номерная серия не настроена для номера продуктов, ее необходимо ввести вручную.</span><span class="sxs-lookup"><span data-stu-id="40868-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="40868-112">В поле "Имя продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="40868-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="40868-113">В качестве имени продукта по умолчанию используется имя поиска.</span><span class="sxs-lookup"><span data-stu-id="40868-113">The product name defaults to the search name.</span></span> <span data-ttu-id="40868-114">Это значение можно изменить при необходимости.</span><span class="sxs-lookup"><span data-stu-id="40868-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="40868-115">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="40868-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="40868-116">Настройка групп аналитик</span><span class="sxs-lookup"><span data-stu-id="40868-116">Set up dimension groups</span></span>
1. <span data-ttu-id="40868-117">Щелкните "Группы аналитики", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="40868-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="40868-118">В поле "Группа аналитик хранения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="40868-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="40868-119">Группа аналитик хранения определяет, какие аналитики хранения необходимо ввести в каждой проводке по продукту и как он будет отслеживается в запасах.</span><span class="sxs-lookup"><span data-stu-id="40868-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="40868-120">В поле "Группа аналитик отслеживания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="40868-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="40868-121">Группа аналитик отслеживания определяет, какие аналитики отслеживания необходимо ввести для каждой проводки по продукту и как он будет обрабатываться в запасах.</span><span class="sxs-lookup"><span data-stu-id="40868-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="40868-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="40868-122">Click OK.</span></span>


