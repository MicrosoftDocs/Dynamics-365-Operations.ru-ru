---
title: Настройка перераспределения номенклатур для недоукомплектованности
description: На этой процедуры показано, как разрешить работникам склада быстро искать альтернативные местоположения, если нет достаточного количества запасов в ячейке, к которой они были направлены.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf56a0811c4793ee2e3eaf78c8696c3c29e984c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560845"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="22c33-103">Настройка перераспределения номенклатур для недоукомплектованности</span><span class="sxs-lookup"><span data-stu-id="22c33-103">Set up short picking item reallocation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22c33-104">На этой процедуры показано, как разрешить работникам склада быстро искать альтернативные местоположения, если нет достаточного количества запасов в ячейке, к которой они были направлены.</span><span class="sxs-lookup"><span data-stu-id="22c33-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="22c33-105">Можно использовать автоматический процесс перераспределения, который использует директивы местоположения, чтобы получить товары, если они доступны в другом месте.</span><span class="sxs-lookup"><span data-stu-id="22c33-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="22c33-106">Кроме того, если используется перераспределение вручную, список местоположений с доступным количеством отображается на мобильном устройстве, позволяя работнику склада выбрать, из какого местоположения использовать запасы.</span><span class="sxs-lookup"><span data-stu-id="22c33-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="22c33-107">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="22c33-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="22c33-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="22c33-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="22c33-109">Настройка исключений работ</span><span class="sxs-lookup"><span data-stu-id="22c33-109">Set up work exceptions</span></span>
1. <span data-ttu-id="22c33-110">Перейдите в раздел "Управление складом" > "Настройка" > "Работа" > "Исключения работы".</span><span class="sxs-lookup"><span data-stu-id="22c33-110">Go to Warehouse management > Setup > Work > Work exceptions.</span></span>
2. <span data-ttu-id="22c33-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="22c33-111">Click New.</span></span>
    * <span data-ttu-id="22c33-112">Можно определить несколько исключений работы с различными политиками переразмещения номенклатур, чтобы рабочий склада мог выбрать одно из них на основе потребностей отгрузки, которую он обрабатывает.</span><span class="sxs-lookup"><span data-stu-id="22c33-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="22c33-113">В поле "Код исключения работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="22c33-113">In the Work exception code field, type a value.</span></span>
    * <span data-ttu-id="22c33-114">Задайте название исключения работы для указания его назначения.</span><span class="sxs-lookup"><span data-stu-id="22c33-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="22c33-115">Например, "Руководство по недостаточной комплектации".</span><span class="sxs-lookup"><span data-stu-id="22c33-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="22c33-116">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="22c33-116">In the Description field, type a value.</span></span>
5. <span data-ttu-id="22c33-117">В поле "Тип исключения" выберите "Недоукомплектовать".</span><span class="sxs-lookup"><span data-stu-id="22c33-117">In the Exception type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="22c33-118">Установите флажок "Корректировка складских запасов".</span><span class="sxs-lookup"><span data-stu-id="22c33-118">Select the Adjust inventory check box.</span></span>
    * <span data-ttu-id="22c33-119">Этот параметр означает, что запасы будут автоматически скорректированы на 0 в местоположении с недостаточной комплектацией.</span><span class="sxs-lookup"><span data-stu-id="22c33-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="22c33-120">В поле "Код типа корректировки по умолчанию" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="22c33-120">In the Default adjustment type code field, enter or select a value.</span></span>
    * <span data-ttu-id="22c33-121">Например, в USMF можно выбрать "Удалить Res Adj Out".</span><span class="sxs-lookup"><span data-stu-id="22c33-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="22c33-122">В поле "Перераспределение номенклатур" выберите "Вручную".</span><span class="sxs-lookup"><span data-stu-id="22c33-122">In the Item reallocation field, select 'Manual'.</span></span>
    * <span data-ttu-id="22c33-123">Если выбрано "Вручную" или "Автоматически и вручную", то работнику склада должно быть разрешено выполнять переразмещение вручную.</span><span class="sxs-lookup"><span data-stu-id="22c33-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="22c33-124">Настройте работника для использования ручного перераспределения номенклатуры</span><span class="sxs-lookup"><span data-stu-id="22c33-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="22c33-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="22c33-125">Close the page.</span></span>
2. <span data-ttu-id="22c33-126">Перейдите в раздел "Управление складом" > "Настройка" > "Рабочий".</span><span class="sxs-lookup"><span data-stu-id="22c33-126">Go to Warehouse management > Setup > Worker.</span></span>
3. <span data-ttu-id="22c33-127">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="22c33-127">Click Edit.</span></span>
4. <span data-ttu-id="22c33-128">В списке выберите работника 24.</span><span class="sxs-lookup"><span data-stu-id="22c33-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="22c33-129">Разверните раздел "Работа".</span><span class="sxs-lookup"><span data-stu-id="22c33-129">Expand the Work section.</span></span>
6. <span data-ttu-id="22c33-130">Выберите "Да" в поле "Разрешить перераспределение номенклатур вручную".</span><span class="sxs-lookup"><span data-stu-id="22c33-130">Select Yes in the Allow manual item reallocation field.</span></span>

