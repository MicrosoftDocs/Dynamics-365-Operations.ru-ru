---
title: Настройка среды для поиска справочника
description: В этом разделе объясняется, как настроить среду для использования функции поиска основных данных для Расчет налогов.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c4435dbfdb808a75b41a77d3c15d1c9fd29b266f353b1fbe18955ff985ab38bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718187"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Настройка среды для поиска справочника

[!include [banner](../includes/banner.md)]

В этом разделе объясняется, как настроить среду для использования функции поиска основных данных для Расчет налогов.

1. Настройте интеграцию Power Platform в Lifecycle Services (LCS). Дополнительные сведения см. в [Microsoft Power Platform интеграция — Обзор надстроек](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. Настройка Dynamics 365 Finance и Microsoft Dataverse. Дополнительные сведения см. в [Получение решения](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) и [Проверка подлинности и авторизация](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. Настройте следующие сущности. Дополнительные сведения см. в разделе [Включение виртуальных сущностей](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).
      - CompanyInfoEntity
      - CurrencyEntity
      - CustCustomerV3Entity
      - DeliveryTermsEntity
      - EcoResProductCategoryEntity
      - EcoResReleasedProductV2Entity
      - LogisticsAddressCityEntity
      - LogisticsAddressCountryRegionTranslationEntity
      - LogisticsAddressStateEntity
      - PurchProcurementChargeCDSEntity
      - SalesChargeCDSEntity
      - TaxGroupEntity
      - TaxItemGroupHeadingEntity
      - VendVendorV2Entity
4. Настройте Dynamics 365 Regulatory Configuration Service (RCS). 
5. Создайте запрос на обслуживание для Microsoft, чтобы включить в фокус-тестирование следующих функций:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. Перейдите к рабочей области **Управление функциями** и включите следующие функции:

      - (Предварительная версия) Поддержка источников данных Dataverse электронной отчетности
      - (Предварительная версия) Поддержка источников данных Dataverse налоговой службы
      - (Предварительная версия) Функции глобализации

5. Войдите в RCS с помощью учетной записи администратора клиента.
6. Перейдите к **Электронная отчетность** > **Подключенные приложения**. 
7. Выберите **Создать**, чтобы добавить запись, и введите следующие сведения в поле. 

   - В поле **Имя** введите имя.
   - В поле **Тип** выберите **Dataverse**.
   - В поле **Приложение** выберите ваш URL-адрес Dataverse.
   - В поле **Клиент** введите ваш клиент.
   - В поле **пользовательский URL-адрес** введите ваш URL-адрес Dataverse и добавьте к нему "/api/data/v9.1".

8. Выберите **Проверить подключение** и завершите процесс подключения. 

   [![Кнопка проверить подключение.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. Перейдите к **Электронная отчетность** > **Конфигурации налогов** и выполните импорт конфигурации налогов из [Конфигурации налогов](https://go.microsoft.com/fwlink/?linkid=2158352).

   [![Страница конфигурации налогов, дерево модели налоговых данных.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. Перейдите к **Сопоставление модели налогооблагаемого документа** или **Dataverse Сопоставление модели** при использовании конфигурации Microsoft, а в поле **Подключенное приложение** выберите запись, созданную на шаге 7.
11. Установите **По умолчанию для сопоставления модели** на **Да**.

   [![Страница сопоставления модели.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
