---
title: Создание профиля функциональности розничной торговли
description: В этом разделе описывается, как создать профиль функциональности розничной торговли в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9fb0fd63b11e55f2b153fc9c135f148a6e343057
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002851"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="4d92e-103">Создание профиля функциональности розничной торговли</span><span class="sxs-lookup"><span data-stu-id="4d92e-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4d92e-104">В этом разделе описывается, как создать профиль функциональности розничной торговли в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d92e-104">This topic describes how to create a retail functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4d92e-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="4d92e-105">Overview</span></span>

<span data-ttu-id="4d92e-106">Профиль функциональности розничной торговли предоставляет различные параметры, используемые для интернет-каналов.</span><span class="sxs-lookup"><span data-stu-id="4d92e-106">The retail functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="4d92e-107">Каждый канал розничной торговли должен указывать профиль функциональности розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="4d92e-107">Each retail channel must specify a retail functionality profile.</span></span>

## <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="4d92e-108">Создание профиля функциональности розничной торговли</span><span class="sxs-lookup"><span data-stu-id="4d92e-108">Create a retail functionality profile</span></span>

<span data-ttu-id="4d92e-109">Чтобы создать новый профиль функциональности розничной торговли, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4d92e-109">To create a retail functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="4d92e-110">В области переходов откройте окно **Модули \> Настройка канала \> Профили POS \> Профили функциональности**.</span><span class="sxs-lookup"><span data-stu-id="4d92e-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="4d92e-111">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4d92e-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4d92e-112">В поле **Профиль** введите код для профиля ("FN006" в примере изображения ниже).</span><span class="sxs-lookup"><span data-stu-id="4d92e-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="4d92e-113">В поле **Описание** введите значение ("Adventure Works Profile" в примере изображения ниже).</span><span class="sxs-lookup"><span data-stu-id="4d92e-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="4d92e-114">В разделе **Общие** выберите страну для языкового стандарта **ISO**.</span><span class="sxs-lookup"><span data-stu-id="4d92e-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="4d92e-115">В разделе **Общие** при необходимости измените другие настройки.</span><span class="sxs-lookup"><span data-stu-id="4d92e-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="4d92e-116">В разделе **Общие** выберите **Код профиля чеков** для чеков по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="4d92e-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="4d92e-117">В разделе **Функции** при необходимости измените настройки.</span><span class="sxs-lookup"><span data-stu-id="4d92e-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="4d92e-118">В разделе **Сумма** при необходимости измените настройки.</span><span class="sxs-lookup"><span data-stu-id="4d92e-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="4d92e-119">В разделе **Инфокоды** при необходимости измените настройки.</span><span class="sxs-lookup"><span data-stu-id="4d92e-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="4d92e-120">В разделе **Нумерация чеков** при необходимости измените настройки.</span><span class="sxs-lookup"><span data-stu-id="4d92e-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="4d92e-121">На следующем рисунке показан пример профиля функциональности розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="4d92e-121">The following image shows an example retail functionality profile.</span></span>
  
![Пример профиля функциональности розничной торговли](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="4d92e-123">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4d92e-123">Additional resources</span></span>

[<span data-ttu-id="4d92e-124">Инфокоды и группы инфокодов</span><span class="sxs-lookup"><span data-stu-id="4d92e-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="4d92e-125">Создание адресной книги</span><span class="sxs-lookup"><span data-stu-id="4d92e-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="4d92e-126">Обзор макета экрана</span><span class="sxs-lookup"><span data-stu-id="4d92e-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="4d92e-127">Настройка и установка Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="4d92e-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
