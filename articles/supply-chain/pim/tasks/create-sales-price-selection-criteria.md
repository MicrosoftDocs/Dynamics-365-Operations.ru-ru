---
title: Создание критериев выбора цены продажи
description: Эта процедура демонстрирует порядок создания критерия выбора цены продажи для моделей цены продажи, основанных на атрибутах.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920539"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="d7d27-103">Создание критериев выбора цены продажи</span><span class="sxs-lookup"><span data-stu-id="d7d27-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7d27-104">Эта процедура демонстрирует порядок создания критерия выбора цены продажи для моделей цены продажи, основанных на атрибутах.</span><span class="sxs-lookup"><span data-stu-id="d7d27-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="d7d27-105">Для этой процедуры требуется наличие не менее одной модели цены продажи.</span><span class="sxs-lookup"><span data-stu-id="d7d27-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="d7d27-106">В этом примере используется модель цены для модели цены продажи решения динамика в демонстрационных данных компании USMF.</span><span class="sxs-lookup"><span data-stu-id="d7d27-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="d7d27-107">Обычно менеджер по продуктам использует эту процедуру.</span><span class="sxs-lookup"><span data-stu-id="d7d27-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="d7d27-108">Добавьте новый критерий для существующей модели цены продажи</span><span class="sxs-lookup"><span data-stu-id="d7d27-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="d7d27-109">Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Модели конфигурации продукта**.</span><span class="sxs-lookup"><span data-stu-id="d7d27-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="d7d27-110">В списке выберите строку для модели продукта решения динамика, но не нажимайте ссылку для имя модели.</span><span class="sxs-lookup"><span data-stu-id="d7d27-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="d7d27-111">В области действий выберите **Модель**.</span><span class="sxs-lookup"><span data-stu-id="d7d27-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="d7d27-112">Выберите **Критерии модели цены**.</span><span class="sxs-lookup"><span data-stu-id="d7d27-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="d7d27-113">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d7d27-113">Select **New**.</span></span>
1. <span data-ttu-id="d7d27-114">В поле **Имя** введите "Группа клиентов 10".</span><span class="sxs-lookup"><span data-stu-id="d7d27-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="d7d27-115">Имя критерия модели цены используется, чтобы помочь определить лежащие в основе критерии выбора.</span><span class="sxs-lookup"><span data-stu-id="d7d27-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="d7d27-116">В поле **Модель цены** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d7d27-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="d7d27-117">В поле **Тип заказа** выберите *Заказ на продажу*.</span><span class="sxs-lookup"><span data-stu-id="d7d27-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="d7d27-118">Тип заказа определяет поля базы данных, которые будут доступны для запроса выбора.</span><span class="sxs-lookup"><span data-stu-id="d7d27-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="d7d27-119">Введите дату в поле **Действительно с**.</span><span class="sxs-lookup"><span data-stu-id="d7d27-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="d7d27-120">В поле **Срок действия истекает** введите дату.</span><span class="sxs-lookup"><span data-stu-id="d7d27-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="d7d27-121">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d7d27-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="d7d27-122">Создайте запрос для критериев выбора</span><span class="sxs-lookup"><span data-stu-id="d7d27-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="d7d27-123">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="d7d27-123">Select **Edit**.</span></span>
2. <span data-ttu-id="d7d27-124">В поле **Таблица** выберите *Клиенты*.</span><span class="sxs-lookup"><span data-stu-id="d7d27-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="d7d27-125">В поле **Поле** выберите *Группа клиентов*.</span><span class="sxs-lookup"><span data-stu-id="d7d27-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="d7d27-126">В этом примере будет использоваться предоставленная группы клиентов для критериев выбора.</span><span class="sxs-lookup"><span data-stu-id="d7d27-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="d7d27-127">В поле **Критерии** выберите *Группа клиентов 10*.</span><span class="sxs-lookup"><span data-stu-id="d7d27-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="d7d27-128">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d7d27-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]