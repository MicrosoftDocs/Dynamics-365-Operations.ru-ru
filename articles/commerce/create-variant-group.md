---
title: Создание группы вариантов
description: В этом разделе описывается, как создать группу вариантов размера, стиля или цвета для продукта в Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0462958d8225de145a8d886b096f96cd3f2cb5c5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799549"
---
# <a name="create-a-variant-group"></a>Создание группы вариантов


[!include [banner](includes/banner.md)]

В этом разделе описывается, как создать группу вариантов размера, стиля или цвета для продукта в Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Dynamics 365 Commerce поддерживает несколько вариантов продуктов. Для различных категорий продуктов лучше всего настроить группы вариантов. Например, группа размера может быть создана для футболок с размерами "самый малый", "малый", "средний", "большой" и "огромный", либо можно создать группу цвета, чтобы включить все доступные цвета продукта. Группы вариантов необходимо добавить перед добавлением продуктов.

В этом разделе будет создана и настроена группа размера. Аналогичные процедуры могут использоваться для добавления и настройки групп стилей и групп цветов.

## <a name="create-a-size-group"></a>Создание группы цвета

Чтобы создать группу цвета, выполните следующие действия.
 
1. В области переходов выберите **Модули \> Retail и Commerce \> Продукты и категории \> Группы вариантов \> Группы размера**.
1. В области действий выберите **Создать**.
1. В поле **Группа размера** введите имя для группы размера.
1. В поле **Описание** введите соответствующее описание.
1. На панели операций выберите **Сохранить**.

## <a name="add-attributes-to-the-size-group"></a>Добавление атрибутов в группу размеров

Чтобы добавить атрибуты в группу размера, выполните следующие действия.

1. В области переходов выберите **Модули \> Retail и Commerce \> Продукты и категории \> Группы вариантов \> Группы размера**
1. В области переходов категорий выберите группу размера.
1. В области **Строки группы размера** выберите **Добавить**.
1. В поле **Группа размера** введите строку, представляющую размер (например, "XL").
1. В поле **Имя размера** введите название для размера (например, "огромный").
1. В поле **Вес пополнения** введите число, обозначающее вес пополнения.
1. В поле **Номер в штрих-коде** введите число, представляющее штрих-код.
1. В поле **Порядок отображения** введите номер порядка отображения.
1. По завершении добавления размеров выберите **Сохранить** на панели операций.

На следующем рисунке показан пример группы размера для "размеров повседневных футболок".

![Создание группы цвета](media/create-variant-group.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор сведений о продуктах](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Настройка розничных продуктов](set-up-retail-products.md)

[Аналитики продуктов](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]