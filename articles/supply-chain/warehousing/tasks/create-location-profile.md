---
title: Создание профиля местонахождения
description: Каждое местоположение склада должно иметь связанный с ним профиль местоположения, описывающий свойства местоположения, например, допускает ли местоположение смешанные номенклатуры.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bc7705b7db46af8fbe8bf9e78a878a53249b452
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560917"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="d233a-103">Создание профиля местонахождения</span><span class="sxs-lookup"><span data-stu-id="d233a-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d233a-104">Каждое местоположение склада должно иметь связанный с ним профиль местоположения, описывающий свойства местоположения, например, допускает ли местоположение смешанные номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="d233a-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="d233a-105">В этой процедуре мы создадим профиль для местоположения, который не требует управления грузоместом.</span><span class="sxs-lookup"><span data-stu-id="d233a-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="d233a-106">Мы разрешим смешанные номенклатуры и смешанные состояния запасов, а также разрешим цикличный подсчет.</span><span class="sxs-lookup"><span data-stu-id="d233a-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="d233a-107">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="d233a-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="d233a-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d233a-108">Click New.</span></span>
2. <span data-ttu-id="d233a-109">В поле "Код профиля местонахождения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d233a-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="d233a-110">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d233a-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d233a-111">В поле "Формат местонахождения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d233a-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="d233a-112">В поле "Тип местоположения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d233a-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="d233a-113">В поле "Код профиля управления доком" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d233a-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="d233a-114">Выберите значение "Да" в поле "Разрешить смешанные номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="d233a-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="d233a-115">Выберите значение "Да" в поле "Разрешить смешанные статусы запасов".</span><span class="sxs-lookup"><span data-stu-id="d233a-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="d233a-116">Выберите "Да" в поле "Разрешить цикличный подсчет".</span><span class="sxs-lookup"><span data-stu-id="d233a-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="d233a-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d233a-117">Click Save.</span></span>
11. <span data-ttu-id="d233a-118">Перейдите в раздел "Управление складом" > "Настройка" > "Склад" > "Профили местонахождения".</span><span class="sxs-lookup"><span data-stu-id="d233a-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

