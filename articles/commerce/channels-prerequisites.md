---
title: Необходимые условия для настройки каналов
description: В этом разделе представлен обзор необходимых условий настройки каналов в Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0da0457240cf12686fff2fa929c7fb510c11f242
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415197"
---
# <a name="channel-setup-prerequisites"></a>Необходимые условия для настройки каналов


[!include [banner](includes/banner.md)]

В этом разделе представлен обзор необходимых условий настройки канала в Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Прежде чем можно будет создать канал Dynamics 365 Commerce, необходимо выполнить несколько предварительных условий. Следующие списки необходимых условий упорядочены по типам каналов.

> [!NOTE]
> Документация по-прежнему записывается, и ссылки будут обновляться по мере публикации нового содержимого.

## <a name="initialization"></a>Инициализация

- [Инициализация начальных данных](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Глобальные необходимые условия для всех типов каналов

- [Определение и настройка структуры юридического лица](channels-legal-entities.md) 
- [Настройка своей организационной иерархии](channels-org-hierarchies.md)
- [Настройка склада](channels-setup-warehouse.md)
- [Настройка налога](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [Настройка профиля уведомлений по электронной почте](email-notification-profiles.md)
- [Настройка номерных серий](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [Настройка клиента по умолчанию и адресной книги](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Необходимые условия для каналов розничной торговли

- [Инфокоды и группы инфокодов](info-codes-retail.md)
- [Настройка профиля функциональности для розничной торговли](retail-functionality-profile.md)
- [Настройка адресной книги сотрудников](new-address-book.md)
- [Настройка макета экрана](pos-screen-layouts.md)
- [Настройка станции оборудования](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>Необходимые условия для канала центра обработки вызовов

- Параметры центра обработки вызовов
- [Заказ центра обработки вызовов и способы оплаты возврата денежных средств](work-with-payments.md)
- [Режимы центра обработки вызовов для доставки и накладных расходов](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>Необходимые условия для каналов онлайн-торговли

- [Создание профиля функциональности для онлайн-торговли](online-functionality-profile.md)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор каналов](channels-overview.md)

[Обзор организаций и организационных иерархий](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Настройка организационных иерархий](channels-org-hierarchies.md)

[Создание юридических лиц](channels-legal-entities.md)

[Настройка канала розничной торговли](channel-setup-retail.md)
    
[Настройка интернет-канала](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]