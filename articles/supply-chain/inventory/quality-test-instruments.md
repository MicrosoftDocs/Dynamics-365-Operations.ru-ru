---
title: Инструменты проверки управления качеством
description: В этой теме описывается, как создавать инструменты проверки, чтобы можно было использовать для проверок с заказами контроля качества в Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3806ca26b8909b03768dad54ddad0084e1cea4a6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021740"
---
# <a name="quality-management-test-instruments"></a>Инструменты проверки управления качеством

[!include [banner](../includes/banner.md)]

В этой теме описывается, как создавать инструменты проверки, чтобы можно было использовать для проверок с заказами контроля качества в Microsoft Dynamics 365 Supply Chain Management.

Страница **Инструменты проверки** используется для определения и просмотра сведений об устройствах, которые используются для выполнения проверок в заказах контроля качества. Инструменты проверки необязательны. Однако они могут помочь работникам системы контроля качества понять, какое устройство или инструмент следует использовать для выполнения конкретной проверки.

## <a name="test-instrument-example"></a>Пример инструмента проверки

Вы выполняете различные проверки электрических компонентов. Некоторые проверки представляют собой выходное напряжение компонентов, другая — для температуры, другая — для массы. Для выполнения каждой проверки используется несколько инструментов, устройств или приборов. Например, индикатор напряжения используется для измерения напряжения, для измерения температуры используется термометр, а для измерения веса используются весы. Каждое из этих устройств можно настроить как инструмент проверки и указать единицу измерения, в которой должны быть записаны результаты проверок. Например, результаты измерения напряжения записываются в вольтах, результаты термометра записываются в градусах по Фаренгейту или Цельсия, а результаты весов записываются в фунтах или килограммах.

## <a name="create-a-test-instrument"></a>Создание инструмента проверки

1. Перейдите **Управление запасами \> Настройка \> Контроль качества \> Инструменты проверки**.
1. На панели операций выберите **Создать**, чтобы добавить строку в сетку. Затем задайте следующие поля для новой строки:

    - **Инструмент проверки** — введите уникальный код или название инструмента проверки.
    - **Описание** — введите подробное описание инструмента проверки.
    - **Единица измерения** — выберите единицу измерения, в которой результаты измеряются результаты. Поле **Точность** устанавливается автоматически в зависимости от выбранной единицы измерения.

1. Закройте страницу.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Проверка управления качеством](quality-tests.md)
- [Группы проверки контроля качества](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
