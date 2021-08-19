---
title: Синхронизация сведений об уровне запасов из Supply Chain Management с Field Service
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации сведений об уровне запасов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 8b6b052aa988a65fbbb2337b8cb14c9065c78516a1fa41d5d77ef9463d54bc7c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770200"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>Синхронизация сведений об уровне запасов из Supply Chain Management с Field Service 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации сведений об уровне запасов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.

[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service.](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Шаблоны и задачи
Следующие шаблон и базовые задачи используются для синхронизации корректировок и перемещений наличных запасов из Supply Chain Management в Field Service.

**Шаблон в интеграции данных**
- Запасы продуктов (из Supply Chain Management в Field Service)
  
**Задача в проекте интеграции данных**
- Запасы продуктов

Чтобы была возможна синхронизация уровней запасов, требуются следующие задачи синхронизации:
- Склады (из Supply Chain Management в Field Service) 
- Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Sales) 

## <a name="entity-set"></a>Набор объектов

| Field Service                      | Управление цепочкой поставок                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Запасы Dataverse в наличии по складам     |

## <a name="entity-flow"></a>Поток объектов
Сведения об уровне запасов из Finance and Operations отправляются в Field Service для выбранных продуктов. Сведения об уровне запасов включают: 
- Количество в наличии (текущее зарегистрированное физическое количество, находящееся на складе)
- Количество по заказу (общее зарегистрированное количество по заказу, например заказы на продажу)
- Заказанное количество (общее зарегистрированное заказанное количество, например заказы на покупку)

Эти сведения фиксируются по выпущенным продуктам для каждого склада и синхронизируются на основе отслеживания изменений при изменении уровня запасов.

В Field Service решение интеграции создает журналы запасов для разницы, чтобы уровни в Field Service соответствовали уровням в Supply Chain Management.

Приложение Supply Chain Management играет роль ведущего для уровней запасов. Поэтому важно настроить интеграцию для заказов на выполнение работ, перемещений и корректировок из Field Service в Supply Chain Management, если эта функция используется в Field Service, вместе с синхронизацией уровней запасов из Supply Chain Management.

Продукты и склады, где уровни запасов поддерживаются из Supply Chain Management, могут контролироваться с помощью расширенных запросов и фильтрация (Power Query).

> [!NOTE]
> Можно создать несколько складов в Field Service (с настройкой **Поддерживается извне = Нет**) и затем сопоставить их с одним складом в Supply Chain Management с функцией расширенного запроса и фильтрации. Это используется в ситуациях, когда требуется, чтобы приложение Field Service управляло подробным уровнем запасов и отправляло только обновления в приложение Supply Chain Management. В этом случае Field Service не будет получать обновления уровней запасов из Supply Chain Management. Дополнительные сведения см. в разделах [Синхронизация корректировок запасов из Field Service в Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) и [Синхронизация заказов на выполнение работ в Field Service с заказами на продажу, связанными с проектом в Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Решение Field Service CRM
Сущность **Внешние запасы продукта** используется только для обработки интеграции на сервере. Эта сущность получает значения уровня складских запасов из Supply Chain Management в интеграции, затем преобразует эти значения для журналов ручных запасов, которые затем изменяют складские продукты на складе.

## <a name="prerequisites-and-mapping-setup"></a>Необходимые условия и настройка сопоставления

### <a name="data-integration"></a>Интеграция данных
Для работы проекта необходимо убедиться, что ключ интеграции был обновлен для msdynce_externalproductinventories.
1.  Выберите **Интеграция данных > Наборы подключений**.
2.  Выберите использованный набор подключений.
3.  На вкладке **Ключ интеграции** убедитесь, что следующие ключи добавлены в msdynce_externalproductinventories:
      - msdynce_productnumber (номер продукта)
      - msdynce_warehouseid (код склада)
      
### <a name="data-integration-project"></a>Проект интеграции данных
Можно применить фильтры с расширенными запросами и фильтрацией, чтобы только определенные продукты и склады отправляли информацию об уровне запасов из Supply Chain Management в Field Service.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>Запасы продуктов (из Supply Chain Management в Field Service): запасы продуктов

[![Сопоставление шаблона в интеграции данных.](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]