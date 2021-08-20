---
title: Невозможно импортировать номенклатуру, используя сущность выпущенных продуктов версии V2
description: Невозможно импортировать номенклатуру, используя сущность выпущенных продуктов версии V2.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: efd773313f89784d8fca6b37d867e204cb2d06ab29694a19cbec7eed107a8019
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764700"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Невозможно импортировать номенклатуру, используя сущность выпущенных продуктов версии V2

Номер статьи базы знаний: 4611825

## <a name="symptoms"></a>Симптомы

При попытке импорта номенклатуры с использованием сущности *Выпущенные продукты V2* выводится сообщение об ошибке, как в следующем примере:

> Невозможно создать запись в группах аналитик отслеживания номенклатур (EcoResTrackingDimensionGroupItem). Номер номенклатуры: 2040663, партия. Запись уже существует.

## <a name="resolution"></a>Приказ

Для импорта новых выпущенных продуктов необходимо использовать сущность *Создание выпущенного продукта V2* вместо сущности *Выпущенные продукты V2*.
