--- 
title: "Создание профиля местонахождения"
description: "Каждое местоположение склада должно иметь связанный с ним профиль местоположения, описывающий свойства местоположения, например, допускает ли местоположение смешанные номенклатуры."
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 67ea9b0ac27a38b3f33523f5e4e1651316e3d2d2
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-location-profile"></a><span data-ttu-id="cb054-103">Создание профиля местонахождения</span><span class="sxs-lookup"><span data-stu-id="cb054-103">Create a location profile</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb054-104">Каждое местоположение склада должно иметь связанный с ним профиль местоположения, описывающий свойства местоположения, например, допускает ли местоположение смешанные номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="cb054-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="cb054-105">В этой процедуре мы создадим профиль для местоположения, который не требует управления грузоместом.</span><span class="sxs-lookup"><span data-stu-id="cb054-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="cb054-106">Мы разрешим смешанные номенклатуры и смешанные состояния запасов, а также разрешим цикличный подсчет.</span><span class="sxs-lookup"><span data-stu-id="cb054-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="cb054-107">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="cb054-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="cb054-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="cb054-108">Click New.</span></span>
2. <span data-ttu-id="cb054-109">В поле "Код профиля местонахождения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cb054-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="cb054-110">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cb054-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="cb054-111">В поле "Формат местонахождения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="cb054-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="cb054-112">В поле "Тип местоположения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="cb054-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="cb054-113">В поле "Код профиля управления доком" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="cb054-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="cb054-114">Выберите значение "Да" в поле "Разрешить смешанные номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="cb054-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="cb054-115">Выберите значение "Да" в поле "Разрешить смешанные статусы запасов".</span><span class="sxs-lookup"><span data-stu-id="cb054-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="cb054-116">Выберите "Да" в поле "Разрешить цикличный подсчет".</span><span class="sxs-lookup"><span data-stu-id="cb054-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="cb054-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="cb054-117">Click Save.</span></span>
11. <span data-ttu-id="cb054-118">Перейдите в раздел "Управление складом" > "Настройка" > "Склад" > "Профили местонахождения".</span><span class="sxs-lookup"><span data-stu-id="cb054-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>


