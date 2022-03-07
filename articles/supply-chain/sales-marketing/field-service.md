---
title: Обзор интеграции с Microsoft Dynamics 365 Field Service
description: Этот раздел содержит обзор интеграции с Microsoft Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 07/25/2019
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 73d20958d0efadefc709db524fe16ed85d1ea33a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824902"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Обзор интеграции с Microsoft Dynamics 365 Field Service

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Supply Chain Management обеспечивает синхронизацию бизнес-процессов между Dynamics 365 Supply Chain Management и Dynamics 365 Field Service. Варианты интеграции настраиваются с помощью расширяемых шаблонов интегратора данных и службы Microsoft Dataverse для обеспечения синхронизации бизнес-процессов.
Стандартные шаблоны можно использовать для создания настраиваемых проектов интеграции, где дополнительные стандартные и настраиваемые столбцы, а также таблицы, могут быть сопоставлены для настройки интеграции и соответствия определенным бизнес-требованиям. 

Интеграция Field Service строится на основе существующей функциональности продажи перспективному клиенту.

![Синхронизация бизнес-процессов между Supply Chain Management и Field Service](./media/field-service-integration.png)

Первый этап интеграции между Field Service и Supply Chain Management направлен на то, чтобы счета за заказы на выполнение работ и соглашения в Field Service можно было выставлять в Supply Chain Management. Поддерживаемый поток начинается в Field Service, где информация из заказов на выполнение работ синхронизируется с Supply Chain Management в виде заказов на продажу. В Supply Chain Management выставляются накладные по заказам на продажу для создания документов накладных. Кроме того, информация из накладных договора в Field Service синхронизируется с Supply Chain Management. Интегратор данных Microsoft Dynamics 365 синхронизирует данные с помощью настраиваемых проектов. Стандартные шаблоны можно использовать для создания настраиваемых проектов интеграции, где дополнительные стандартные и настраиваемые столбцы, а также таблицы, могут быть сопоставлены для настройки интеграции и соответствия определенным требованиям.

Первый этап интеграции между Field Service и Supply Chain Management включает синхронизацию следующих элементов:

- [Синхронизация продуктов непосредственно из Supply Chain Management с продуктами в Field Service](field-service-product.md)
- [Синхронизация заказов на выполнение работ в Field Service с заказами на продажу в Supply Chain Management](field-service-work-order.md)
- [Синхронизация накладных договора в Field Service с накладными с произвольным текстом в Supply Chain Management](field-service-invoice.md)

Пример того, как можно синхронизировать заказ на выполнение работ между Field Service и Supply Chain Management, можно посмотреть в этом коротком видео на YouTube: [Как синхронизировать заказ на выполнение работ с помощью интеграции Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>Интеграция с Field Service, включая сведения о запасах и проектах

Дополнительная функциональность на этом втором этапе ориентирована на предоставление выездным специалистам информации по сведениям о запасах из Supply Chain Management, что позволяет им обновлять уровни запасов и выполнять перемещения материалов. Кроме того, компании, устанавливающие или обслуживающие проданные товары, получат выгоду от лучшего управления и более наглядного представления всего процесса продажи и обслуживания с интеграцией из проектов.

### <a name="functionality-includes-integration-of"></a>Функциональные возможности включают следующую интеграцию:
- Сведения о складе
- Сведения о запасах в наличии
- Перемещение запасов
- Корректировки запасов
- Проекты Supply Chain Management, связанные с заказами на работу Dynamics 365 Field Service
- Заказы на выполнение работ Dynamics 365 Field Service со ссылкой на проекты Supply Chain Management применяют этот номер проекта к заказу на продажу, чтобы обеспечить выставление накладных из проекта. 

![Синхронизация бизнес-процессов между Supply Chain Management и Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>Второй этап интеграции между Field Service и Supply Chain Management включает синхронизацию со следующими шаблонами:
- Склады (из Supply Chain Management в Field Service) — склады из Supply Chain Management в Field Service [Расширенный запрос] 
- Запасы продуктов (из Supply Chain Management в Field Service) — сведения об уровне запасов из Supply Chain Management в Field Service [Расширенный запрос] 
- Корректировка запасов (из Field Service в Supply Chain Management) — корректировки запасов из Field Service в Supply Chain Management [Расширенный запрос] 
- Перемещение запасов (из Field Service в Supply Chain Management) — перемещения запасов из Field Service в Supply Chain Management [Расширенный запрос] 
- Проекты (из Supply Chain Management в Field Service) — список проектов из Supply Chain Management в Field Service 
- Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management) — заказы на выполнение работ в Field Service с заказами на продажу в Supply Chain Management, с поддержкой для проекта [Расширенный запрос] 
- Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Sales) — "Запущенные в производство продукты продажи" из Supply Chain Management в "Продукты" из Sales для Field Service, включая единицу измерения складского учета 

## <a name="system-requirements"></a>Требования к системе

### <a name="system-requirements-for-supply-chain-management"></a>Требования к системе для Supply Chain Management
Интеграция Field Service поддерживает следующие версии:

- Версия 8.1.2 Dynamics 365 for Finance and Operations (декабрь 2018) была выпущена в декабре 2018 г. и имеет номер сборки приложения 8.1.195 с Platform update 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Системные требования для Field Service
Чтобы использовать решение интеграции Field Service, вы должны установить следующие компоненты:

- Field Service (версия 8.2.0.286) или более поздняя в Dynamics 365 9.1.x - выпущено в ноябре 2018 г.
- Решение "Перспективный клиент в наличные деньги" (P2C) для Dynamics 365, версия 1.15.0.1 или более новая версия. Это решение можно загрузить с сайта [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Решение "интеграции Field Service, проект и запасы" для Dynamics 365, версия 2.0.0.0 или более новая. Это решение можно загрузить с сайта [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]