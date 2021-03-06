---
title: Компоненты администрирования электронного выставления накладных
description: В этой теме приводятся сведения о компонентах, которые относятся к администрированию электронного выставления накладных.
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 081d23c85d3555210b54597920a49e800ffe284b
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980932"
---
# <a name="electronic-invoicing-administration-components"></a>Компоненты администрирования электронного выставления накладных

[!include [banner](../includes/banner.md)]


В этой теме приводятся сведения о компонентах, которые относятся к администрированию электронного выставления накладных. Здесь также приводятся сведения о настройке службы электронного выставления счетов.

## <a name="azure"></a>Azure

Используйте Microsoft Azure для создания секретов для хранилища ключей и учетной записи хранения. Затем используйте эти секреты в конфигурации электронного выставления накладных.

## <a name="lifecycle-services"></a>Lifecycle Services

Используйте Microsoft Dynamics Lifecycle Services (LCS), чтобы включить микрослужбы для вашего проекта развертывания LCS.

> [!NOTE]
> При установке микрослужбы в LCS требуется как минимум виртуальная машина уровня 2. Дополнительные сведения о планирования среды см. в разделе [Планирование среды](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Службы Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) — это интерфейс, который используется для настройки электронного выставления счетов. Ресурсы, такие как среды и функции электронного выставления накладных, создаются, поддерживаются и размещаются в RCS. Когда ресурсы готовы, они публикуются в службе электронного выставления накладных.

Для регистрации в RCS см [Regulatory services](https://marketing.configure.global.dynamics.com/).

Дополнительные сведения об RCS см. в разделе [Regulatory Configuration Services (RCS) — функции глобализации](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>Интеграция с электронным выставлением накладных 

Прежде чем можно будет использовать RCS для настройки электронных накладных, необходимо настроить RCS для обеспечения связи с электронным выставлением накладных. Эту настройку можно выполнить на вкладке **Электронное выставление накладных** на странице **Параметры электронной отчетности**.

#### <a name="service-endpoint"></a>Конечная точка службы

Электронное выставление накладных доступно в нескольких географических регионах центра обработки данных Azure. В приведенной ниже таблице содержится список доступности по регионам.

| География центров обработки данных Azure |
|----------------------------|
| США              |
| Европа                     |
| Великобритания             |
| Азия                       |

### <a name="service-environments"></a>Среды службы

Среды службы — это логические разделы, создаваемые для поддержки выполнения функций электронного выставления накладных в модуле электронного выставления накладных. Секреты безопасности и цифровые сертификаты, а также руководство (т. е., разрешения доступа) должны быть настроены на уровне среды службы.

Клиенты могут создавать столько сред служб, сколько необходимо. Все среды службы, которые создает клиент, независимы друг от друга.

Среды службы должны создаваться и поддерживаться в RCS. Когда среды службы готовы, они должны быть опубликованы в модуле электронного выставления накладных.

#### <a name="service-environment-status"></a>Состояние среды службы

Управление средами служб осуществляется через их состояние. Возможны следующие варианты:

- **Не опубликовано** — среда создана, но еще не была опубликована.
- **Опубликовано** — среда была опубликована в модуле электронного выставления накладных.
- **Изменено** — атрибуты опубликованной среды были изменены, но изменения еще не были опубликованы.

#### <a name="customer-secrets"></a>Секреты клиентов

Служба электронного выставления накладных отвечает за хранение всех ваших деловых данных в ресурсах Azure, принадлежащих вашей компании. Для обеспечения правильной работы службы и того, что все деловые данные, необходимые для модуля электронного выставления накладных и создаваемые ими, были доступны должным образом, необходимо создать два основных ресурса Azure:

- Учетная запись хранилища Azure (хранилище BLOB-объектов), в которой будут храниться электронные накладные
- Azure Key Vault, в котором будут храниться сертификаты и универсальный код ресурса (URI) учетной записи хранилища


Учетная запись Key Vault и хранилища клиента должна быть выделена специально для использования с электронным выставлением накладных. Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

Чтобы отслеживать работоспособность Key Vault и получать оповещения, настройте Azure Monitor для Key Vault. При включении ведения журнала Key Vault можно отслеживать, как осуществляется доступ к вашим основным хранилищам, когда и насколько доступны Key Vault. Дополнительные сведения см. в разделе [Мониторинг и оповещение для Azure Key Vault](/azure/key-vault/general/alert) и [Порядок включения ведения журнала Key Vault](/azure/key-vault/general/howto-logging?tabs=azure-cli).

Рекомендуется периодически изменять секреты. Дополнительные сведения см. в [документации по секретам](/azure/key-vault/secrets/).

#### <a name="users"></a>Пользователи

В каждой среде службы должны быть перечислены пользователи, которые могут подключаться из Dynamics 365 Finance и Dynamics 365 Supply Chain Management в электронном выставлении накладных.

#### <a name="publication"></a>Публикация

Среды службы должны быть опубликованы в модуле электронного выставления накладных, прежде чем их можно будет использовать. Только опубликованные среды могут быть доступны в Finance и Supply Chain Management. Кроме того, среда службы должна быть опубликована, прежде чем все обновления ее атрибутов вступят в силу для службы электронного выставления накладных.

### <a name="connected-applications"></a>Подключенные приложения

Подключенные приложения — это экземпляры Finance и Supply Chain Management, которые могут быть доступны через RCS. Кроме URL-адреса приложения и его клиента, подключенное приложение содержит учетные данные, позволяющие RCS подключиться к среде.

С помощью подключенных приложений можно настроить часть функции электронного выставления накладных в Finance и Supply Chain Management, чтобы сделать всю работу функции электронного выставления счетов.

## <a name="finance-and-supply-chain-management"></a>Finance и Supply Chain Management

### <a name="integration-with-electronic-invoicing"></a>Интеграция с электронным выставлением накладных

Прежде чем использовать Finance и Supply Chain Management для выдачи электронных накладных через модуль электронного выставления накладных, необходимо настроить его на разрешение связи со службой.

#### <a name="electronic-invoicing-integration-feature"></a>Функция интеграции электронного выставления накладных

Чтобы включить связь между Finance и Supply Chain Management и модулем электронного выставления накладных, следует включить функцию **Интеграция электронного выставления накладных** в рабочей области **Управление функциями**.

#### <a name="service-endpoint"></a>Конечная точка службы

Конечная точка службы — это URL-адрес, по которому расположен модуль электронного выставления накладных. Прежде чем можно будет выпускать электронные накладные, необходимо настроить конечную точку службы в Finance и Supply Chain Management, чтобы разрешить связь со службой.

Чтобы настроить конечную точку для службы, перейдите в раздел **Администрирование организации \> Настройка \> Параметр электронных документов** на вкладке **Службы отправки** в поле **URL-адрес электронного выставления накладных**, введите URL-адрес, как описано в таблице, описанной в разделе **Конечная точка службы**.

#### <a name="environments"></a>Среды

Имя среды, введенное в Finance и Supply Chain Management, относится к имени среды, созданной в RCS и опубликованной в модуле электронного выставления накладных.

Среда должна быть настроена на вкладке **Службы отправки** страницы **Параметры электронных документов**, чтобы каждый запрос на выпуск электронных накладных содержал среду, в которой модуль электронного выставления накладных может определить, какая функция электронного выставления накладных должна обработать запрос.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Настройка электронного выставления накладных в RCS](e-invoicing-configuration-rcs.md)
- [Выпуск электронных накладных в Finance и Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
