--- 
title: "Выбытие основного средства с использованием накладной с произвольным текстом"
description: "Эта процедура показывает, как приобрести основное средство с помощью предложения по приобретению в журнале основных средств."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
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
ms.openlocfilehash: 24c7721a1e5467e98e6c4d245f1d8e24a973f5aa
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="dispose-of-a-fixed-asset-using-a-free-text-invoice"></a><span data-ttu-id="2367e-103">Выбытие основного средства с использованием накладной с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="2367e-103">Dispose of a fixed asset using a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2367e-104">Эта процедура показывает, как приобрести основное средство с помощью предложения по приобретению в журнале основных средств.</span><span class="sxs-lookup"><span data-stu-id="2367e-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="2367e-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="2367e-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="2367e-106">Перейдите в раздел "Основные средства" > "Записи в журнале" > "Журнал основных средств".</span><span class="sxs-lookup"><span data-stu-id="2367e-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="2367e-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2367e-107">Click New.</span></span>
3. <span data-ttu-id="2367e-108">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2367e-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="2367e-109">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="2367e-109">Click Lines.</span></span>
5. <span data-ttu-id="2367e-110">Щелкните "Предложения".</span><span class="sxs-lookup"><span data-stu-id="2367e-110">Click Proposals.</span></span>
6. <span data-ttu-id="2367e-111">Щелкните "Предложение по приобретению".</span><span class="sxs-lookup"><span data-stu-id="2367e-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="2367e-112">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="2367e-112">Click Filter.</span></span>
8. <span data-ttu-id="2367e-113">Щелкните "Сброс", чтобы сбросить вне предыдущие значения.</span><span class="sxs-lookup"><span data-stu-id="2367e-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="2367e-114">Выберите строку "Инв. номер ОС".</span><span class="sxs-lookup"><span data-stu-id="2367e-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="2367e-115">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2367e-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="2367e-116">Настройте оставшиеся критерии для основных средств, которые необходимо приобрести с этим предложением.</span><span class="sxs-lookup"><span data-stu-id="2367e-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="2367e-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2367e-117">Click OK.</span></span>
12. <span data-ttu-id="2367e-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2367e-118">Click OK.</span></span>
    * <span data-ttu-id="2367e-119">Проверьте созданные строки проводки.</span><span class="sxs-lookup"><span data-stu-id="2367e-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="2367e-120">Только основные средства, для которых заданы параметры даты приобретения и цены приобретения в книге, будут включены в предложение по приобретению.</span><span class="sxs-lookup"><span data-stu-id="2367e-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="2367e-121">Перейдите на вкладку "Книги".</span><span class="sxs-lookup"><span data-stu-id="2367e-121">Click the Books tab.</span></span>
14. <span data-ttu-id="2367e-122">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="2367e-122">Click Post.</span></span>


