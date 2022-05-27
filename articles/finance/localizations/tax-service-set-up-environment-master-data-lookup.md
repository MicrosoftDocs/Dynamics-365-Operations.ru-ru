---
title: Включение подстановки основных данных для конфигурации расчета налога
description: В этой теме объясняется, как настроить и включить функцию подстановки основных данных для расчета налогов.
author: kai-cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7640144b1687fc64e55f659d49cdb0817c17294a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686721"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Включение подстановки основных данных для конфигурации расчета налога 

[!include [banner](../includes/banner.md)]

В этой теме объясняется, как настроить и включить функцию подстановки основных данных для расчета налогов. Раскрывающийся список доступен для выбора значений в конфигурации расчета налогов для таких полей , как **Юридическое лицо**, **Счет поставщика**, **Код номенклатуры** и **Условия поставки**. Эти значения берутся из связанной среды Microsoft Dynamics 365 Finance, использующей источник данных Microsoft Dataverse.

> [!NOTE] 
> Функция подстановки основных данных в расчете налога является дополнительной функциональностью. Можно пропустить следующие шаги, если отключить функцию **Поддержка источника данных налоговой службы Dataverse** в Regulatory Configuration Service (RCS). Однако в этом случае раскрывающийся список не будет доступен в конфигурации расчета налогов.

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
