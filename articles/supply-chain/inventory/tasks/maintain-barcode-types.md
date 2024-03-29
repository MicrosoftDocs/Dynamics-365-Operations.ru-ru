---
title: Ведение типов штрихкодов
description: Эта процедура описывает, как настроить новое определение штрих-кода, которое можно использовать как часть отчета листа подбора.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b689d1fc85d59ac87efa1903fd7122ae5ff011da
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571121"
---
# <a name="maintain-bar-code-types"></a>Ведение типов штрихкодов

[!include [banner](../../includes/banner.md)]

Эта процедура описывает, как настроить новое определение штрих-кода, которое можно использовать как часть отчета листа подбора. Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные. При использовании USMF можно использовать представленные примеры значений. Эти задачи обычно выполняются менеджером склада.

1. Перейдите к **Штрих-коды**.
1. Выберите **Создать**.
1. В поле **Настройка штрих-кода** введите значение.
1. В поле **Описание** введите значение.
1. В поле **Тип штрих-кода** выберите один из вариантов.
    * При использовании USMF можно выбрать "Code 39".
1. В поле **код маски** укажите код маски штрих-кода. Маски штрих-кодов используются для создания штрих-кодов и для быстрого определения штрих-кодов, которые сканируются в системе POS. Дополнительные сведения см. в разделе [Настройка масок штрих-кодов](../../../commerce/set-up-bar-code-masks.md).
1. В поле **Размер** введите число.
1. В поле **Максимальная длина** введите число.
1. Нажмите **Сохранить**.
1. Закройте страницу.
1. Перейдите к **параметрам модуля "Управление запасами и складами"**.
1. В поле **Настройка штрих-кода** введите или выберите значение.
    * Выберите настройку штрих-кода, созданную ранее, но помните, что формат штрих-кода должен соответствовать формату уникального кода для типа записи, используемой в процессе. Например, для маршрутов комплектации формат штрих-кода должен соответствовать формату ссылки маршрута комплектации, которая обычно является номерной серией.  
1. Нажмите **Сохранить**.
1. Закройте страницу.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
