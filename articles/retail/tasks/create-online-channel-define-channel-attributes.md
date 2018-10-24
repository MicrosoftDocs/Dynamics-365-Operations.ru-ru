--- 
title: "Создание канала продаж через интернет и определение атрибутов канала"
description: "Эта процедура содержит указания по созданию нового канала и его добавлению в организационную иерархию."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e066e9901a97bd5b72815a7af472247ef519ecb9
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="d6432-103">Создание канала продаж через интернет и определение атрибутов канала</span><span class="sxs-lookup"><span data-stu-id="d6432-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d6432-104">Эта процедура содержит указания по созданию нового канала и его добавлению в организационную иерархию.</span><span class="sxs-lookup"><span data-stu-id="d6432-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="d6432-105">Необходимо создать организационную иерархию перед созданием нового интернет-канала.</span><span class="sxs-lookup"><span data-stu-id="d6432-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="d6432-106">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="d6432-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="d6432-107">Создание нового интернет-канала</span><span class="sxs-lookup"><span data-stu-id="d6432-107">Create a new online channel</span></span>
1. <span data-ttu-id="d6432-108">Перейдите в раздел "Розничная торговля и коммерция" > "Каналы" > "Интернет-магазины".</span><span class="sxs-lookup"><span data-stu-id="d6432-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="d6432-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d6432-109">Click New.</span></span>
3. <span data-ttu-id="d6432-110">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d6432-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d6432-111">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6432-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="d6432-112">В поле "Часовой пояс магазина" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="d6432-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="d6432-113">В поле "Клиент по умолчанию" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6432-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="d6432-114">В поле "Адресная книга клиентов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6432-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="d6432-115">В поле "Условия оплаты" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6432-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="d6432-116">В поле "Способ оплаты" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6432-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="d6432-117">В поле "Профиль уведомлений по электронной почте" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6432-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="d6432-118">Разверните раздел "Финансовые аналитики".</span><span class="sxs-lookup"><span data-stu-id="d6432-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="d6432-119">В поле "BusinessUnit" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6432-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="d6432-120">Аналогично задайте значение всех остальных аналитик по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6432-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="d6432-121">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d6432-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="d6432-122">Добавление интернет-канала в организационную иерархию</span><span class="sxs-lookup"><span data-stu-id="d6432-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="d6432-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d6432-123">Close the page.</span></span>
2. <span data-ttu-id="d6432-124">Перейдите в раздел "Управление организацией" > "Организации" > "Организационные иерархии".</span><span class="sxs-lookup"><span data-stu-id="d6432-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="d6432-125">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="d6432-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d6432-126">Щелкните "Вид".</span><span class="sxs-lookup"><span data-stu-id="d6432-126">Click View.</span></span>
5. <span data-ttu-id="d6432-127">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="d6432-127">Click Edit.</span></span>
    * <span data-ttu-id="d6432-128">Вы можете выбрать любой узел иерархии, под который вы хотите поместить новый канал.</span><span class="sxs-lookup"><span data-stu-id="d6432-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="d6432-129">Нажмите Вставить.</span><span class="sxs-lookup"><span data-stu-id="d6432-129">Click Insert.</span></span>
7. <span data-ttu-id="d6432-130">Щелкните "Канал розничной торговли".</span><span class="sxs-lookup"><span data-stu-id="d6432-130">Click Retail channel.</span></span>
8. <span data-ttu-id="d6432-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d6432-131">Click OK.</span></span>
9. <span data-ttu-id="d6432-132">Щелкните "Опубликовать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d6432-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="d6432-133">В поле "Действует с" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="d6432-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="d6432-134">Щелкните "Опубликовать".</span><span class="sxs-lookup"><span data-stu-id="d6432-134">Click Publish.</span></span>


