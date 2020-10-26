---
title: Создание критериев выбора цены продажи
description: Эта процедура демонстрирует порядок создания критерия выбора цены продажи для моделей цены продажи, основанных на атрибутах.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ae444008e550d808a02d55dad02cc1b52874f0d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985469"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="e65c3-103">Создание критериев выбора цены продажи</span><span class="sxs-lookup"><span data-stu-id="e65c3-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e65c3-104">Эта процедура демонстрирует порядок создания критерия выбора цены продажи для моделей цены продажи, основанных на атрибутах.</span><span class="sxs-lookup"><span data-stu-id="e65c3-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="e65c3-105">Для этой процедуры требуется наличие не менее одной модели цены продажи.</span><span class="sxs-lookup"><span data-stu-id="e65c3-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="e65c3-106">В этом примере используется модель цены для модели цены продажи решения динамика в демонстрационных данных компании USMF.</span><span class="sxs-lookup"><span data-stu-id="e65c3-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="e65c3-107">Обычно менеджер по продуктам использует эту процедуру.</span><span class="sxs-lookup"><span data-stu-id="e65c3-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="e65c3-108">Добавьте новый критерий для существующей модели цены продажи</span><span class="sxs-lookup"><span data-stu-id="e65c3-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="e65c3-109">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="e65c3-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="e65c3-110">Щелкните "Модели конфигурации продукта".</span><span class="sxs-lookup"><span data-stu-id="e65c3-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="e65c3-111">В списке выберите строку для модели продукта решения динамика, но не нажимайте ссылку для имя модели.</span><span class="sxs-lookup"><span data-stu-id="e65c3-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="e65c3-112">В области действий щелкните "Модель".</span><span class="sxs-lookup"><span data-stu-id="e65c3-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="e65c3-113">Щелкните "Критерии модели цены".</span><span class="sxs-lookup"><span data-stu-id="e65c3-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="e65c3-114">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="e65c3-114">Click New.</span></span>
7. <span data-ttu-id="e65c3-115">В поле "Имя" введите "Группа клиентов 10".</span><span class="sxs-lookup"><span data-stu-id="e65c3-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="e65c3-116">Имя критерия модели цены используется, чтобы помочь определить лежащие в основе критерии выбора.</span><span class="sxs-lookup"><span data-stu-id="e65c3-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="e65c3-117">В поле "Модель цены" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e65c3-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="e65c3-118">В поле "Тип заказа" выберите "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="e65c3-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="e65c3-119">Тип заказа определяет поля базы данных, которые будут доступны для запроса выбора.</span><span class="sxs-lookup"><span data-stu-id="e65c3-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="e65c3-120">Введите дату в поле "Действительно с".</span><span class="sxs-lookup"><span data-stu-id="e65c3-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="e65c3-121">В поле "Срок действия истекает" введите дату.</span><span class="sxs-lookup"><span data-stu-id="e65c3-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="e65c3-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e65c3-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="e65c3-123">Создайте запрос для критериев выбора</span><span class="sxs-lookup"><span data-stu-id="e65c3-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="e65c3-124">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="e65c3-124">Click Edit.</span></span>
2. <span data-ttu-id="e65c3-125">В поле "Таблица" выберите "Клиенты".</span><span class="sxs-lookup"><span data-stu-id="e65c3-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="e65c3-126">В поле "Поле" выберите "Группа клиентов".</span><span class="sxs-lookup"><span data-stu-id="e65c3-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="e65c3-127">В этом примере будет использоваться предоставленная группы клиентов для критериев выбора.</span><span class="sxs-lookup"><span data-stu-id="e65c3-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="e65c3-128">В поле "Критерии" выберите "Группа клиентов 10".</span><span class="sxs-lookup"><span data-stu-id="e65c3-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="e65c3-129">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e65c3-129">Click OK.</span></span>

