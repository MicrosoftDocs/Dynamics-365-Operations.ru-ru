---
title: Создание и приобретение основных средств в модуле "Расчеты с поставщиками"
description: В этом руководстве по задаче показано, как создать и приобрести основное средство в процессе покупки.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cb9a37c65fb8eab4db6084b91a71c13a45ba42c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142877"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="c7db4-103">Создание и приобретение основных средств в модуле "Расчеты с поставщиками"</span><span class="sxs-lookup"><span data-stu-id="c7db4-103">Create and acquire assets from Accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7db4-104">В этом руководстве по задаче показано, как создать и приобрести основное средство в процессе покупки.</span><span class="sxs-lookup"><span data-stu-id="c7db4-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="c7db4-105">В нем используются роли "Бухгалтер" и "Сотрудник отдела расчетов с поставщиками", а также демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="c7db4-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="c7db4-106">Настройка параметров основных средств</span><span class="sxs-lookup"><span data-stu-id="c7db4-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="c7db4-107">В **области перехода** выберите **Модули > Основные средства > Настройка > Параметры основных средств**.</span><span class="sxs-lookup"><span data-stu-id="c7db4-107">In the **Navigation pane**, go to **Modules > Fixed assets > Setup > Fixed assets parameters**.</span></span>
2. <span data-ttu-id="c7db4-108">Разверните экспресс-вкладку **Заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="c7db4-108">Expand the **Purchase orders** fastTab.</span></span>
3. <span data-ttu-id="c7db4-109">Установите флажок **Разрешить приобретение активов из модуля "Покупки"**.</span><span class="sxs-lookup"><span data-stu-id="c7db4-109">Check the **Allow asset acquisition from Purchasing** checkbox.</span></span>
4. <span data-ttu-id="c7db4-110">Установите флажок **Создавать актив при разноске поступления продуктов или накладной**.</span><span class="sxs-lookup"><span data-stu-id="c7db4-110">Check the **Create asset during product receipt or invoice posting** checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="c7db4-111">Создание новой накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="c7db4-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="c7db4-112">В **области перехода** выберите **Модули > Расчеты с поставщиками > Рабочие области > Запись накладной поставщика**.</span><span class="sxs-lookup"><span data-stu-id="c7db4-112">In the **Navigation pane**, go to **Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="c7db4-113">Щелкните **Новая накладная поставщика**.</span><span class="sxs-lookup"><span data-stu-id="c7db4-113">Click **New vendor invoice**.</span></span>
3. <span data-ttu-id="c7db4-114">В поле **Счет в накладной** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c7db4-114">In the **Invoice account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c7db4-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c7db4-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c7db4-116">В поле **Число** введите значение.</span><span class="sxs-lookup"><span data-stu-id="c7db4-116">In the **Number** field, type a value.</span></span>
6. <span data-ttu-id="c7db4-117">В поле **Дата разноски** введите дату.</span><span class="sxs-lookup"><span data-stu-id="c7db4-117">In the **Posting date** field, enter a date.</span></span>
7. <span data-ttu-id="c7db4-118">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="c7db4-118">Click **Add line**.</span></span>
8. <span data-ttu-id="c7db4-119">В поле **Код номенклатуры** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c7db4-119">In the **Item number** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="c7db4-120">Для приобретения основных средств можно использовать либо номенклатуры, не учитываемые в запасах, либо категории закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="c7db4-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="c7db4-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c7db4-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="c7db4-122">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="c7db4-122">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="c7db4-123">Одна строка накладной создает только одно основное средство независимо от количества.</span><span class="sxs-lookup"><span data-stu-id="c7db4-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span> <span data-ttu-id="c7db4-124">Значение поля количества по накладной будет перенесено в количество основного средства.</span><span class="sxs-lookup"><span data-stu-id="c7db4-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="c7db4-125">В поле **Цена за единицу** введите число.</span><span class="sxs-lookup"><span data-stu-id="c7db4-125">In the **Unit price** field, enter a number.</span></span>
12. <span data-ttu-id="c7db4-126">Разверните экспресс-вкладку **Сведения о строке**.</span><span class="sxs-lookup"><span data-stu-id="c7db4-126">Expand the **Line details** fastTab.</span></span>
13. <span data-ttu-id="c7db4-127">Перейдите на вкладку **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="c7db4-127">Click the **Fixed assets** tab.</span></span>
14. <span data-ttu-id="c7db4-128">Установите флажок **Создание нового основного средства**.</span><span class="sxs-lookup"><span data-stu-id="c7db4-128">Check the **Create a new fixed asset** checkbox.</span></span>
15. <span data-ttu-id="c7db4-129">В поле **Группа ОС** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c7db4-129">In the **Fixed asset group** field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="c7db4-130">В списке выберите группу основных средств для использования при создании нового основного средства.</span><span class="sxs-lookup"><span data-stu-id="c7db4-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="c7db4-131">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c7db4-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="c7db4-132">Щелкните **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="c7db4-132">Click **Post**.</span></span> <span data-ttu-id="c7db4-133">Основное средство будет создано и приобретено при разноске накладной.</span><span class="sxs-lookup"><span data-stu-id="c7db4-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

