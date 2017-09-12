--- 
title: "Создание и приобретение основных средств в модуле \"Расчеты с поставщиками\""
description: "В этом руководстве по задаче показано, как создать и приобрести основное средство в процессе покупки."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c483622346bf61d0805402ae4ae8d2ba7c7aed89
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="9cd8e-103">Создание и приобретение основных средств в модуле "Расчеты с поставщиками"</span><span class="sxs-lookup"><span data-stu-id="9cd8e-103">Create and acquire assets from accounts payable</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9cd8e-104">В этом руководстве по задаче показано, как создать и приобрести основное средство в процессе покупки.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="9cd8e-105">В нем используются роли "Бухгалтер" и "Сотрудник отдела расчетов с поставщиками", а также демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="9cd8e-106">Настройка параметров основных средств</span><span class="sxs-lookup"><span data-stu-id="9cd8e-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="9cd8e-107">Перейдите в раздел "Основные средства" > "Настройка" > "Параметры основных средств".</span><span class="sxs-lookup"><span data-stu-id="9cd8e-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="9cd8e-108">Разверните или сверните раздел "Заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="9cd8e-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="9cd8e-109">Установите флажок «Разрешить приобретение активов из модуля "Покупки"».</span><span class="sxs-lookup"><span data-stu-id="9cd8e-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="9cd8e-110">Установите флажок "Создавать актив при разноске поступления продуктов или накладной".</span><span class="sxs-lookup"><span data-stu-id="9cd8e-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="9cd8e-111">Создание новой накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="9cd8e-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="9cd8e-112">Перейдите в раздел "Расчеты с поставщиками" > "Рабочие области" > "Запись накладной поставщика".</span><span class="sxs-lookup"><span data-stu-id="9cd8e-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="9cd8e-113">Щелкните "Новая накладная поставщика".</span><span class="sxs-lookup"><span data-stu-id="9cd8e-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="9cd8e-114">В поле "Счет в накладной" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9cd8e-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9cd8e-116">В поле "Число" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="9cd8e-117">В поле "Дата разноски" введите дату.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="9cd8e-118">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="9cd8e-118">Click Add line.</span></span>
8. <span data-ttu-id="9cd8e-119">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9cd8e-120">Для приобретения основных средств можно использовать либо номенклатуры, не учитываемые в запасах, либо категории закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="9cd8e-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="9cd8e-122">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9cd8e-123">Одна строка накладной создает только одно основное средство независимо от количества.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="9cd8e-124">Значение поля количества по накладной будет перенесено в количество основного средства.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="9cd8e-125">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="9cd8e-126">Разверните или сверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="9cd8e-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="9cd8e-127">Перейдите на вкладку "Основные средства".</span><span class="sxs-lookup"><span data-stu-id="9cd8e-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="9cd8e-128">Установите флажок "Создание нового основного средства".</span><span class="sxs-lookup"><span data-stu-id="9cd8e-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="9cd8e-129">В поле "Группа ОС" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="9cd8e-130">В списке выберите группу основных средств для использования при создании нового основного средства.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="9cd8e-131">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="9cd8e-132">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="9cd8e-132">Click Post.</span></span>
    * <span data-ttu-id="9cd8e-133">Основное средство будет создано и приобретено при разноске накладной.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  


