---
title: Расширение сущностей данных по запасам в наличии
description: В этом разделе приводится пример, в котором показано, как добавлять расширенные поля в представления INVENTORSITEONHANDENTITY и INVENTWAREHOUSEONHANDENTITY, чтобы возможности сущностей данных по запасам в наличии могли работать с этими расширениями.
author: sherry-zheng
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 7863f37e66727e2e80ea8c8b013ee49930e7c684
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829916"
---
# <a name="extend-inventory-on-hand-data-entities"></a>Расширение сущностей данных по запасам в наличии

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management предоставляет функции [расширяемости](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md), позволяющие [добавлять поля в таблицы посредством расширения](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md). В этом разделе приводится пример, в котором показано, как добавлять расширенные поля в представления `INVENTORSITEONHANDENTITY` и `INVENTWAREHOUSEONHANDENTITY`, чтобы возможности сущностей данных по запасам в наличии могли работать с этими расширениями. Дополнительные сведения о сущностях данных см. в разделе [Обзор управления данными](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

> [!NOTE]
> Ниже приводится список некоторых сущностей данных по запасам в наличии:
>
> - Запасы в наличии по сайту
> - Запасы в наличии по сайту V2
> - Запасы в наличии по складам
> - Запасы в наличии по складам v2

После добавления полей в таблицы, используемые представлением `inventSiteOnHandView`, необходимо синхронизировать механизм, чтобы расширения были правильно распознаны.

1. Расширьте представление `InventSiteOnHandView`, добавив поле расширения.
1. Расширьте представление `InventSiteOnHandAggregatedView` с помощью полей расширения.
1. Расширение класса viewBuilder `InventSiteOnHandAggregatedViewBuilder` путем изменения метода `getExtensionFields()`. Таким образом, поля старого представления сопоставляются с новыми полями просмотра при выполнении синхронизации viewBuilder.

Например, к таблице `InventTable` добавлены следующие четыре поля с помощью расширения:

- Настраиваемое поле 1
- Настраиваемое поле 2
- Настраиваемое поле 3
- Настраиваемое поле 4

В таком случае метод `getExtensionFields()` необходимо изменить следующим образом.

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

После выполнения этих шагов можно расширить сущности данных по запасам в наличии по сайту и запасам в наличии по складу, добавив новые поля. Таким образом можно гарантировать, что расширенные поля будут распознаны и включены во время переноса данных, использующего эти сущности данных.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]