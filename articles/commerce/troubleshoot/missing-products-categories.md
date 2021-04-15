---
title: Продукты и категории отсутствуют после копирования среды
description: В этом разделе приведены инструкции по устранению неполадок, которые могут помочь при отсутствии продуктов и категорий после копирования сайта между средами или в рамках одной и той же среды.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 527fd0fa62775f65f61b538474b1d45d1a0155ed
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801731"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Продукты и категории отсутствуют после копирования среды

[!include [banner](../../includes/banner.md)]

В этом разделе приведены инструкции по устранению неполадок, которые могут помочь при отсутствии продуктов и категорий после копирования сайта между средами или в рамках одной и той же среды.

## <a name="description"></a>описание

После копирования сайта из одной среды в другую или в рамках той же среды продукты и категории на сайте отсутствуют. Продукты и категории будут отсутствовать в витрине электронной коммерции и на вкладке **продукты** в конструкторе сайтов Commerce.

## <a name="resolution"></a>Приказ

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>Сопоставьте номер операционной единицы канала с новым скопированным сайтом в конструкторе сайтов Commerce

Чтобы сопоставить номер операционной единицы канала (OUN) с новым скопированным сайтом в конструкторе сайтов Commerce, выполните следующие действия.

1. Выберите недавно скопированный сайт.
1. В **Параметры сайта** выберите **Каналы**.
1. Рядом с названием канала выберите многоточие (**...**), а затем выберите **Изменить канал интернет-магазина**.
1. В диалоговом окне **Изменить канал интернет-магазина** выберите канал, который необходимо сопоставить с новым скопированным сайтом, а затем нажмите кнопку **ОК**.
1. Выберите **Сохранить и опубликовать**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Связывание сайта Dynamics 365 Commerce с интернет-каналом](../associate-site-online-store.md)
