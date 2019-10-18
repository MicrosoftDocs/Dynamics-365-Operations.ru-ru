---
title: Настройка групп ОС
description: В этой теме показано, как создать новую группу основных средств.
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 246502f66c0cfcd4b4ed3c4b9f2ae616e71a1c50
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186885"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="24527-103">Настройка групп ОС</span><span class="sxs-lookup"><span data-stu-id="24527-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="24527-104">В этой теме показано, как создать новую группу основных средств.</span><span class="sxs-lookup"><span data-stu-id="24527-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="24527-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="24527-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="24527-106">В области перехода, перейдите к **Модули > Основные средства > Настройка > Группы ОС**.</span><span class="sxs-lookup"><span data-stu-id="24527-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="24527-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="24527-107">Select **New**.</span></span>
3. <span data-ttu-id="24527-108">В поле **Группа ОС** введите значение.</span><span class="sxs-lookup"><span data-stu-id="24527-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="24527-109">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="24527-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="24527-110">Параметры "Автонумерация ОС" и "Код номерной серии" в группе **Основное средство** переопределяют настройки в параметрах основных средств.</span><span class="sxs-lookup"><span data-stu-id="24527-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="24527-111">Значения можно изменить здесь, если основные средства в этой группе основных средств имеют нумерацию, отличную от других групп.</span><span class="sxs-lookup"><span data-stu-id="24527-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="24527-112">Выберите **Книги**.</span><span class="sxs-lookup"><span data-stu-id="24527-112">Select **Books**.</span></span>
6. <span data-ttu-id="24527-113">В поле **Книга** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="24527-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="24527-114">Если в поле **Расчет амортизации** задано значение **Да**, журнал основных средств будет включен в предложения по амортизации.</span><span class="sxs-lookup"><span data-stu-id="24527-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="24527-115">Если в поле **Расчет амортизации** задано значение **Нет**, основное средство не будет амортизироваться автоматически.</span><span class="sxs-lookup"><span data-stu-id="24527-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="24527-116">Задайте срок службы основного средства в годах.</span><span class="sxs-lookup"><span data-stu-id="24527-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="24527-117">Обратите внимание, что значение поля **Периоды амортизации** рассчитывается после настройки срока службы.</span><span class="sxs-lookup"><span data-stu-id="24527-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="24527-118">В поле **Соглашение по амортизации** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="24527-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="24527-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="24527-119">Close the page.</span></span>

