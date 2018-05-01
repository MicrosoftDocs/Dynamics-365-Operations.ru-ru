---
title: "Печать в приложениях Finance and Operations"
description: "В Microsoft Dynamics 365 for Finance and Operations можно печатать документы с помощью локального принтера или устройства, подключенного к сети. В этой статье представлен обзор того, как печатаются документы."
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro, Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 30a418e6c49849369f0a0e3ffa28f31b9b88b7e7
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="printing-in-finance-and-operations-applications"></a>Печать в приложениях Finance and Operations

[!INCLUDE [banner](../includes/banner.md)]

В Microsoft Dynamics 365 for Finance and Operations можно печатать документы с помощью локального принтера или устройства, подключенного к сети. В этой статье представлен обзор того, как печатаются документы.

<a name="printing-overview"></a>Общие сведения о печати
-----------------

Microsoft Dynamics 365 for Finance and Operations предоставляет интегрированные службы и клиентские приложения, которые позволяют легко создавать, сохранять и распространять документы, которые поддерживают деловую деятельность. В Finance and Operations можно печатать документы с помощью локального принтера или устройства, подключенного к сети. Кроме того, можно экспортировать страницы и отчеты Finance and Operations непосредственно из клиента в виде PDF-файлов или документов Microsoft Office. Наконец, распределенная рабочая нагрузка позволяет печатать бизнес-документы непосредственно с мобильных устройств с использованием сетевых ресурсов. Несмотря на то, что требования печати могут быть различными, во всех отраслях обычно необходимо создавать бумажные копии деловых документов, используя Finance and Operations. Печать документов на сетевых устройствах из размещенных приложений представляет уникальный набор задач. Далее приводятся некоторые примеры.

-   Драйверы печати могут быть недоступны на устройстве пользователя.
-   Устройство пользователя может быть не подключено к сети организации.

Используя выделенный хост и выполнив несколько простых шагов, системные администраторы могут настроить развертывания таким образом, что пользователи смогут выполнять печать непосредственно из бизнес-приложений на сетевых устройствах.

### <a name="printing-scenarios-in-finance-and-operations-applications"></a>Сценарии печати в приложениях Finance and Operations

В следующей таблице описываются три основных варианта печати с помощью приложений Finance and Operations.

| Сценарий                        | Цель                                                      | Решение                                                                                                            |
|---------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 1. Печать того, что вы видите        | Печать содержимого, в данный момент отображаемого в браузере.             | Предназначенная для печати версия веб-страницы создается для браузера.                                             |
| 2. Интерактивная печать         | Печать точного документа на локально подключенном устройстве. | Можно экспортировать PDF-версию отчета и загрузить ее в веб-браузер.                                          |
| 3. Печать на сетевом устройстве | Отправка точного документа на принтер домена.     | Точный документ отправляется в клиентское приложение, которое выполняется на сервере, который размещен в домене клиента. |

Поскольку решения разные в зависимости от сценария, приложения Finance and Operations содержат встроенные службы и инструменты, чтобы помочь пользователям достигать своих целей:

-   **Сценарий 1** поддерживается при отображении HTML5-клиента в браузере.
-   **Сценарий 2** использует клиентских приложений и службы Microsoft Office 365.
-   **Сценарий 3** требует поддержки от клиентских приложений и служб, размещенных в Microsoft Azure.

В дополнение к платформе, которая развертывается в подписке Azure, приложения Finance and Operations обеспечивают клиентам интегрированное приложение Azure первой стороны, которое помогает клиентам легче контролировать использование устройств, размещенных в домене, для печати документов.

## <a name="service-overview"></a>Обзор службы
Пока документы, производимые размещенными приложениями, ожидаются печати на устройстве, подключенном к сети, они хранятся в хранилище BLOB-объектов Azure. [Агент маршрутизации документов](install-document-routing-agent.md) использует проверку подлинности Azure для установления безопасного канала со службами Azure. **Последовательность выполнения**

1.  Отчет формируется службами по Microsoft SQL Server Reporting Services (SSRS) и хранится в хранилище BLOB-объектов Azure. Приложенные настройки принтера хранятся вместе с документом.
2.  Агент маршрутизации документов запрашивает в очереди шины служб Azure активное задание.
3.  Документ загружается агентом маршрутизации документов и помещается в очередь печати сетевого принтера.

Решение на основе клиента позволяет клиентам управлять масштабом их потребностей в печати. Клиенты с большим объемом печати могут установить много агентов маршрутизации документов для увеличения числа одновременных операций печати. Другим клиентам требуется очень мало установок агента маршрутизации документов для обработки их ожидаемой потребности в печати.

### <a name="service-components-for-network-printing"></a>Компоненты службы для сетевой печати

На следующей схеме показаны основные компоненты, которые помогают поддерживать операции сетевой печати. [![компоненты-службы-для-сетевой-печати\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png) Обратите внимание, что один принтер может быть зарегистрирован с несколькими агентами маршрутизации документов. Чтобы решить настройки принтера, размещенная служба использует сетевой путь, который уникально идентифицирует каждый сетевой принтер. В результате даже в том случае, если принтер зарегистрирован несколькими клиентами, он отображается как один элемент в списке принтеров, доступных в приложениях Finance and Operations.



