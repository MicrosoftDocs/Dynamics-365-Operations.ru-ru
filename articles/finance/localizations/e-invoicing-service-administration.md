---
title: Компоненты администрирования электронного выставления накладных
description: В этой теме приводятся сведения о компонентах, которые относятся к администрированию электронного выставления накладных.
author: gionoder
ms.date: 08/31/2021
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
ms.openlocfilehash: d187e8a03552258099d7021ff056d0726ea60ca1
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463889"
---
# <a name="electronic-invoicing-administration-components"></a>Компоненты администрирования электронного выставления накладных

[!include [banner](../includes/banner.md)]


В этой теме приводятся сведения о компонентах, которые относятся к администрированию электронного выставления накладных. Здесь также приводятся сведения о настройке службы электронного выставления счетов.

## <a name="azure"></a>Azure

Используйте Microsoft Azure для создания секретов для хранилища ключей и настройки учетной записи хранения. Затем используйте секреты хранилища ключей и маркер SAS учетной записи хранения в конфигурации электронного выставления накладных.

## <a name="lifecycle-services"></a>Lifecycle Services

Используйте Microsoft Dynamics Lifecycle Services (LCS), чтобы включить надстройку "Электронное выставление счетов" для вашего проекта развертывания LCS.

> [!NOTE]
> При установке надстроек в LCS требуется как минимум **Среда уровня 2**. Дополнительные сведения о планирования среды см. в разделе [Планирование среды](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Службы Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) — это интерфейс, который используется для настройки электронного выставления счетов. Ресурсы, такие как среды и функции электронного выставления накладных, создаются, поддерживаются и размещаются в RCS. Когда ресурсы готовы, они публикуются в службе электронного выставления накладных.

Для регистрации в RCS см [Regulatory services](https://marketing.configure.global.dynamics.com/).

Дополнительные сведения об RCS см. в разделе [Regulatory Configuration Services (RCS) — функции глобализации](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>Интеграция с электронным выставлением накладных 

Прежде чем можно будет использовать RCS для настройки электронных накладных, необходимо настроить RCS для обеспечения связи с электронным выставлением накладных. Эту настройку можно выполнить на вкладке **Электронное выставление накладных** на странице **Параметры электронной отчетности**.

#### <a name="service-endpoint"></a><a id='svc-endpoint-uris'></a>Конечная точка службы

Электронное выставление накладных доступно в нескольких географических регионах центра обработки данных Azure. В приведенной ниже таблице содержится список доступности по регионам.


| География центра обработки данных Azure | Универсальный код ресурса (URI) конечной точки службы                                                       |
|----------------------------|----------------------------------------------------------------------------|
| Соединенные штаты              | <p>https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing</p> |
| Европа                     | <p>https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Соединенное Королевство             | <p>https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Азия                       | <p>https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |

### <a name="service-environments"></a>Среды службы

Среды службы — это логические разделы, создаваемые для поддержки выполнения функций глобализации в модуле электронного выставления накладных. Секреты безопасности и цифровые сертификаты, а также руководство (т. е., разрешения доступа) должны быть настроены на уровне среды службы.

Клиенты могут создавать столько сред служб, сколько необходимо. Все среды службы, которые создает клиент, независимы друг от друга.

Среды службы должны создаваться и поддерживаться в RCS. Когда среды службы готовы, они должны быть опубликованы в модуле электронного выставления накладных.

#### <a name="service-environment-status"></a>Состояние среды службы

Управление средами служб осуществляется через их состояние. Возможны следующие варианты:

- **Не опубликовано** — среда создана, но еще не была опубликована.
- **Опубликовано** — среда была опубликована в модуле электронного выставления накладных.
- **Изменено** — атрибуты опубликованной среды были изменены, но изменения еще не были опубликованы.

#### <a name="customer-secrets"></a>Секреты клиентов

Служба электронного выставления накладных отвечает за хранение всех ваших деловых данных в ресурсах Azure, принадлежащих вашей компании. Для обеспечения правильной работы службы и того, что все деловые данные, необходимые для модуля электронного выставления накладных и создаваемые ими, были доступны должным образом, необходимо создать два основных ресурса Azure:

- Учетная запись хранения Azure (хранилище BLOB-объектов), которая будет хранить электронные документы, включая электронные накладные, результаты преобразований документов и отклики от внешних веб-служб.
- Azure Key Vault, в котором будут храниться сертификаты и универсальный код ресурса (URI) учетной записи хранилища (маркер SAS).


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

Чтобы настроить конечную точку для службы, перейдите в раздел **Администрирование организации \> Настройка \> Параметры электронных документов** на вкладке **Электронное выставление накладных** в поле **URL-адрес конечной точки**, введите соответствующий URL-адрес из таблицы в разделе [Конечная точка службы](#svc-endpoint-uris) выше в этом разделе.

#### <a name="environments"></a>Среды

Имя среды, введенное в Finance и Supply Chain Management, относится к имени среды, созданной в RCS и опубликованной в модуле электронного выставления накладных.

Среда должна быть настроена на вкладке **Электронное выставление накладных** на странице **Параметры электронных документов**. Таким образом, каждый запрос на выпуск электронных накладных содержит среду, в которой электронное выставление накладных может определить, какая электронная накладная должна обработать запрос.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Настройка электронного выставления накладных в RCS](e-invoicing-configuration-rcs.md)
- [Выпуск электронных накладных в Finance и Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
