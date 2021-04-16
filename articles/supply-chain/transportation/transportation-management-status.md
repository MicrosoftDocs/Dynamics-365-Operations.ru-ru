---
title: Статусы управления транспортировкой
description: В этой теме объясняется, как создать статус транспортировки и сопоставить этот статус статусу перевозчика.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3a2b9e50dddf0f015cdd3f16d6d93fcc03d464d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807616"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="06536-103">Статусы управления транспортировкой</span><span class="sxs-lookup"><span data-stu-id="06536-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06536-104">Настройте коды шаблонов для статусов транспортировки, чтобы интерпретировать коды, предоставленные вашими перевозчиками.</span><span class="sxs-lookup"><span data-stu-id="06536-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="06536-105">Это позволяет интегрироваться с перевозчиками для предоставления статуса.</span><span class="sxs-lookup"><span data-stu-id="06536-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="06536-106">С помощью статуса транспортировки, введенного для кода статуса шаблона транспортировки, можно отслеживать статус загрузки, отгрузки или контейнера.</span><span class="sxs-lookup"><span data-stu-id="06536-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="06536-107">Конкретный статус транспортировки для загрузки, отгрузки или контейнера может быть обновлен только с помощью интеграции данных, а не вручную через интерфейс пользователя.</span><span class="sxs-lookup"><span data-stu-id="06536-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="06536-108">Создание статуса транспортировки</span><span class="sxs-lookup"><span data-stu-id="06536-108">Create a transportation status</span></span>

<span data-ttu-id="06536-109">Чтобы создать статус транспортировки, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="06536-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="06536-110">Перейдите в раздел **Управление транспортировкой \> Настройка \> Шаблоны статуса транспортировки**.</span><span class="sxs-lookup"><span data-stu-id="06536-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="06536-111">Выберите **Создать**, чтобы создать шаблон статуса транспортировки.</span><span class="sxs-lookup"><span data-stu-id="06536-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="06536-112">В поле **Шаблон статуса транспортировки** введите уникальный код для статуса транспортировки.</span><span class="sxs-lookup"><span data-stu-id="06536-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="06536-113">В поле **Тип транспортировки** выберите *Перевозчик* или *Центр* в качестве типа транспортировки.</span><span class="sxs-lookup"><span data-stu-id="06536-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="06536-114">Введите имя и статус транспортировки.</span><span class="sxs-lookup"><span data-stu-id="06536-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="06536-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="06536-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="06536-116">Сопоставление статуса транспортировки статусу перевозчика</span><span class="sxs-lookup"><span data-stu-id="06536-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="06536-117">Для сопоставления статуса транспортировки статусу перевозчика выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="06536-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="06536-118">Перейдите в раздел **Управление транспортировкой \> Настройка \> Перевозчики \> Статус транспортировки перевозчика**.</span><span class="sxs-lookup"><span data-stu-id="06536-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="06536-119">Выберите **Создать**, чтобы сопоставить код перевозчика с кодом шаблона статуса транспортировки.</span><span class="sxs-lookup"><span data-stu-id="06536-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="06536-120">Выберите уникальный код для перевозчика и услуги перевозчика.</span><span class="sxs-lookup"><span data-stu-id="06536-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="06536-121">Выберите код статуса транспортировки, который требуется сопоставить с кодом выбранного перевозчика.</span><span class="sxs-lookup"><span data-stu-id="06536-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="06536-122">Введите внешний код, используемый перевозчиком.</span><span class="sxs-lookup"><span data-stu-id="06536-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="06536-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="06536-123">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]