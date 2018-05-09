---
title: "Получение грузоместа со смешанными номенклатурами"
description: "В этом разделе описывается использование получения грузоместа со смешанными номенклатурами для регистрации и создания работы для нескольких номенклатур с помощью мобильного устройства."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0088290a05deb96f597c9f24209bb73a6e7918e9
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="a8e8e-103">Получение грузоместа со смешанными номенклатурами</span><span class="sxs-lookup"><span data-stu-id="a8e8e-103">Mixed license plate receiving</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8e8e-104">Получение грузоместа со смешанными номенклатурами позволяет создавать грузоместо с несколькими номенклатурами перед их регистрацией и созданием размещения.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="a8e8e-105">Грузоместо с несколькими номенклатурами нет необходимости разделять в доке приемки для регистрации каждой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="a8e8e-106">При использовании потока, относящегося к номенклатуре, для идентификации строк документа-источника можно сканировать штрих-код на элементе управления номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="a8e8e-107">Если на штрих-коде указано количество и настроена единица измерения, номенклатура и количество будут автоматически добавлены в грузоместо со смешанными номенклатурами и произойдет возврат на экран для сканирования другой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="a8e8e-108">Это позволяет быстро просканировать все номенклатуры без подтверждения на каждом шаге.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="a8e8e-109">В потоке получения грузоместа со смешанными номенклатурами можно отобразить список номенклатур, которые уже просканированы для грузоместа, и откуда можно изменить или исправить количество номенклатур.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="a8e8e-110">Где это применяется</span><span class="sxs-lookup"><span data-stu-id="a8e8e-110">Where it applies</span></span>

<span data-ttu-id="a8e8e-111">Получение грузоместа со смешанными номенклатурами является мобильным устройством, получающим поток для регистрации и создания работы для нескольких строк или номенклатур одновременно.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="a8e8e-112">Это полезно при получении входящих грузомест с несколькими номенклатурами.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="a8e8e-113">Настройка получения грузоместа со смешанными номенклатурами</span><span class="sxs-lookup"><span data-stu-id="a8e8e-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="a8e8e-114">Получение грузоместа со смешанными номенклатурами настраивается как элемент меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="a8e8e-115">Необходимо создать новый элемент меню с режимом работы, где не используется текущая работа, и применяется один из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="a8e8e-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="a8e8e-116">Получение грузоместа со смешанными номенклатурами</span><span class="sxs-lookup"><span data-stu-id="a8e8e-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="a8e8e-117">Получение и складирование грузоместа со смешанными номенклатурами</span><span class="sxs-lookup"><span data-stu-id="a8e8e-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="a8e8e-118">Параметры идентификации строк документа-источника — это номенклатура заказа на покупку, строка заказа на покупку, заказ на возврат, номенклатура заказа на перемещение и строка заказа на перемещение.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="a8e8e-119">Эти параметры могут изменить порядок получения в одном грузоместе.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="a8e8e-120">Последний параметр относится к номенклатуре загрузки.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-120">The last option is by load item.</span></span> <span data-ttu-id="a8e8e-121">Можно добавить несколько номенклатур для грузоместа, но нельзя переключаться между несколькими загрузками.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>

