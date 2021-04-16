---
title: Настройка дополнительных расходов и справочников дополнений для узла
description: В этой процедуре показано, как создать справочник дополнений для узла и, используя этот справочник, создать дополнительные расходы для узла.
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f4c0d3af96e6ef6735b01165a49c1450b3b633b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837576"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="328fd-103">Настройка дополнительных расходов и справочников дополнений для узла</span><span class="sxs-lookup"><span data-stu-id="328fd-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="328fd-104">В этой процедуре показано, как создать справочник дополнений для узла и, используя этот справочник, создать дополнительные расходы для узла.</span><span class="sxs-lookup"><span data-stu-id="328fd-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="328fd-105">В процедуре используется набор данных USMF.</span><span class="sxs-lookup"><span data-stu-id="328fd-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="328fd-106">Обычно это настраивается координатором транспортировки.</span><span class="sxs-lookup"><span data-stu-id="328fd-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="328fd-107">Настройка шаблона узла</span><span class="sxs-lookup"><span data-stu-id="328fd-107">Set up a hub master</span></span>
1. <span data-ttu-id="328fd-108">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Расчет ставок" > "Шаблоны дополнения".</span><span class="sxs-lookup"><span data-stu-id="328fd-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="328fd-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="328fd-109">Click New.</span></span>
3. <span data-ttu-id="328fd-110">В поле "Шаблон дополнения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="328fd-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="328fd-111">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="328fd-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="328fd-112">В поле "Тип дополнения" выберите "Узел".</span><span class="sxs-lookup"><span data-stu-id="328fd-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="328fd-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="328fd-113">Click Save.</span></span>
7. <span data-ttu-id="328fd-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="328fd-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="328fd-115">Настройка дополнительных расходов для узла</span><span class="sxs-lookup"><span data-stu-id="328fd-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="328fd-116">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Расчет ставок" > "Дополнительные расходы узла".</span><span class="sxs-lookup"><span data-stu-id="328fd-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="328fd-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="328fd-117">Click New.</span></span>
3. <span data-ttu-id="328fd-118">В поле "Код дополнительного узла" введите значение.</span><span class="sxs-lookup"><span data-stu-id="328fd-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="328fd-119">В поле "Узел" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="328fd-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="328fd-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="328fd-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="328fd-121">В поле "Позиция узла" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="328fd-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="328fd-122">Расходы можно создавать как вывоз или разгрузку.</span><span class="sxs-lookup"><span data-stu-id="328fd-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="328fd-123">В зависимости от выбранного варианта расходы будут применяться к соответствующему сегменту транспортировки на маршруте.</span><span class="sxs-lookup"><span data-stu-id="328fd-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="328fd-124">В поле "Шаблон дополнения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="328fd-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="328fd-125">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="328fd-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="328fd-126">Выберите только что созданный справочник.</span><span class="sxs-lookup"><span data-stu-id="328fd-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="328fd-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="328fd-127">Click Save.</span></span>
10. <span data-ttu-id="328fd-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="328fd-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]