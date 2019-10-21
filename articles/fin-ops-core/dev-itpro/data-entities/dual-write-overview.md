---
title: Интеграция данных между Finance and Operations и Common Data Service почти в режиме реального времени
description: Эта тема содержит обзор интеграции между Finance and Operations и Common Data Service.
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
ms.openlocfilehash: b7d9e6be6fb2fef85bcf1182f89b8e370abea3d6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184493"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Интеграция данных почти в реальном времени с Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

В современном цифровом мире бизнес-экосистемы используют приложения Microsoft Dynamics 365 как единое целое. Поскольку данные от людей, клиентов, операций и устройств Интернета вещей (IoT) стекаются в один источник, есть возможность для цифровых циклов обратной связи. Для достижения этого опыта важна интеграция между приложениями Finance and Operations и другими приложениями Dynamics 365. Некоторые приложения строятся на основе Common Data Service. Интеграция данных между приложениями Finance and Operations с Common Data Service позволяет другим приложениям взаимодействовать согласованно и свободно с Finance and Operations.

Приложения Finance and Operations и Common Data Service обеспечивают синхронизацию данных почти в режиме реального времени между приложениями Finance and Operations и другими приложениями Dynamics 365 через систему двойной записи. Охват широк и включает 28 поверхностных областей приложения. Цель состоит в том, чтобы обеспечить пользовательский опыт "одного Dynamics 365" через бесшовные потоки данных, которые соединяют бизнес-процессы между приложениями.

![Диаграмма обзора архитектуры](media/dual-write-overview.jpg)

Следующие ценностные предложения доступны для клиентов:

+ [Организационная иерархия в Common Data Service](dual-write-organization.md)
+ [Концепция компании в Common Data Service](dual-write-company.md)
+ [Интегрированный мастер клиентов](dual-write-customer.md)
+ [Интегрированный мастер поставщиков](dual-write-vendor.md)
+ Единый шаблон продукта

## <a name="system-requirements"></a>Требования к системе

Синхронные, двунаправленные, практически в режиме реального времени потоки данных требуют следующих версий:

+ Microsoft Dynamics 365 for Finance and Operations версии 10.0.4 (июль 2019 г.) с обновлением платформы Platform update 28 или выше
+ Microsoft Dynamics 365 for Customer Engagement, платформа версии 9.1 (4.2) или более новая версия

## <a name="setup-instructions"></a>Инструкции по установке

Выполните следующие шаги, чтобы настроить интеграцию между приложениями Finance and Operations и Common Data Service.
    
1. Для настройки системы двойной записи, см. [пошаговое руководство](https://aka.ms/dualwrite-docs) в объявлении предварительной версии двойной записи.
2. Скачайте и установите решение из группы [Интеграция Finance and Operations, Common Data Service и Customer Engagement](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) в Yammer. Пакет содержит пять решений:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Следуйте порядку выполнения для [синхронизации исходных справочных данных](dual-write-initial.md).
4. Если вы столкнулись с проблемами синхронизации с двойной записью, см. [Руководство по устранению неполадок для интеграции данных](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Вы не можете запустить двойную запись и [продажу перспективному клиенту](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) бок о бок. Если вы выполняете решение "Продажа перспективному клиенту", вы должны удалить его. Вы также должны отключить шаблоны двойной записи для клиентов и поставщиков, которые являются частью решения продажи перспективному клиенту.
