---
title: Статусы управления транспортировкой
description: В этой теме объясняется, как создать статус транспортировки и сопоставить этот статус статусу перевозчика.
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
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9d3ed4b73f909b50e97c971a37c548c8c4a9e620
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006474"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="3a99d-103">Статусы управления транспортировкой</span><span class="sxs-lookup"><span data-stu-id="3a99d-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a99d-104">Настройте коды шаблонов для статусов транспортировки, чтобы интерпретировать коды, предоставленные вашими перевозчиками.</span><span class="sxs-lookup"><span data-stu-id="3a99d-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="3a99d-105">Это позволяет интегрироваться с перевозчиками для предоставления статуса.</span><span class="sxs-lookup"><span data-stu-id="3a99d-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="3a99d-106">С помощью статуса транспортировки, введенного для кода статуса шаблона транспортировки, можно отслеживать статус загрузки, отгрузки или контейнера.</span><span class="sxs-lookup"><span data-stu-id="3a99d-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="3a99d-107">Конкретный статус транспортировки для загрузки, отгрузки или контейнера может быть обновлен только с помощью интеграции данных, а не вручную через интерфейс пользователя.</span><span class="sxs-lookup"><span data-stu-id="3a99d-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="3a99d-108">Создание статуса транспортировки</span><span class="sxs-lookup"><span data-stu-id="3a99d-108">Create a transportation status</span></span>

<span data-ttu-id="3a99d-109">Чтобы создать статус транспортировки, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="3a99d-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="3a99d-110">Перейдите в раздел **Управление транспортировкой \> Настройка \> Шаблоны статуса транспортировки**.</span><span class="sxs-lookup"><span data-stu-id="3a99d-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="3a99d-111">Выберите **Создать**, чтобы создать шаблон статуса транспортировки.</span><span class="sxs-lookup"><span data-stu-id="3a99d-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="3a99d-112">В поле **Шаблон статуса транспортировки** введите уникальный код для статуса транспортировки.</span><span class="sxs-lookup"><span data-stu-id="3a99d-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="3a99d-113">В поле **Тип транспортировки** выберите *Перевозчик* или *Центр* в качестве типа транспортировки.</span><span class="sxs-lookup"><span data-stu-id="3a99d-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="3a99d-114">Введите имя и статус транспортировки.</span><span class="sxs-lookup"><span data-stu-id="3a99d-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="3a99d-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a99d-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="3a99d-116">Сопоставление статуса транспортировки статусу перевозчика</span><span class="sxs-lookup"><span data-stu-id="3a99d-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="3a99d-117">Для сопоставления статуса транспортировки статусу перевозчика выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="3a99d-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="3a99d-118">Перейдите в раздел **Управление транспортировкой \> Настройка \> Перевозчики \> Статус транспортировки перевозчика**.</span><span class="sxs-lookup"><span data-stu-id="3a99d-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="3a99d-119">Выберите **Создать**, чтобы сопоставить код перевозчика с кодом шаблона статуса транспортировки.</span><span class="sxs-lookup"><span data-stu-id="3a99d-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="3a99d-120">Выберите уникальный код для перевозчика и услуги перевозчика.</span><span class="sxs-lookup"><span data-stu-id="3a99d-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="3a99d-121">Выберите код статуса транспортировки, который требуется сопоставить с кодом выбранного перевозчика.</span><span class="sxs-lookup"><span data-stu-id="3a99d-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="3a99d-122">Введите внешний код, используемый перевозчиком.</span><span class="sxs-lookup"><span data-stu-id="3a99d-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="3a99d-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a99d-123">Close the page.</span></span>
