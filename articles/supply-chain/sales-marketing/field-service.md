---
title: Обзор интеграции с Microsoft Dynamics 365 for Field Service
description: Этот раздел содержит обзор интеграции с Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 22abe83f06b7fc57c73fb82ccafc4b426667e7c6
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865215"
---
# <a name="integration-with-microsoft-dynamics-365-for-field-service-overview"></a>Обзор интеграции с Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations обеспечивает синхронизацию бизнес-процессов между Finance and Operations и Microsoft Dynamics 365 for Field Service. Варианты интеграции настраиваются с помощью расширяемых шаблонов интегратора данных и службы Common Data Service (CDS) для обеспечения синхронизации бизнес-процессов.
Стандартные шаблоны можно использовать для создания настраиваемых проектов интеграции, где дополнительные стандартные и настраиваемые поля, а также объекты, могут быть сопоставлены для настройки интеграции и соответствия определенным бизнес-требованиям. 

Интеграция Field Service строится на основе существующей функциональности продажи перспективному клиенту.

![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/field-service-integration.png)

Первый этап интеграции между Field Service и Finance and Operations направлен на то, чтобы счета за заказы на выполнение работ и соглашения в Field Service можно было выставлять в Finance and Operations. Поддерживаемый поток начинается в Field Service, где информация из заказов на выполнение работ синхронизируется с Finance and Operations в виде заказов на продажу. В Finance and Operations счета за заказы на продажу выставляются для создания документов накладных. Кроме того, информация из накладных договора в Field Service синхронизируется с Finance and Operations. Интегратор данных Microsoft Dynamics 365 синхронизирует данные с помощью настраиваемых проектов. Стандартные шаблоны можно использовать для создания настраиваемых проектов интеграции, где дополнительные стандартные и настраиваемые поля, а также объекты, могут быть сопоставлены для настройки интеграции и соответствия определенным требованиям.

Первый этап интеграции между Field Service and Finance and Operations включает синхронизацию следующих элементов:

- [Продукты в Finance and Operations с продуктами в Field Service, которые включают сведения о типе продукта](field-service-product.md)
- [Заказы на выполнение работ в Field Service с заказами на продажу в Finance and Operations](field-service-work-order.md)
- [Накладные в Field Service с накладными с произвольным текстом в Finance and Operations](field-service-invoice.md)

Пример того, как можно синхронизировать заказ на выполнение работ между Field Service и Finance and Operations, можно посмотреть в этом коротком видео на YouTube: [Как синхронизировать заказ на выполнение работ с помощью интеграции Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Интеграция с Microsoft Dynamics 365 for Field Service, включая сведения о запасах и проектах

Дополнительная функциональность на этом втором этапе ориентирована на предоставление выездным специалистам информации по сведениям о запасах из Finance and Operations, что позволяет им обновлять уровни запасов и выполнять перемещения материалов. Кроме того, компании, устанавливающие или обслуживающие проданные товары, получат выгоду от лучшего управления и более наглядного представления всего процесса продажи и обслуживания с интеграцией из проектов.

### <a name="functionality-includes-integration-of"></a>Функциональные возможности включают следующую интеграцию:
- Сведения о складе
- Сведения о запасах в наличии
- Перемещение запасов
- Корректировки запасов
- Проекты Dynamics 365 for Finance and Operations, связанные с заказами на выполнение работ в Dynamics 365 for Field Service
- Заказы на выполнение работ Dynamics 365 for Field Service со ссылкой на проекты Dynamics 365 for Finance and Operations применяют этот номер проекта к заказу на продажу в Dynamics 365 for Finance and Operations, чтобы обеспечить выставление накладных из проекта. 

![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Второй этап интеграции между Field Service and Finance and Operations включает синхронизацию со следующими шаблонами:
- Склады (из Fin and Ops в Field Service) — склады из Finance and Operations в Field Service [Расширенные запросы] 
- Запасы продуктов (из Fin and Ops в Field Service) — сведения об уровне запасов из Finance and Operations в Field Service [Расширенные запросы] 
- Корректировка запасов (из Field Service в Fin and Ops) — корректировки запасов из Field Service в Finance and Operations [Расширенные запросы] 
- Перемещения запасов (из Field Service в Fin and Ops) — перемещения запасов из Field Service в Finance and Operations [Расширенные запросы] 
- Проекты (из Fin and Ops в Field Service) — список проектов из Finance and Operations в Field Service 
- Заказы на выполнение работ с проектом (из Field Service в Fin and Ops) — заказы на выполнение работ в Field Service с заказами на продажу в Finance and Operations, с поддержкой для проекта [Расширенные запросы] 
- Продукты Field Service с единицей измерения складского учета (из Fin and Ops в Sales) — "Запущенные в производство продукты продажи" из Finance and Operations в "Продукты" из Sales для Field Service, включая единицу измерения складского учета 

## <a name="system-requirements"></a>Требования к системе

### <a name="system-requirements-for-finance-and-operations"></a>Системные требования для Finance and Operations
Интеграция Field Service поддерживает следующие версии:

- Версия 8.1.2 Dynamics 365 for Finance and Operations (декабрь 2018) была выпущена в декабре 2018 г. и имеет номер сборки приложения 8.1.195 с Platform Update 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Системные требования для Field Service
Чтобы использовать решение интеграции Field Service, вы должны установить следующие компоненты:

- Field Service for Dynamics 365 (версия 8.2.0.286) или более поздняя в Dynamics 365 9.1.x - выпущено в ноябре 2018 г.
- Решение "Перспективный клиент в наличные деньги" (P2C) для Dynamics 365, версия 1.15.0.1 или более новая версия. Это решение можно загрузить с сайта [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Решение "интеграции Field Service, проект и запасы" для Dynamics 365, версия 2.0.0.0 или более новая. Это решение можно загрузить с сайта [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).
