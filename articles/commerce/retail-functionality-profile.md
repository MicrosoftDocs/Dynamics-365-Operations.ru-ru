---
title: Создание профиля функциональности розничной торговли
description: В этой статье описывается, как создать профиль функциональности в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 2ef6ae6dfd455f8021a0a2620fcacd0b4b7fcac4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900420"
---
# <a name="create-a-retail-functionality-profile"></a>Создание профиля функциональности розничной торговли

[!include [banner](includes/banner.md)]

В этой статье описывается, как создать профиль функциональности в Microsoft Dynamics 365 Commerce.

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
  
![Пример профиля функциональности.](media/retail-functionality-profile.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Инфокоды и группы инфокодов](info-codes-retail.md)           

[Создание адресной книги](new-address-book.md) 

[Обзор макета экрана](pos-screen-layouts.md)       

[Настройка и установка Retail Hardware Station](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
