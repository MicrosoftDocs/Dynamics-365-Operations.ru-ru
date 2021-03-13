---
title: Гарантийные соглашения
description: В этом разделе описывается гарантийные соглашения в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7080af2059c9c9bcdd11ca0ee9c5e339cef69302
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021512"
---
# <a name="warranty-agreements"></a><span data-ttu-id="b1b07-103">Гарантийные соглашения</span><span class="sxs-lookup"><span data-stu-id="b1b07-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="b1b07-104">В управлении активами можно настроить условия гарантии, которые могут быть связаны с активом или с типом актива.</span><span class="sxs-lookup"><span data-stu-id="b1b07-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="b1b07-105">Условия гарантии создаются за конкретный период.</span><span class="sxs-lookup"><span data-stu-id="b1b07-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="b1b07-106">Гарантию можно настроить для обеспечения полного покрытия или частичного покрытия, а также можно настроить условия, которые относятся к часам, расходам и номенклатурам.</span><span class="sxs-lookup"><span data-stu-id="b1b07-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="b1b07-107">Первым шагом является создание любых гарантийных соглашений по поставщику для вашего оборудования.</span><span class="sxs-lookup"><span data-stu-id="b1b07-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="b1b07-108">Затем соглашения о гарантии присоединяются к активам или типам активов.</span><span class="sxs-lookup"><span data-stu-id="b1b07-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="b1b07-109">Гарантийные соглашения поставщика используются только в информационных целях.</span><span class="sxs-lookup"><span data-stu-id="b1b07-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="b1b07-110">Если гарантия поставщика настроена для актива, можно просмотреть период покрытия гарантии для актива.</span><span class="sxs-lookup"><span data-stu-id="b1b07-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="b1b07-111">Создание гарантийного соглашения</span><span class="sxs-lookup"><span data-stu-id="b1b07-111">Create a warranty agreement</span></span>

<span data-ttu-id="b1b07-112">Соглашение о гарантии может включать несколько строк соглашения для покрытия гарантии на рабочие часы, расходы и номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b1b07-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="b1b07-113">Выберите **Управление активами** \> **Настройка** \> **Активы** \> **Гарантия**.</span><span class="sxs-lookup"><span data-stu-id="b1b07-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="b1b07-114">Выберите **Создать**, чтобы создать продукт.</span><span class="sxs-lookup"><span data-stu-id="b1b07-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="b1b07-115">В поле **Гарантия** введите код гарантии.</span><span class="sxs-lookup"><span data-stu-id="b1b07-115">In the **Warranty** field, enter a warranty ID.</span></span> 
4. <span data-ttu-id="b1b07-116">В поле **Имя** введите описание.</span><span class="sxs-lookup"><span data-stu-id="b1b07-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="b1b07-117">На экспресс-вкладке **Сведения** в поле **Активы** отображается число активных активов, использующих соглашение о гарантии.</span><span class="sxs-lookup"><span data-stu-id="b1b07-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="b1b07-118">На экспресс-вкладке **Строки гарантии** выполните следующие шаги, чтобы добавить строки, которые должны быть включены в гарантийное соглашение:</span><span class="sxs-lookup"><span data-stu-id="b1b07-118">On the **Warranty lines** FastTab, follow these steps to add lines that should be included in a warranty agreement:</span></span>

    1. <span data-ttu-id="b1b07-119">Выберите **Добавить строку**, чтобы добавить новое условие в гарантию.</span><span class="sxs-lookup"><span data-stu-id="b1b07-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="b1b07-120">Порядковый номер строки автоматически вводится в поле **Строка**.</span><span class="sxs-lookup"><span data-stu-id="b1b07-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="b1b07-121">В поле **Период** выберите тип периода гарантии.</span><span class="sxs-lookup"><span data-stu-id="b1b07-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="b1b07-122">В поле **Интервал** введите число.</span><span class="sxs-lookup"><span data-stu-id="b1b07-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="b1b07-123">Это поле определяет число периодов действия гарантии.</span><span class="sxs-lookup"><span data-stu-id="b1b07-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="b1b07-124">В поле **Процент** введите процент покрытия для строки гарантии.</span><span class="sxs-lookup"><span data-stu-id="b1b07-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="b1b07-125">Процентное значение указывает, сколько покрывает ваша компания.</span><span class="sxs-lookup"><span data-stu-id="b1b07-125">The percentage indicates how much is covered by your company.</span></span>

![Страница гарантий](media/01-warranty.png)
