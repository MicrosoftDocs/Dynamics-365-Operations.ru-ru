---
title: Режимы и способы управления транспортировкой
description: В этой теме показано, как настроить способы и методы управления транспортировкой.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0d41d8665252a978962bf6a2e307dce3dad64a5b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233447"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="d97aa-103">Режимы и способы управления транспортировкой</span><span class="sxs-lookup"><span data-stu-id="d97aa-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d97aa-104">Режим управления транспортировкой — это тип транспортировки, который использует перевозчик для перевозки грузов, например мелкая отправка (LTL), транзитная норма (TL) или пакет.</span><span class="sxs-lookup"><span data-stu-id="d97aa-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="d97aa-105">Способ транспортировки — это форма транспортировки, которую использует перевозчик для перевозки грузов, например воздушным транспортом, наземным транспортом, морским транспортом или железнодорожным транспортом.</span><span class="sxs-lookup"><span data-stu-id="d97aa-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="d97aa-106">Режимы и способы транспортировки используются в нескольких контекстах.</span><span class="sxs-lookup"><span data-stu-id="d97aa-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="d97aa-107">В маршрутных планах используются только режимы, в то время как используются режимы и способы транспортировки при настройке перевозчиков и услуг перевозчиков.</span><span class="sxs-lookup"><span data-stu-id="d97aa-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="d97aa-108">Явного отношения или иерархии между режимами и способами транспортировки не существует.</span><span class="sxs-lookup"><span data-stu-id="d97aa-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="d97aa-109">Создание режима</span><span class="sxs-lookup"><span data-stu-id="d97aa-109">Create a mode</span></span>

<span data-ttu-id="d97aa-110">Чтобы создать режим, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d97aa-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="d97aa-111">Перейдите в раздел **Управление транспортировкой \> \> Настройка \> Перевозчики**.</span><span class="sxs-lookup"><span data-stu-id="d97aa-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="d97aa-112">Выберите **Создать** для создания нового режима.</span><span class="sxs-lookup"><span data-stu-id="d97aa-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="d97aa-113">Введите уникальный идентификатор и описательное имя режима.</span><span class="sxs-lookup"><span data-stu-id="d97aa-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="d97aa-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d97aa-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="d97aa-115">Создание способа транспортировки</span><span class="sxs-lookup"><span data-stu-id="d97aa-115">Create a transportation method</span></span>

<span data-ttu-id="d97aa-116">Чтобы создать способ транспортировки, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="d97aa-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="d97aa-117">Перейдите в раздел **Управление транспортировкой \> Настройка \> Перевозчики \> Способы транспортировки**.</span><span class="sxs-lookup"><span data-stu-id="d97aa-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="d97aa-118">Выберите **Создать**, чтобы создать новый способ транспортировки.</span><span class="sxs-lookup"><span data-stu-id="d97aa-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="d97aa-119">Введите уникальный идентификатор и описательное имя способа транспортировки.</span><span class="sxs-lookup"><span data-stu-id="d97aa-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="d97aa-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d97aa-120">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]