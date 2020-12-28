---
title: Создание профиля функциональности для онлайн-торговли
description: В этом разделе описывается, как создать профиль функциональности интернет-магазина в Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415360"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="3aa6f-103">Создание профиля функциональности для онлайн-торговли</span><span class="sxs-lookup"><span data-stu-id="3aa6f-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3aa6f-104">В этом разделе представлен обзор настройки профиля функциональности интернет-магазина для Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3aa6f-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3aa6f-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="3aa6f-105">Overview</span></span>

<span data-ttu-id="3aa6f-106">Профиль функциональности интернет-магазина предоставляет различные параметры, используемые для интернет-каналов.</span><span class="sxs-lookup"><span data-stu-id="3aa6f-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="3aa6f-107">Каждый интернет-канал должен указывать профиль функциональности интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="3aa6f-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="3aa6f-108">Создание профиля функциональности для онлайн-торговли</span><span class="sxs-lookup"><span data-stu-id="3aa6f-108">Create an online functionality profile</span></span>

<span data-ttu-id="3aa6f-109">Следующая процедура объясняет, как создать профиль функциональности интернет-магазина из приложения Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3aa6f-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="3aa6f-110">В области переходов откройте окно **Модули \> Настройка канала \> Настройка интернет-магазина \> Профили функциональности**.</span><span class="sxs-lookup"><span data-stu-id="3aa6f-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="3aa6f-111">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3aa6f-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3aa6f-112">В поле **Профиль** введите код профиля.</span><span class="sxs-lookup"><span data-stu-id="3aa6f-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="3aa6f-113">В поле **Описание** введите значение ("Adventure Works Profile" в примере изображения ниже).</span><span class="sxs-lookup"><span data-stu-id="3aa6f-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="3aa6f-114">В разделе **Функции** измените необходимые параметры **КОРЗИНА**, **РОЗНИЧНЫЕ КЛИЕНТЫ** или **ОФОРМЛЕНИЕ ЗАКАЗА**.</span><span class="sxs-lookup"><span data-stu-id="3aa6f-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="3aa6f-115">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3aa6f-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="3aa6f-116">На следующем рисунке показан пример профиля функциональности интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="3aa6f-116">The following image shows an example online functionality profile.</span></span>
  
![Пример профиля функциональности интернет-магазина](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="3aa6f-118">Функции</span><span class="sxs-lookup"><span data-stu-id="3aa6f-118">Functions</span></span>

- <span data-ttu-id="3aa6f-119">**Объединить продукты**: если этот флажок установлен, эта функция позволяет корзине обновлять количество при добавлении одной и той же номенклатуры несколько раз.</span><span class="sxs-lookup"><span data-stu-id="3aa6f-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="3aa6f-120">**Разрешить оформление заказа без платежей**: при включении эта функция обрабатывает сценарий, когда номенклатуры, добавленные в корзину, имеют цену 0,00 долларов США.</span><span class="sxs-lookup"><span data-stu-id="3aa6f-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="3aa6f-121">**Создание клиента в асинхронном режиме**: это устаревший параметр, применимый к каналам электронной коммерции сторонних производителей и неприменимый к сайту электронной коммерции Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3aa6f-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3aa6f-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3aa6f-122">Additional resources</span></span>

[<span data-ttu-id="3aa6f-123">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="3aa6f-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="3aa6f-124">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="3aa6f-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="3aa6f-125">Настройка интернет-канала</span><span class="sxs-lookup"><span data-stu-id="3aa6f-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="3aa6f-126">Настройка канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="3aa6f-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="3aa6f-127">Настройка канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="3aa6f-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
