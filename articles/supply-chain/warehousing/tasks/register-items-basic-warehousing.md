--- 
title: "Регистрация номенклатур для базовых складских процессов с использованием журнала прихода номенклатуры"
description: "В этой процедуре показано, как зарегистрировать номенклатуры с помощью журнала прибытия номенклатур при использовании базового управления складами и модуля \"Управление запасами\"."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 184f38347e2525f3efef9b0d55003a94a75380d4
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="84d8d-103">Регистрация номенклатур для базовых складских процессов с использованием журнала прихода номенклатуры</span><span class="sxs-lookup"><span data-stu-id="84d8d-103">Register items for a basic warehousing enabled item using an item arrival journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84d8d-104">В этой процедуре показано, как зарегистрировать номенклатуры с помощью журнала прибытия номенклатур при использовании базового управления складами и модуля "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="84d8d-104">This procedure shows you how to register items using the item arrival journal when you are using “basic warehousing” in the Inventory management module.</span></span> <span data-ttu-id="84d8d-105">Обычно эту задачу выполняет сотрудник, ответственный за приемку.</span><span class="sxs-lookup"><span data-stu-id="84d8d-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="84d8d-106">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF и приведенные примеры значений.</span><span class="sxs-lookup"><span data-stu-id="84d8d-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="84d8d-107">Если вы не используете USMF, необходимо иметь подтвержденный заказ на покупку с открытой строкой заказа на покупку перед началом выполнения этого руководства.</span><span class="sxs-lookup"><span data-stu-id="84d8d-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="84d8d-108">Номенклатура в строке должна быть учтена в запасах, в ней не должны использоваться варианты продукта, и она не должна иметь аналитики отслеживания.</span><span class="sxs-lookup"><span data-stu-id="84d8d-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="84d8d-109">Кроме того, номенклатура должна быть связана с группой аналитик хранения с активным сайтом и складом.</span><span class="sxs-lookup"><span data-stu-id="84d8d-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="84d8d-110">Создание заголовка журнала прибытия номенклатур</span><span class="sxs-lookup"><span data-stu-id="84d8d-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="84d8d-111">Перейдите "Управление запасами" > "Записи журнала" > "Прибытие номенклатуры" > "Прибытие номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="84d8d-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="84d8d-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="84d8d-112">Click New.</span></span>
3. <span data-ttu-id="84d8d-113">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84d8d-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="84d8d-114">При использовании USMF можно ввести WHS.</span><span class="sxs-lookup"><span data-stu-id="84d8d-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="84d8d-115">При использовании других данных журнал, имя которого выбрано, должен иметь следующие свойства: для параметра "Проверять ячейки комплектации" должно быть задано значение "Нет", для параметра "Управление карантином" должно быть задано значение "Нет".</span><span class="sxs-lookup"><span data-stu-id="84d8d-115">If you’re using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="84d8d-116">В поле "Отборочная накладная" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84d8d-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="84d8d-117">Это код отборочной накладной из отборочной накладной, выданной поставщиком.</span><span class="sxs-lookup"><span data-stu-id="84d8d-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="84d8d-118">Добавьте уникальный номер.</span><span class="sxs-lookup"><span data-stu-id="84d8d-118">Add a unique number.</span></span>  
5. <span data-ttu-id="84d8d-119">В поле "Номер" выберите заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="84d8d-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="84d8d-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="84d8d-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="84d8d-121">Добавление строк в журнал прибытия номенклатур</span><span class="sxs-lookup"><span data-stu-id="84d8d-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="84d8d-122">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="84d8d-122">Click Functions.</span></span>
2. <span data-ttu-id="84d8d-123">Щелкните "Создать строки".</span><span class="sxs-lookup"><span data-stu-id="84d8d-123">Click Create lines.</span></span>
    * <span data-ttu-id="84d8d-124">Строки могут вводиться вручную в этот журнал или создаваться автоматически.</span><span class="sxs-lookup"><span data-stu-id="84d8d-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="84d8d-125">Ниже показано, как создать строки автоматически.</span><span class="sxs-lookup"><span data-stu-id="84d8d-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="84d8d-126">Установите или снимите флажок "Инициализировать количество".</span><span class="sxs-lookup"><span data-stu-id="84d8d-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="84d8d-127">В результате будет выполнена инициализация количества в строках журнала с количеством, незарегистрированным из строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="84d8d-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="84d8d-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="84d8d-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="84d8d-129">Разноска журнала</span><span class="sxs-lookup"><span data-stu-id="84d8d-129">Post the journal</span></span>
1. <span data-ttu-id="84d8d-130">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="84d8d-130">Click Post.</span></span>
2. <span data-ttu-id="84d8d-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="84d8d-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="84d8d-132">Создание поступления продуктов</span><span class="sxs-lookup"><span data-stu-id="84d8d-132">Generate the product receipt</span></span>
1. <span data-ttu-id="84d8d-133">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="84d8d-133">Click Functions.</span></span>
2. <span data-ttu-id="84d8d-134">Щелкните "Поступление продуктов".</span><span class="sxs-lookup"><span data-stu-id="84d8d-134">Click Product receipt.</span></span>
3. <span data-ttu-id="84d8d-135">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="84d8d-135">Click OK.</span></span>


