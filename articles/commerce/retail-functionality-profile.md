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
# <a name="create-a-retail-functionality-profile"></a>Создание профиля функциональности розничной торговли

[!include [banner](includes/banner.md)]

В этом разделе описывается, как создать профиль функциональности в Microsoft Dynamics 365 Commerce.

Профиль функциональности коммерции предоставляет различные параметры, используемые для интернет-каналов. Каждый канал должен указывать профиль функциональности.

## <a name="create-a-functionality-profile"></a>Создать профиль функциональности

Чтобы создать новый профиль функциональности, выполните следующие действия.

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
  
На следующем рисунке показан пример профиля функциональности.
  
![Пример профиля функциональности](media/retail-functionality-profile.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Инфокоды и группы инфокодов](info-codes-retail.md)           

[Создание адресной книги](new-address-book.md) 

[Обзор макета экрана](pos-screen-layouts.md)       

[Настройка и установка Retail Hardware Station](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
