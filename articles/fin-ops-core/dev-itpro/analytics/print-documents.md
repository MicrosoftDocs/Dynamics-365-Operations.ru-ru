---
title: Обзор печати документов
description: Можно печатать документы с помощью локального принтера или устройства, подключенного к сети. В этой статье представлен обзор того, как печатаются документы.
author: RichdiMSFT
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 69161,  ""intro-internal
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.openlocfilehash: 840a635af14e5140834e5c1d2b319d0c8c4bff14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280875"
---
# <a name="document-printing-overview"></a>Обзор печати документов

[!include [banner](../includes/banner.md)]

Можно печатать документы с помощью локального принтера или устройства, подключенного к сети. В этой статье представлен обзор того, как печатаются документы.

## <a name="printing-overview"></a>Общие сведения о печати

Приложение предоставляет интегрированные службы и клиентские приложения, которые позволяют легко создавать, сохранять и распространять документы, которые поддерживают деловую деятельность. Можно печатать документы с помощью локального принтера или устройства, подключенного к сети. Кроме того, можно экспортировать страницы и отчеты непосредственно из клиента в виде PDF-файлов или документов Microsoft Office. Наконец, распределенная рабочая нагрузка позволяет печатать бизнес-документы непосредственно с мобильных устройств с использованием сетевых ресурсов. Несмотря на то, что требования печати могут быть различными, во всех отраслях обычно необходимо создавать бумажные копии деловых документов, используя приложение. Печать документов на сетевых устройствах из размещенных приложений представляет уникальный набор задач. Далее приводятся некоторые примеры.

- Драйверы печати могут быть недоступны на устройстве пользователя.
- Устройство пользователя может быть не подключено к сети организации.

Используя выделенный хост и выполнив несколько простых шагов, системные администраторы могут настроить развертывания таким образом, что пользователи смогут выполнять печать непосредственно из бизнес-приложений на сетевых устройствах.

### <a name="application-printing-scenarios"></a>Сценарии печати из приложений 

В следующей таблице описаны три основных сценария печати.

| Сценарий                        | Цель                                                      | Решение |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Печать того, что вы видите        | Печать содержимого, в данный момент отображаемого в браузере.             | Для браузера создается предназначенная для печати версия веб-страницы. |
| 2. Интерактивная печать         | Печать точного документа на локально подключенном устройстве. | Можно экспортировать PDF-версию отчета и загрузить ее в веб-браузер. |
| 3. Печать на сетевом устройстве | Отправка точного документа на принтер домена.     | Точный документ отправляется в клиентское приложение, которое выполняется на сервере, размещенном в домене клиента. |

Поскольку решения разные в зависимости от сценария, приложения содержат встроенные службы и инструменты, чтобы помочь пользователям достигать своих целей:

- **Сценарий 1** поддерживается при отображении HTML5-клиента в браузере.
- **Сценарий 2** использует клиентских приложений и службы Microsoft 365.
- **Сценарий 3** требует поддержки от клиентских приложений и служб, размещенных в Microsoft Azure.

В дополнение к платформе, которая развертывается в подписке Azure, приложения для управления финансами и операциями обеспечивают клиентам интегрированное приложение Azure первой стороны, которое помогает клиентам легче контролировать использование устройств, размещенных в домене, для печати документов.

## <a name="service-overview"></a>Обзор службы
Пока документы, производимые размещенными приложениями, ожидаются печати на устройстве, подключенном к сети, они хранятся в хранилище BLOB-объектов Azure. [Установка агента маршрутизации документов для включения сетевой печати](install-document-routing-agent.md) использует проверку подлинности Azure для установления безопасного канала со службами Azure.

**Последовательность выполнения**

1. Отчет формируется службами по Microsoft SQL Server Reporting Services (SSRS) и хранится в хранилище BLOB-объектов Azure. Приложенные настройки принтера хранятся вместе с документом.
2. Агент маршрутизации документов запрашивает в очереди шины служб Azure активное задание.
3. Документ загружается агентом маршрутизации документов и помещается в очередь печати сетевого принтера.

Решение на основе клиента позволяет клиентам управлять масштабом их потребностей в печати. Клиенты с большим объемом печати могут установить много агентов маршрутизации документов для увеличения числа одновременных операций печати. Другим клиентам требуется очень мало установок агента маршрутизации документов для обработки их ожидаемой потребности в печати.

### <a name="service-components-for-network-printing"></a>Компоненты службы для сетевой печати

На следующей схеме показаны основные компоненты, которые помогают поддерживать операции сетевой печати.

[![service-components-for-network-printing\_2016.](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Обратите внимание, что один принтер может быть зарегистрирован с несколькими агентами маршрутизации документа. Чтобы решить настройки принтера, размещенная служба использует сетевой путь, который уникально идентифицирует каждый сетевой принтер. В результате даже в том случае, если принтер зарегистрирован несколькими клиентами, он отображается как один элемент в списке принтеров, доступных в приложениях.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
