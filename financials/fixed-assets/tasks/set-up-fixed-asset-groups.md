--- 
title: "Настройка групп основных активов"
description: "В этой процедуре показано, как создать новую группу основных средств."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
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
ms.openlocfilehash: c44ce1219c0fc860d621aa32c8eec7c5d640fa03
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="92616-103">Настройка групп основных активов</span><span class="sxs-lookup"><span data-stu-id="92616-103">Set up fixed asset groups</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92616-104">В этой процедуре показано, как создать новую группу основных средств.</span><span class="sxs-lookup"><span data-stu-id="92616-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="92616-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="92616-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="92616-106">Перейдите в раздел "Основные средства" > "Настройка" > "Группы ОС".</span><span class="sxs-lookup"><span data-stu-id="92616-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="92616-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="92616-107">Click New.</span></span>
3. <span data-ttu-id="92616-108">В поле "Группа ОС" введите значение.</span><span class="sxs-lookup"><span data-stu-id="92616-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="92616-109">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="92616-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="92616-110">Параметры "Автонумерация ОС" и "Код номерной серии" в группе основных средств переопределяют настройки в параметрах основных средств.</span><span class="sxs-lookup"><span data-stu-id="92616-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="92616-111">Значения можно изменить здесь, если основные средства в этой группе основных средств имеют нумерацию, отличную от других групп.</span><span class="sxs-lookup"><span data-stu-id="92616-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="92616-112">Нажмите "Книги".</span><span class="sxs-lookup"><span data-stu-id="92616-112">Click Books.</span></span>
6. <span data-ttu-id="92616-113">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="92616-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="92616-114">Если в поле "Расчет амортизации" задано значение "Да", журнал основных средств будет включен в предложения по амортизации.</span><span class="sxs-lookup"><span data-stu-id="92616-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="92616-115">Если в поле "Расчет амортизации" задано значение "Нет", основное средство не будет амортизироваться автоматически.</span><span class="sxs-lookup"><span data-stu-id="92616-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="92616-116">Задайте срок службы основного средства в годах.</span><span class="sxs-lookup"><span data-stu-id="92616-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="92616-117">Обратите внимание, что значение поля "Периоды амортизации" рассчитывается после настройки срока службы.</span><span class="sxs-lookup"><span data-stu-id="92616-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="92616-118">В поле "Соглашение по амортизации" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="92616-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="92616-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="92616-119">Close the page.</span></span>


