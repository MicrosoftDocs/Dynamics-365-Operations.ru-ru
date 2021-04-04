---
title: Создание профиля функциональности розничной торговли
description: В этом разделе описывается, как создать профиль функциональности в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 14da5fd2b409790de2269036ccb941ffa6d3311c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478316"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="550c5-103">Создание профиля функциональности розничной торговли</span><span class="sxs-lookup"><span data-stu-id="550c5-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="550c5-104">В этом разделе описывается, как создать профиль функциональности в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="550c5-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="550c5-105">Профиль функциональности коммерции предоставляет различные параметры, используемые для интернет-каналов.</span><span class="sxs-lookup"><span data-stu-id="550c5-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="550c5-106">Каждый канал должен указывать профиль функциональности.</span><span class="sxs-lookup"><span data-stu-id="550c5-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="550c5-107">Создать профиль функциональности</span><span class="sxs-lookup"><span data-stu-id="550c5-107">Create a functionality profile</span></span>

<span data-ttu-id="550c5-108">Чтобы создать новый профиль функциональности, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="550c5-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="550c5-109">В области переходов откройте окно **Модули \> Настройка канала \> Профили POS \> Профили функциональности**.</span><span class="sxs-lookup"><span data-stu-id="550c5-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="550c5-110">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="550c5-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="550c5-111">В поле **Профиль** введите код для профиля ("FN006" в примере изображения ниже).</span><span class="sxs-lookup"><span data-stu-id="550c5-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="550c5-112">В поле **Описание** введите значение ("Adventure Works Profile" в примере изображения ниже).</span><span class="sxs-lookup"><span data-stu-id="550c5-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="550c5-113">В разделе **Общие** выберите страну для языкового стандарта **ISO**.</span><span class="sxs-lookup"><span data-stu-id="550c5-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="550c5-114">В разделе **Общие** при необходимости измените другие настройки.</span><span class="sxs-lookup"><span data-stu-id="550c5-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="550c5-115">В разделе **Общие** выберите **Код профиля чеков** для чеков по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="550c5-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="550c5-116">В разделе **Функции** при необходимости измените настройки.</span><span class="sxs-lookup"><span data-stu-id="550c5-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="550c5-117">В разделе **Сумма** при необходимости измените настройки.</span><span class="sxs-lookup"><span data-stu-id="550c5-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="550c5-118">В разделе **Инфокоды** при необходимости измените настройки.</span><span class="sxs-lookup"><span data-stu-id="550c5-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="550c5-119">В разделе **Нумерация чеков** при необходимости измените настройки.</span><span class="sxs-lookup"><span data-stu-id="550c5-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="550c5-120">На следующем рисунке показан пример профиля функциональности.</span><span class="sxs-lookup"><span data-stu-id="550c5-120">The following image shows an example functionality profile.</span></span>
  
![Пример профиля функциональности](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="550c5-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="550c5-122">Additional resources</span></span>

[<span data-ttu-id="550c5-123">Инфокоды и группы инфокодов</span><span class="sxs-lookup"><span data-stu-id="550c5-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="550c5-124">Создание адресной книги</span><span class="sxs-lookup"><span data-stu-id="550c5-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="550c5-125">Обзор макета экрана</span><span class="sxs-lookup"><span data-stu-id="550c5-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="550c5-126">Настройка и установка Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="550c5-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
