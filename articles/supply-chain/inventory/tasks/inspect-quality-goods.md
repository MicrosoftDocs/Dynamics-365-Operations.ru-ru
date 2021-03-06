---
title: Контроль качества товаров
description: В этом разделе объясняется, как обработать заказы для контроля качества.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956142"
---
# <a name="inspect-the-quality-of-goods"></a>Контроль качества товаров

[!include [banner](../../includes/banner.md)]

В этом разделе объясняется, как обработать заказы для контроля качества. Контроль качества обычно выполняется сотрудником отдела контроля качества.

Если установлены стандартные демонстрационные данные, их можно использовать для выполнения процедур, описанных в этом разделе. Для использования демонстрационных данных выберите юридическое лицо *USMF*. Затем необходимо подтвердить заказ на покупку *000016* и разнести поступление продуктов. Автоматически создается заказа на контроль качества.

## <a name="step-1-select-a-quality-order"></a>Шаг 1. Выбор заказа контроля качества

Чтобы выбрать заказ контроля качества, выполните следующие действия.

1. Перейдите в раздел **Управление запасами \> Периодические задачи \> Управление качеством \> Заказы для контроля качества**.
1. Выберите заказ контроля качества, созданный перед началом этой процедуры.

## <a name="step-2-record-test-results"></a>Шаг 2. Запись результатов проверки

Чтобы записать результаты проверки, выполните следующие действия.

1. Выберите **Результаты**.
1. Выберите **Правка**.
1. В поле **Итоговое количество** введите число.
1. В поле **Результаты** выберите требуемую запись. В этом примере результат основан на заранее определенном итоге. Обычно фиксируется более конкретный результат проверки, например размер или другая аналитика.
1. Нажмите **Сохранить**.
1. Закройте страницу.

## <a name="step-3-validate-the-quality-order"></a>Шаг 3. Проверить заказ контроля качества

Чтобы проверить заказ контроля качества, выполните следующие действия.

1. Выберите **Проверить**.
1. В поле **Кем проверено** выберите пользователя, который выполняет проверку.
1. Выберите **Выбрать**.
1. Нажмите **ОК**.
1. Закройте страницу.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
