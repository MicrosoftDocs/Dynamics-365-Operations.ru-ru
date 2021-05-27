---
title: Типы проблем для несоответствий
description: В этой теме описывается, как создавать и использовать типы проблем для несоответствий.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df509365f5c900898921acfbda380b5e20c7a251
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956809"
---
# <a name="problem-types-for-nonconformances"></a>Типы проблем для несоответствий

[!include [banner](../includes/banner.md)]

В этой теме описывается, как создавать и использовать типы проблем для несоответствий.

Используйте страницу **Типы проблем**, чтобы определить классификацию проблем качества, которые могут возникнуть для различных типов несоответствий. Для каждого создаваемого типа проблемы необходимо указать типы несоответствий, с которыми может использоваться тип проблемы. Можно настроить следующие типы несоответствий:

- **Внутреннее** — несоответствия этого типа относятся к запасам в наличии (например, к заказам контроля качества или карантинным заказам).
- **Клиент** — несоответствия этого типа относятся к заказам на продажу.
- **Поставщик** — несоответствия этого типа относятся к заказам на покупку.
- **Запрос на обслуживание** — несоответствия этого типа относятся к заказам на сервисное обслуживание.
- **Производство** — несоответствия этого типа связаны с заказами партий или производственными заказами.
- **Производство сопутствующих продуктов** — несоответствия этого типа связаны с заказами партий для сопутствующих продуктов.

При создании нового типа проблемы выберите **Типы несоответствия** на панели операций, чтобы создать список одного или нескольких типов несоответствий, которые разрешены для данного типа проблемы. Например, тип проблемы, относящийся к коду дефекта, может применяться ко всем типам несоответствия. Однако тип проблемы, относящийся к жалобам клиентов, может применяться только к типам несоответствия **Клиент** и **Запрос на обслуживание**.

## <a name="examples-of-problem-types"></a>Примеры типов проблем

Ниже приводятся примеры сценариев для типов проблем, которые могут использоваться с другими типами несоответствия:

- **Клиент:** клиент подал жалобу, клиент сделал возврат или не соблюдается спецификация качества.
- **Поставщик:** продукт поврежден, спецификации качества не соблюдены или получен неправильный продукт.
- **Запрос на обслуживание:** спецификации качества не соблюдена, клиент направил жалобу или необходимо обслуживание оборудования.
- **Производство:** спецификации качества не соблюдены, необходимо обслуживание оборудования или продукт поврежден.
- **Производство сопутствующих продуктов:** спецификации качества не соблюдены, необходимо обслуживание оборудования или продукт поврежден.

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>Создание типа проблемы и назначение его типу несоответствия

1. Перейдите в раздел **Управление запасами \> Настройка \> Управление качеством \> Типы проблемы**.
1. На панели операций выберите **Создать**, чтобы добавить строку в сетку. Затем задайте следующие поля для новой строки:

    - **Тип проблемы** — введите уникальный код или имя типа проблемы.
    - **Описание** — введите подробное описание типа проблемы.

1. Когда новая строка все еще выбрана, выберите **Типы несоответствия** на панели операций.
1. На панели операций выберите **Создать**, чтобы добавить строку в сетку. Затем в новой строке задайте в поле **Тип несоответствия** тип несоответствия, который требуется разрешить для данного типа проблемы.
1. Повторите предыдущий шаг для каждого дополнительного типа несоответствия, который необходимо разрешить для данного типа проблемы.
1. Закройте страницы.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Обзор управления качеством](quality-management-processes.md)
- [Включение управления качеством и несоответствием](enable-quality-management.md)
- [Работники, ответственные за утверждение несоответствий](quality-responsible-workers.md)
- [Карантинные зоны для несоответствий](quality-quarantine-zones.md)
- [Типы диагностики для несоответствий](quality-diagnostic-types.md)
- [Расходы по контролю качества для несоответствий](quality-charges.md)
- [Операции для несоответствий](quality-operations.md)
- [Управление качеством для складских процессов](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]