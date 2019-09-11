---
title: Создание профиля ячейки
description: В этом разделе описывается, как создать профиль местонахождения в Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46aa1001c21ae39c158062444303ca02c0f41a45
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866987"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="46614-103">Создание профиля ячейки</span><span class="sxs-lookup"><span data-stu-id="46614-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46614-104">В этом разделе описывается, как создать профиль местонахождения в Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="46614-104">This topic explains how to create a location profile in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="46614-105">Каждое местоположение склада должно иметь связанный с ним профиль местоположения, описывающий свойства местоположения, например, допускает ли местоположение смешанные номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="46614-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="46614-106">В этой процедуре мы создадим профиль для местоположения, который не требует управления грузоместом.</span><span class="sxs-lookup"><span data-stu-id="46614-106">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="46614-107">Мы разрешим смешанные номенклатуры и смешанные состояния запасов, а также разрешим цикличный подсчет.</span><span class="sxs-lookup"><span data-stu-id="46614-107">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="46614-108">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="46614-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="46614-109">В области перехода выберите **Модули > Управление складом > Настройка > Склад > Профили местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="46614-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="46614-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="46614-110">Select **New**.</span></span>
3. <span data-ttu-id="46614-111">В поле **Код профиля местонахождения** введите значение.</span><span class="sxs-lookup"><span data-stu-id="46614-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="46614-112">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="46614-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="46614-113">В поле **Формат местонахождения** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="46614-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="46614-114">В поле **Тип местоположения** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="46614-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="46614-115">В поле **Код профиля управления доком** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="46614-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="46614-116">Выберите значение **Да** в поле **Разрешить смешанные номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="46614-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="46614-117">Выберите значение **Да** в поле **Разрешить смешанные статусы запасов**.</span><span class="sxs-lookup"><span data-stu-id="46614-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="46614-118">Выберите **Да** в поле **Разрешить цикличный подсчет**.</span><span class="sxs-lookup"><span data-stu-id="46614-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="46614-119">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="46614-119">Select **Save**.</span></span>

