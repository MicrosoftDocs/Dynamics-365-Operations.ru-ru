---
title: Интеграция данных почти в реальном времени с Common Data Service
description: Этот раздел содержит обзор интеграции между Finance and Operations и Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019982"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Интеграция данных почти в реальном времени с Common Data Service

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

В современном цифровом мире бизнес-экосистемы используют приложения Microsoft Dynamics 365 как единое целое. Поскольку данные от людей, клиентов, операций и устройств Интернета вещей (IoT) стекаются в один источник, есть возможность для цифровых циклов обратной связи. Для достижения этого опыта важна интеграция между приложениями Finance and Operations и другими приложениями Dynamics 365. Некоторые приложения строятся на основе Common Data Service. Интеграция между данными приложений Finance and Operations и Common Data Service позволяет другим приложениям взаимодействовать друг с другом и свободно с Finance and Operations.

Приложения Finance and Operations и Common Data Service обеспечивают синхронизацию данных почти в режиме реального времени между приложениями Finance and Operations и другими приложениями Dynamics 365 через систему двойной записи. Охват широк и включает 28 поверхностных областей приложения. Цель состоит в том, чтобы обеспечить пользовательский опыт "одного Dynamics 365" через бесшовные потоки данных, которые соединяют бизнес-процессы между приложениями.

![Диаграмма обзора архитектуры](media/dual-write-overview.jpg)

Следующие ценностные предложения доступны:

+ [Организационная иерархия в Common Data Service](organization-mapping.md)
+ [Концепция компании в Common Data Service](company-data.md)
+ [Интегрированный мастер клиентов](customer-mapping.md)
+ [Интегрированная ГК](ledger-mapping.md)
+ [Унифицированный опыт работы с продуктом](product-mapping.md)
+ [Интегрированный мастер поставщиков](vendor-mapping.md)
+ [Интегрированные сайты и склады](sites-warehouses-mapping.md)
+ [Интегрированная налоговый справочник](tax-mapping.md)

## <a name="system-requirements"></a>Требования к системе

Синхронные, двунаправленные, практически в режиме реального времени потоки данных требуют следующих версий:

+ Microsoft Dynamics 365 for Finance and Operations версии 10.0.4 (июль 2019 г.) с обновлением платформы Platform update 28 или выше
+ Microsoft Dynamics 365 for Customer Engagement, платформа версии 9.1 (4.2) или более новая версия

## <a name="setup-instructions"></a>Инструкции по установке

Выполните эти шаги для настройки интеграции между приложениями Finance and Operations и Common Data Service.
    
1. Для настройки системы двойной записи, см. [пошаговое руководство](https://aka.ms/dualwrite-docs) в объявлении предварительной версии двойной записи.
2. Загрузите и установите решение из группы Yammer [Fin Ops и CDS/CE Integration через Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096). Пакет содержит пять решений:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Следуйте порядку выполнения для [синхронизации исходных справочных данных](initial-sync.md).
4. Если вы столкнулись с проблемами синхронизации с двойной записью, см. [Руководство по устранению неполадок для интеграции данных](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Вы не можете запустить двойную запись и [продажу перспективному клиенту](../../../../supply-chain/sales-marketing/prospect-to-cash.md) бок о бок. Если вы выполняете решение "Продажа перспективному клиенту", вы должны удалить его. Вы также должны отключить шаблоны двойной записи для клиентов и поставщиков, которые являются частью решения продажи перспективному клиенту.
