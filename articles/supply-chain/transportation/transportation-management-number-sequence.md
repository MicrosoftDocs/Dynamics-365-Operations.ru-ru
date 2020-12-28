---
title: Номерная серия управления транспортировкой
description: В этой теме описывается, как настроить номерные серии для управления транспортировкой.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2c3f087ac76412cd2dce93dcb31b796ce2cb3bc4
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2020
ms.locfileid: "4436502"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="40a4e-103">Номерная серия управления транспортировкой</span><span class="sxs-lookup"><span data-stu-id="40a4e-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40a4e-104">Страница **Номерные серии** в модуле управления транспортировкой используется для настройки различных номеров продуктов.</span><span class="sxs-lookup"><span data-stu-id="40a4e-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="40a4e-105">Номера продуктов используются перевозчиками для упорядочения и отслеживания хода выполнения каждой отгрузки.</span><span class="sxs-lookup"><span data-stu-id="40a4e-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="40a4e-106">Создание номерной серии для номера продукта</span><span class="sxs-lookup"><span data-stu-id="40a4e-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="40a4e-107">Чтобы создать номерную серию для номера продукта, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="40a4e-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="40a4e-108">Перейдите в раздел **Управление транспортировкой \> Настройка \> Перевозчики \> Номерные серии**.</span><span class="sxs-lookup"><span data-stu-id="40a4e-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="40a4e-109">Выберите **Создать** для создания номерной серии.</span><span class="sxs-lookup"><span data-stu-id="40a4e-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="40a4e-110">Введите уникальный код и описательное имя номерной серии.</span><span class="sxs-lookup"><span data-stu-id="40a4e-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="40a4e-111">В поле **Тип номерной серии** вариант *Номер продукта* является единственным.</span><span class="sxs-lookup"><span data-stu-id="40a4e-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="40a4e-112">В поле **Контрольный разряд** вариант *Контрольный разряд* является единственным вариантом и настраивается как универсальный механизм.</span><span class="sxs-lookup"><span data-stu-id="40a4e-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="40a4e-113">На экспресс-вкладке **Последовательность** введите информацию о последовательности.</span><span class="sxs-lookup"><span data-stu-id="40a4e-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="40a4e-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="40a4e-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="40a4e-115">Связывание номерной серии с перевозчиком</span><span class="sxs-lookup"><span data-stu-id="40a4e-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="40a4e-116">Чтобы связать номерную серию с перевозчиком, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="40a4e-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="40a4e-117">Перейдите в раздел **Управление транспортировкой \> Настройка \> Перевозчики \> Перевозчики, осуществляющий доставку**.</span><span class="sxs-lookup"><span data-stu-id="40a4e-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="40a4e-118">Выберите перевозчика.</span><span class="sxs-lookup"><span data-stu-id="40a4e-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="40a4e-119">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="40a4e-119">Select **Edit**.</span></span>
1. <span data-ttu-id="40a4e-120">На экспресс-вкладке **Обзор** выберите параметр в поле **Номерная серия продуктов**.</span><span class="sxs-lookup"><span data-stu-id="40a4e-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="40a4e-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="40a4e-121">Close the page.</span></span>
