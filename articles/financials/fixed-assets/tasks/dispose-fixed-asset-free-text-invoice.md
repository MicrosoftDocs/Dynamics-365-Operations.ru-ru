--- 
title: "Выбытие основного средства с использованием накладной с произвольным текстом"
description: "Эта процедура показывает, как приобрести основное средство с помощью предложения по приобретению в журнале основных средств."
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 742c7d732ff121bff841ac0149b15bef5a94c756
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="dispose-of-a-fixed-asset-using-a-free-text-invoice"></a><span data-ttu-id="54ebe-103">Выбытие основного средства с использованием накладной с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="54ebe-103">Dispose of a fixed asset using a free text invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54ebe-104">Эта процедура показывает, как приобрести основное средство с помощью предложения по приобретению в журнале основных средств.</span><span class="sxs-lookup"><span data-stu-id="54ebe-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="54ebe-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="54ebe-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="54ebe-106">Перейдите в раздел "Основные средства" > "Записи в журнале" > "Журнал основных средств".</span><span class="sxs-lookup"><span data-stu-id="54ebe-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="54ebe-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="54ebe-107">Click New.</span></span>
3. <span data-ttu-id="54ebe-108">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="54ebe-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="54ebe-109">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="54ebe-109">Click Lines.</span></span>
5. <span data-ttu-id="54ebe-110">Щелкните "Предложения".</span><span class="sxs-lookup"><span data-stu-id="54ebe-110">Click Proposals.</span></span>
6. <span data-ttu-id="54ebe-111">Щелкните "Предложение по приобретению".</span><span class="sxs-lookup"><span data-stu-id="54ebe-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="54ebe-112">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="54ebe-112">Click Filter.</span></span>
8. <span data-ttu-id="54ebe-113">Щелкните "Сброс", чтобы сбросить вне предыдущие значения.</span><span class="sxs-lookup"><span data-stu-id="54ebe-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="54ebe-114">Выберите строку "Инв. номер ОС".</span><span class="sxs-lookup"><span data-stu-id="54ebe-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="54ebe-115">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="54ebe-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="54ebe-116">Настройте оставшиеся критерии для основных средств, которые необходимо приобрести с этим предложением.</span><span class="sxs-lookup"><span data-stu-id="54ebe-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="54ebe-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="54ebe-117">Click OK.</span></span>
12. <span data-ttu-id="54ebe-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="54ebe-118">Click OK.</span></span>
    * <span data-ttu-id="54ebe-119">Проверьте созданные строки проводки.</span><span class="sxs-lookup"><span data-stu-id="54ebe-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="54ebe-120">Только основные средства, для которых заданы параметры даты приобретения и цены приобретения в книге, будут включены в предложение по приобретению.</span><span class="sxs-lookup"><span data-stu-id="54ebe-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="54ebe-121">Перейдите на вкладку "Книги".</span><span class="sxs-lookup"><span data-stu-id="54ebe-121">Click the Books tab.</span></span>
14. <span data-ttu-id="54ebe-122">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="54ebe-122">Click Post.</span></span>


