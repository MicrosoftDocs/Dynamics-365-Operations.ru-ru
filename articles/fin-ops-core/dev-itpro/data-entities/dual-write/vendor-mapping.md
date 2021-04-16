---
title: Интегрированный справочник поставщиков
description: Эта тема описывает интеграцию данных поставщика между приложениями Finance and Operations и Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f57a20ed56a761894b2cedf8835310dac098b098
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750626"
---
# <a name="integrated-vendor-master"></a>Интегрированный справочник поставщиков

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Термин *поставщик* относится к организации поставщика или к отдельному уполномоченному лицу, поставляющему товары или услуги для бизнеса. Хотя *поставщик* является устоявшейся концепцией в приложениях Microsoft Dynamics 365 Supply Chain Management, концепция поставщика не существует в приложениях на основе модели в Dynamics 365. Однако можно перегрузить таблицу **Организация/Контакт**, чтобы сохранить сведения о поставщике. В интегрированном сводном поставщике представлена явная концепция поставщика в приложениях на основе модели в Dynamics 365. Можно либо использовать новый дизайн поставщика, либо хранить данные поставщика в таблице **Организация/Контакт**. Двойная запись поддерживает оба подхода.

В обоих подходах данные поставщика интегрируются между Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service и порталами Power Apps. В Supply Chain Management данные доступны для рабочих процессов, таких как заявки на закупку и заказы на покупку.

## <a name="vendor-data-flow"></a>Поток данных поставщика

Если вы не хотите хранить данные поставщиков в таблице **Организация/Контакт** в Dataverse, можно использовать новый дизайн поставщика.

![Поток данных поставщика](media/dual-write-vendor-data-flow.png)

Если вы хотите продолжить хранить данные поставщиков в таблице **Организация/Контакт** , можно использовать расширенный дизайн поставщика. Чтобы использовать расширенный дизайн поставщиков, необходимо настроить рабочие-процессы поставщиков в пакете решения с двойной записью. Дополнительные сведения см. в разделе [Переключение между макетами поставщиков](vendor-switch.md).

![Поток расширенных данных поставщика](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Если порталы Power Apps используются для самообслуживания поставщиков, сведения о поставщике могут непосредственно поступать в приложения Finance and Operations.

## <a name="templates"></a>Шаблоны

Данные о поставщиках включают всю информацию о поставщике, например, группу поставщиков, адреса, контактную информацию, профиль платежа и профиль счета-фактуры. Коллекция сопоставлений таблиц работает совместно во время взаимодействия данных о поставщиках, как показано в следующей таблице.

Приложения Finance and Operations | Другие приложения Dynamics 365     | описание
----------------------------|-----------------------------|------------
Поставщик V2                   | Счет                     | Предприятия, которые используют таблицу организации для хранения информации о поставщиках, могут продолжать использовать ее таким же образом. Они также могут воспользоваться явной функциональностью поставщика, которая появляется из-за интеграции с приложениями Finance and Operations.
Поставщик V2                   | Msdyn\_vendors              | Компании, которые используют пользовательское решение для поставщиков, могут воспользоваться готовой концепцией поставщиков, которая вводится в Dataverse из-за интеграции с приложениями Finance and Operations. 
Группы поставщиков               | msdyn\_vendorgroups         | Этот шаблон синхронизирует информацию о группах поставщиков.
Метод платежа поставщикам       | msdyn\_vendorpaymentmethods | Этот шаблон синхронизирует информацию о способах оплаты поставщикам.
Контакты CDS V2             | контакты                    | Шаблон [контакты](customer-mapping.md#cds-contacts-v2-to-contacts) синхронизирует все первичные, вторичные и третичные контактные данные клиентов и поставщиков.
Строки графика платежей      | msdyn\_paymentschedulelines | Шаблон [строки графика платежей](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) синхронизирует ссылочные данные графиков как для клиентов, так и для поставщиков.
График оплаты            | msdyn\_paymentschedules     | Шаблон [графики оплаты](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) синхронизирует ссылочные данные графиков оплаты как для клиентов, так и для поставщиков.
Строки платежных дней CDS V2    | msdyn\_paymentdaylines      | Шаблон [строки дней оплаты](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) синхронизирует ссылочные данные строк дней оплаты как для клиентов, так и для поставщиков.
Платежные дни CDS            | msdyn\_paymentdays          | Шаблон [дни оплаты](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) синхронизирует ссылочные данные дней оплаты как для клиентов, так и для поставщиков.
Условия оплаты            | msdyn\_paymentterms         | Шаблон [условия оплаты](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) синхронизирует ссылочные данные условий оплаты как для клиентов, так и для поставщиков.
Аффиксы имен                | msdyn\_nameaffixes          | Шаблон [дополнения к наименованиям](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) синхронизирует ссылочные данные аффиксов имен как для клиентов, так и для поставщиков.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]