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
# <a name="create-a-retail-functionality-profile"></a>Создание профиля функциональности розничной торговли


[!include [banner](includes/banner.md)]

В этом разделе описывается, как создать профиль функциональности розничной торговли в Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Профиль функциональности розничной торговли предоставляет различные параметры, используемые для интернет-каналов. Каждый канал розничной торговли должен указывать профиль функциональности розничной торговли.

## <a name="create-a-retail-functionality-profile"></a>Создание профиля функциональности розничной торговли

Чтобы создать новый профиль функциональности розничной торговли, выполните следующие действия.

1. В области переходов откройте окно **Модули \> Настройка канала \> Профили POS \> Профили функциональности**.
1. В области действий выберите **Создать**.
1. В поле **Профиль** введите код для профиля ("FN006" в примере изображения ниже).
1. В поле **Описание** введите значение ("Adventure Works Profile" в примере изображения ниже).
1. В разделе **Общие** выберите страну для языкового стандарта **ISO**.
1. В разделе **Общие** при необходимости измените другие настройки.
1. В разделе **Общие** выберите **Код профиля чеков** для чеков по электронной почте.
1. В разделе **Функции** при необходимости измените настройки.
1. В разделе **Сумма** при необходимости измените настройки.
1. В разделе **Инфокоды** при необходимости измените настройки.
1. В разделе **Нумерация чеков** при необходимости измените настройки. 
  
На следующем рисунке показан пример профиля функциональности розничной торговли.
  
![Пример профиля функциональности розничной торговли](media/retail-functionality-profile.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Инфокоды и группы инфокодов](info-codes-retail.md)           

[Создание адресной книги](new-address-book.md) 

[Обзор макета экрана](pos-screen-layouts.md)       

[Настройка и установка Retail Hardware Station](retail-hardware-station-configuration-installation.md) 
