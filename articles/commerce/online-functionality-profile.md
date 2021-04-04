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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: cb9d78a945132c913dcb8a5d5b41eaacd1a6db3b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477740"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="f4b4c-103">Создание профиля функциональности для онлайн-торговли</span><span class="sxs-lookup"><span data-stu-id="f4b4c-103">Create an online functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f4b4c-104">В этом разделе представлен обзор настройки профиля функциональности интернет-магазина для Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f4b4c-105">Профиль функциональности интернет-магазина предоставляет различные параметры, используемые для интернет-каналов.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-105">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="f4b4c-106">Каждый интернет-канал должен указывать профиль функциональности интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-106">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="f4b4c-107">Создание профиля функциональности для онлайн-торговли</span><span class="sxs-lookup"><span data-stu-id="f4b4c-107">Create an online functionality profile</span></span>

<span data-ttu-id="f4b4c-108">Следующая процедура объясняет, как создать профиль функциональности интернет-магазина из приложения Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-108">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="f4b4c-109">В области переходов откройте окно **Модули \> Настройка канала \> Настройка интернет-магазина \> Профили функциональности**.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-109">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="f4b4c-110">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f4b4c-111">В поле **Профиль** введите код профиля.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-111">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="f4b4c-112">В поле **Описание** введите значение ("Adventure Works Profile" в примере изображения ниже).</span><span class="sxs-lookup"><span data-stu-id="f4b4c-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="f4b4c-113">В разделе **Функции** измените необходимые параметры **КОРЗИНА**, **РОЗНИЧНЫЕ КЛИЕНТЫ** или **ОФОРМЛЕНИЕ ЗАКАЗА**.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-113">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="f4b4c-114">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-114">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f4b4c-115">На следующем рисунке показан пример профиля функциональности интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-115">The following image shows an example online functionality profile.</span></span>
  
![Пример профиля функциональности интернет-магазина](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="f4b4c-117">Функции</span><span class="sxs-lookup"><span data-stu-id="f4b4c-117">Functions</span></span>

- <span data-ttu-id="f4b4c-118">**Объединить продукты**: если этот флажок установлен, эта функция позволяет корзине обновлять количество при добавлении одной и той же номенклатуры несколько раз.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-118">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="f4b4c-119">**Разрешить оформление заказа без платежей**: при включении эта функция обрабатывает сценарий, когда номенклатуры, добавленные в корзину, имеют цену 0,00 долларов США.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-119">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="f4b4c-120">**Создание клиента в асинхронном режиме**: это устаревший параметр, применимый к каналам электронной коммерции сторонних производителей и неприменимый к сайту электронной коммерции Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-120">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4b4c-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f4b4c-121">Additional resources</span></span>

[<span data-ttu-id="f4b4c-122">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="f4b4c-122">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="f4b4c-123">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="f4b4c-123">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="f4b4c-124">Настройка интернет-канала</span><span class="sxs-lookup"><span data-stu-id="f4b4c-124">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="f4b4c-125">Настройка канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="f4b4c-125">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="f4b4c-126">Настройка канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="f4b4c-126">Set up a call center channel</span></span>](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
