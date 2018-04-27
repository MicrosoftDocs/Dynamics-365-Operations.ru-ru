---
title: "Интеграция с Microsoft Dynamics 365 for Field Service"
description: "В этом разделе представлен обзор интеграции с Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d32a4e376770fc73c79b94924d5ae062d201d84a
ms.openlocfilehash: a224962152e80293f6cf3425dea74d73a283e31a
ms.contentlocale: ru-ru
ms.lasthandoff: 04/12/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Интеграция с Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations включает синхронизацию бизнес-процессов между Finance and Operations и Microsoft Dynamics 365 for Field Service. Варианты интеграции настраиваются с помощью расширяемых шаблонов интегратора данных и службы Common Data Service (CDS) для обеспечения синхронизации бизнес-процессов.

[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

Первый этап интеграции между Field Service и Finance and Operations направлен на то, чтобы счета за заказы на выполнение работ и соглашения в Field Service можно было выставлять в Finance and Operations. Поддерживаемый поток начинается в Field Service, где информация из заказов на выполнение работ синхронизируется с Finance and Operations в виде заказов на продажу. В Finance and Operations счета за заказы на продажу выставляются для создания документов накладных. Кроме того, информация из накладных договора в Field Service синхронизируется с Finance and Operations. Интегратор данных Microsoft Dynamics 365 синхронизирует данные с помощью настраиваемых проектов. Стандартные шаблоны можно использовать для создания настраиваемых проектов интеграции, где дополнительные стандартные и настраиваемые поля, а также объекты, могут быть сопоставлены для настройки интеграции и соответствия определенным требованиям.

Первый этап интеграции между Field Service and Finance and Operations включает синхронизацию следующих элементов:

- [Продукты в Finance and Operations с продуктами в Field Service, которые включают сведения о типе продукта](field-service-product.md)
- [Заказы на выполнение работ в Field Service с заказами на продажу в Finance and Operations](field-service-work-order.md)
- [Накладные в Field Service с накладными с произвольным текстом в Finance and Operations](field-service-invoice.md)

## <a name="system-requirements-for-finance-and-operations"></a>Системные требования для Finance and Operations
Интеграция Field Service поддерживает следующие версии:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations, версия 8.0 (апрель 2018 г.) и новее

- Dynamics 365 for Finance and Operations версии 8.0 (апрель 2018) выпущена в апреле 2018 и имеет номер сборки приложения 8.0.30.8020 с обновлением платформы 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Системные требования для Field Service
Чтобы использовать решение интеграции Field Service, вы должны установить следующие компоненты:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 или новее

- Dynamics 365 for Field Service версии 1612 (9.0.1.733) (БД 9.0.1.733) (сетевая версия) или более новой.
- Решение "Перспективный клиент в наличные деньги" (P2C) для Dynamics 365, версия 1.15.0.1 или более новая версия. Это решение можно загрузить с сайта [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Решение интеграции Field Service для Dynamics 365, версия 1.0.0.0 или более новая. Это решение можно загрузить с сайта AppSource. **(ОЖИДАЕТСЯ ВЫПУСК)**

