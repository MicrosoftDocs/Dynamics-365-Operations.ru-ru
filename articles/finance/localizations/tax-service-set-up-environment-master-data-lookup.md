---
title: Настройка среды для поиска справочника
description: В этом разделе объясняется, как настроить среду для использования функции поиска основных данных для Расчет налогов.
author: kai-cloud
ms.date: 10/26/2021
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
ms.openlocfilehash: 901f8bcb0220355866952b68e92bc2dd906bb430
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2021
ms.locfileid: "7700412"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Настройка среды для поиска справочника

[!include [banner](../includes/banner.md)]

В этом разделе объясняется, как настроить среду для использования функции поиска основных данных для Расчет налогов.

1. Настройте интеграцию Microsoft Power Platform в Microsoft Dynamics Lifecycle Services (LCS). Дополнительные сведения см. в [Microsoft Power Platform интеграция — Обзор надстроек](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). После выполнения этого шага появится название среды Microsoft Power Platform в разделе **Интеграция Power Platform**.
2. Перейдите в [центр администрирования Microsoft Power Platform](https://admin.powerplatform.microsoft.com/environments) и выберите имя среды. Предоставлен URL-адрес среды.
3. Настройка Dynamics 365 Finance и Dataverse. Дополнительные сведения см. в [Получение решения виртуальной сущности](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) и [Проверка подлинности и авторизация](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
4. Настройте следующие сущности. Дополнительные сведения см. в разделе [Включение виртуальных объектов Microsoft Dataverse](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

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

5. Настройка Regulatory Configuration Service (RCS). Откройте рабочую область **Управление функциями** и включите следующие функции:

    - Поддержка источников данных Dataverse электронной отчетности
    - Поддержка источников данных Dataverse налоговой службы
    - Функции глобализации

6. Войдите в RCS с помощью учетной записи администратора клиента.
7. Перейдите к **Электронная отчетность** > **Подключенные приложения**. 
8. Выберите **Создать**, чтобы добавить запись, и введите следующие сведения в поле. 

    - В поле **Имя** введите имя.
    - В поле **Тип** выберите **Dataverse**.
    - В поле **Приложение** выберите ваш URL-адрес Dataverse.
    - В поле **Клиент** введите ваш клиент.
    - В поле **пользовательский URL-адрес** введите ваш URL-адрес Dataverse и добавьте к нему "/api/data/v9.1".

9. Выберите **Проверить подключение** и завершите процесс подключения. 

    [![Кнопка проверить подключение.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. Перейдите к **Электронная отчетность** > **Конфигурации налогов** и выполните импорт конфигурации налогов из [Конфигурации налогов](https://go.microsoft.com/fwlink/?linkid=2158352).

    [![Страница конфигурации налогов, дерево модели налоговых данных.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. Перейдите к **Сопоставление модели налогооблагаемого документа** или **Dataverse Сопоставление модели** при использовании конфигурации Microsoft, а в поле **Подключенное приложение** выберите запись, созданную на шаге 7.
12. Установите **По умолчанию для сопоставления модели** на **Да**.

    [![Страница сопоставления модели.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
