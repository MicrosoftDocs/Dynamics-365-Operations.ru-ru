---
title: "Решение \"Перспективный клиент в наличные деньги\""
description: "В этой теме представлен обзор решения \"Перспективный клиент в наличные деньги\" между Dynamics 365 for Finance and Operations, Enterprise Edition и Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a>Решение "Перспективный клиент в наличные деньги"  

[!include[banner](../includes/banner.md)]

Решение "Перспективный клиент в наличные деньги" использует [интеграцию данных](/common-data-service/entity-reference/dynamics-365-integration) для синхронизации данных между экземплярами Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition и Dynamics 365 for Sales с помощью службы Common Data Service (CDS). Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных о счетах, контактах, продуктах, предложениях по продажам, заказах на продажу и накладных по продажам между Finance and Operations и Sales. Во время выполнения обмена данными между Finance and Operations и Sales вы можете продолжать выполнять мероприятия по продажам и маркетингу в Sales и обрабатывать выполнение заказов с помощью управления запасами в Finance and Operations. 

Это решение обеспечивает интеграцию в следующих областях: 

-   [Ведение счетов в Sales и их синхронизация с Finance and Operations](accounts-template-mapping.md)
-   [Ведение контактов в Sales и их синхронизация с Finance and Operations](contacts-template-mapping.md)
-   [Ведение продуктов в Finance and Operations и их синхронизация с Sales](products-template-mapping.md)
-   [Создание предложений по продажам в Sales и их синхронизация с Finance and Operations](sales-quotation-template-mapping.md)
-   [Создание заказов на продажу в Finance and Operations и их синхронизация с Sales](sales-order-template-mapping.md)
-   [Создание накладных по продажам в Finance and Operations и их синхронизация с Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Требования к системе для Dynamics 365 for Finance and Operations, Enterprise Edition

Чтобы использовать решение "Перспективный клиент в наличные деньги", вы должны установить следующее:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.) с обновлением платформы 8 (приложение 7.2.11792.56024 с платформой 7.0.4565.16212)

- Два исправления для Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.).

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) — это исправление делает возможным синхронизацию строк заказов на продажу с помощью компонента интеграции данных из Finance and Operations в Sales.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) — это исправление делает возможным синхронизацию заказов на продажу с помощью компонента интеграции данных из Finance and Operations в Sales.
    
**Примечание**. Достаточно установить только KB4036524, потому что в пакет установки входят изменения из KB4036461.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Требования к системе для Dynamics 365 for Sales

Чтобы использовать решение "Перспективный клиент в наличные деньги", вы должны установить следующее:

- Dynamics 365 for Sales версии 1612 (8.2.1.207) (БД 8.2.1.207) (сетевая версия) или выше.
- Решение "Перспективный клиент в наличные деньги" Dynamics 365 for Sales, версия 1.14.0.0 (v14) или выше.

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Установка решения "Перспективный клиент в наличные деньги" для Sales

- Загрузите [ZIP-файл с пакетом решения "Перспективный клиент в наличные деньги" для Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) на CustomerSource.

- Убедитесь, что ZIP-файл не заблокирован, чтобы не получить при установке пакета решения сообщение об ошибке "Пакеты для импорта не найдены". Чтобы разблокировать файл, выполните следующие действия:

    -  Щелкните ZIP-файл правой кнопкой мыши.
    -  Выберите **Свойства**, а затем выберите **Разблокировать**. 

- Распакуйте и запустите PackageDeployer.exe.

- Установите решение "Перспективный клиент в наличные деньги" в своем экземпляре Sales.

    - Выберите тип развертывания **Office 365**.
    - Выберите **Показать дополнительные параметры**.
    - Для быстрой установки выберите **Область**. При выборе варианта **Не знаю** система выполняет поиск всех регионов, и установка займет больше времени.
    - Введите **Имя пользователя** и **Пароль** для пользователя admin, у которого есть права на установку.

