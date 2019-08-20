---
title: Решение "Перспективный клиент в наличные деньги"
description: В этой теме представлен обзор решения "Перспективный клиент в наличные деньги" между Microsoft Dynamics 365 for Finance and Operations и Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
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
ms.openlocfilehash: e31994ea3cd73dcc749a02ce2cd0815be191a567
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742409"
---
# <a name="prospect-to-cash"></a>Решение "Перспективный клиент в наличные деньги"

[!include [banner](../includes/banner.md)]

Решение "Перспективный клиент в наличные деньги" обеспечивает прямую синхронизацию между Dynamics 365 for Finance and Operations и Dynamics 365 for Sales. Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных для организаций, контактов, продуктов, предложений по продажам, заказов на продажу и накладных по продажам между Finance and Operations и Sales. Во время выполнения обмена данными между Finance and Operations и Sales вы можете выполнять мероприятия по продажам и маркетингу в Sales и обрабатывать выполнение заказов с помощью управления запасами в Finance and Operations. 

Дополнительные сведения об интеграции решения "Перспективный клиент в наличные деньги" см. в коротком видео на YouTube: [Интеграция решения "Перспективный клиент в наличные деньги"](https://www.youtube.com/watch?v=AVV9x5x-XCg).

В текущей версии решение "Перспективный клиент в наличные деньги" предоставляет следующие типы прямой синхронизации:

- [Ведение организаций в Sales и их прямая синхронизация из Sales в Finance and Operations](accounts-template-mapping-direct.md)
- [Ведение продуктов в Finance and Operations и их синхронизация напрямую с Sales](products-template-mapping-direct.md)
- [Ведение контактов в Sales и их синхронизация с контактами или клиентами напрямую в Finance and Operations](contacts-template-mapping-direct.md)
- [Синхронизация предложений по продажам напрямую из Sales с Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [Синхронизация заказов на продажу напрямую между Sales и Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
- [Синхронизация накладных по продаже напрямую из Finance and Operations в Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a>Системные требования для Finance and Operations
Интеграция решения "Перспективный клиент в наличные деньги" поддерживается в следующих версиях:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (декабрь 2017 г.)

- Dynamics 365 for Finance and Operations, Enterprise edition (декабрь 2017 г.) — сборка приложения 7.3.11971.56116 с обновлением платформы 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise edition (июль 2017 г.)

- Dynamics 365 for Finance and Operations, Enterprise edition (июль 2017 г.) — с обновлением платформы 8 (сборка приложения 7.2.11792.56024 со сборкой платформы 7.0.4565.16212).
- Следующие исправления являются обязательными:

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** — это исправление делает возможным синхронизацию заказов на продажу из Sales в Finance and Operations с помощью компонента интеграции данных. Оно также предоставляет несколько других улучшений.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** — это исправление делает возможным синхронизацию строк заказов на продажу из Finance and Operations в Sales с помощью компонента интеграции данных.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** — это исправление делает возможным синхронизацию заказов на продажу из Finance and Operations в Sales с помощью компонента интеграции данных.

    > [!NOTE]
    > Достаточно установить только KB4045570, потому что в пакет установки входят изменения из других исправлений. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations версии 1611 (ноябрь 2016 г.)

- Dynamics 365 for Finance and Operations версии 1611 (ноябрь 2016 г.) с обновлением платформы 8 или выше

- Следующие исправления являются обязательными:

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** — делает возможной синхронизацию заказов на продажу с помощью компонента интеграции данных из Finance and Operations в Sales. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** — делает возможной синхронизацию заголовков и строк заказов на продажу с помощью компонента интеграции данных из Finance and Operations в Sales.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** — требуется поддержка интеграции решения "Перспективный клиент в наличные деньги" с помощью информационных объектов.
    
    > [!NOTE]
    > После установки исправлений необходимо запустить следующее пакетное задание из формы **SalesPopulateProspectToCash**. Эта форма скрыта, так как она требуется только один раз. Для доступа к форме выполните вход в среду и добавьте следующее в URL-адрес в веб-браузере: *&mi=action:SalesPopulateProspectToCash*, например `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Когда форма откроется, щелкните OK. При этом новое поле **LineCreationSequnceNumber** в таблицах **SalesLine**, **SalesQuotationLine** и **CustInvoiceTrans** будет заполнено уникальными значениями, и будет обновлен список продуктов. Это необходимо для работы интеграции решения "Перспективный клиент в наличные деньги".


## <a name="system-requirements-for-sales"></a>Системные требования для Sales

Чтобы использовать решение "Перспективный клиент в наличные деньги", вы должны установить следующие компоненты:

- Dynamics 365 for Sales версии 1612 (8.2.1.207) (DB 8.2.1.207) Online или более новая версия
- Решение "Перспективный клиент в наличные деньги" для Dynamics 365 for Sales, версия 1.15.0.0 или более новая версия. Это решение можно загрузить с сайта AppSource. [Загрузка Dynamics 365, "Перспективный клиент в наличные деньги"](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
