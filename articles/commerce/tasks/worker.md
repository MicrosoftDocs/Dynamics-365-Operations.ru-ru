---
title: Настройка работника
description: Эта процедура демонстрирует порядок настройки работника в качестве торгового представителя, который имеет право на комиссионные по продажам в POS.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 73c200f7f6ff0aa5672e50c539bfaa5e30213185
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003611"
---
# <a name="configure-a-worker"></a><span data-ttu-id="706af-103">Настройка работника</span><span class="sxs-lookup"><span data-stu-id="706af-103">Configure a worker</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="706af-104">Эта процедура демонстрирует порядок настройки работника в качестве торгового представителя, который имеет право на комиссионные по продажам в POS.</span><span class="sxs-lookup"><span data-stu-id="706af-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="706af-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="706af-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="706af-106">Создание группы комиссий по продажам для работника</span><span class="sxs-lookup"><span data-stu-id="706af-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="706af-107">Перейдите в раздел "Продажи и маркетинг" > "Комиссии" > "Группы продаж".</span><span class="sxs-lookup"><span data-stu-id="706af-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="706af-108">Работники и могут быть назначены в одну или несколько групп продаж.</span><span class="sxs-lookup"><span data-stu-id="706af-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="706af-109">В POS можно выбрать любую группу продаж, содержащую работников из адресной книги магазина.</span><span class="sxs-lookup"><span data-stu-id="706af-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="706af-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="706af-110">Click New.</span></span>
3. <span data-ttu-id="706af-111">В поле "Группа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="706af-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="706af-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="706af-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="706af-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="706af-113">Click Save.</span></span>
6. <span data-ttu-id="706af-114">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="706af-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="706af-115">Щелкните "Торг. представитель".</span><span class="sxs-lookup"><span data-stu-id="706af-115">Click Sales rep.</span></span>
    * <span data-ttu-id="706af-116">Группа продаж может содержать несколько работников.</span><span class="sxs-lookup"><span data-stu-id="706af-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="706af-117">Комиссии можно разделить между работниками на основе того, как определена доля в комиссии.</span><span class="sxs-lookup"><span data-stu-id="706af-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="706af-118">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="706af-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="706af-119">В поле "Распределение комиссии" введите число.</span><span class="sxs-lookup"><span data-stu-id="706af-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="706af-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="706af-120">Click Save.</span></span>
11. <span data-ttu-id="706af-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="706af-121">Close the page.</span></span>
12. <span data-ttu-id="706af-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="706af-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="706af-123">Назначение группы продаж по умолчанию для работников</span><span class="sxs-lookup"><span data-stu-id="706af-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="706af-124">Перейдите в раздел "Retail и Commerce" > "Сотрудники" > "Работники".</span><span class="sxs-lookup"><span data-stu-id="706af-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="706af-125">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="706af-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="706af-126">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="706af-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="706af-127">Щелкните вкладку Commerce.</span><span class="sxs-lookup"><span data-stu-id="706af-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="706af-128">Работник может быть назначен группе продаж по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="706af-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="706af-129">Группа продаж по умолчанию будет автоматически добавлена в строки продаж в POS, если этот параметр включен в профиле функции для магазина.</span><span class="sxs-lookup"><span data-stu-id="706af-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="706af-130">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="706af-130">Click Edit.</span></span>
6. <span data-ttu-id="706af-131">В поле "Группа по умолчанию" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="706af-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="706af-132">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="706af-132">Click Save.</span></span>

