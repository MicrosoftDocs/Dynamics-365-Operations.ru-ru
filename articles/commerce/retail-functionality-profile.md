---
title: Создание профиля функциональности розничной торговли
description: В этом разделе описывается, как создать профиль функциональности в Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b8d481597485775796290f61de19ef7682cb9f43
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792006"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="0c154-103">Создание профиля функциональности розничной торговли</span><span class="sxs-lookup"><span data-stu-id="0c154-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c154-104">В этом разделе описывается, как создать профиль функциональности в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0c154-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0c154-105">Профиль функциональности коммерции предоставляет различные параметры, используемые для интернет-каналов.</span><span class="sxs-lookup"><span data-stu-id="0c154-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="0c154-106">Каждый канал должен указывать профиль функциональности.</span><span class="sxs-lookup"><span data-stu-id="0c154-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="0c154-107">Создать профиль функциональности</span><span class="sxs-lookup"><span data-stu-id="0c154-107">Create a functionality profile</span></span>

<span data-ttu-id="0c154-108">Чтобы создать новый профиль функциональности, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0c154-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="0c154-109">В области переходов откройте окно **Модули \> Настройка канала \> Профили POS \> Профили функциональности**.</span><span class="sxs-lookup"><span data-stu-id="0c154-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="0c154-110">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="0c154-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="0c154-111">В поле **Профиль** введите код для профиля ("FN006" в примере изображения ниже).</span><span class="sxs-lookup"><span data-stu-id="0c154-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="0c154-112">В поле **Описание** введите значение ("Adventure Works Profile" в примере изображения ниже).</span><span class="sxs-lookup"><span data-stu-id="0c154-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="0c154-113">В разделе **Общие** выберите страну для языкового стандарта **ISO**.</span><span class="sxs-lookup"><span data-stu-id="0c154-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="0c154-114">В разделе **Общие** при необходимости измените другие настройки.</span><span class="sxs-lookup"><span data-stu-id="0c154-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="0c154-115">В разделе **Общие** выберите **Код профиля чеков** для чеков по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="0c154-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="0c154-116">В разделе **Функции** при необходимости измените настройки.</span><span class="sxs-lookup"><span data-stu-id="0c154-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="0c154-117">В разделе **Сумма** при необходимости измените настройки.</span><span class="sxs-lookup"><span data-stu-id="0c154-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="0c154-118">В разделе **Инфокоды** при необходимости измените настройки.</span><span class="sxs-lookup"><span data-stu-id="0c154-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="0c154-119">В разделе **Нумерация чеков** при необходимости измените настройки.</span><span class="sxs-lookup"><span data-stu-id="0c154-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="0c154-120">На следующем рисунке показан пример профиля функциональности.</span><span class="sxs-lookup"><span data-stu-id="0c154-120">The following image shows an example functionality profile.</span></span>
  
![Пример профиля функциональности](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="0c154-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0c154-122">Additional resources</span></span>

[<span data-ttu-id="0c154-123">Инфокоды и группы инфокодов</span><span class="sxs-lookup"><span data-stu-id="0c154-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="0c154-124">Создание адресной книги</span><span class="sxs-lookup"><span data-stu-id="0c154-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="0c154-125">Обзор макета экрана</span><span class="sxs-lookup"><span data-stu-id="0c154-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="0c154-126">Настройка и установка Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="0c154-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
