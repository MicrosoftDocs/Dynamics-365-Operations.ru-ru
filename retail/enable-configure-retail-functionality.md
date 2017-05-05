---
title: "Инициализация начальных данных в новой среде розничной торговли"
description: "В этой статье описываются данные, создаваемые в процессе инициализации для Microsoft Dynamics 365 for Operations - Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Инициализация начальных данных в новой среде розничной торговли

[!include[banner](includes/banner.md)]


В этой статье описываются данные, создаваемые в процессе инициализации для Microsoft Dynamics 365 for Operations - Retail.

После развертывания решения "Розничная торговля" посредством Microsoft Dynamics Lifecycle Services (LCS) необходимо инициализировать конфигурацию розничной торговли, чтобы создать базовые данные конфигурации. **Важно:** прежде чем инициализировать конфигурацию розничной торговли, убедитесь, что вы указали язык и почтовый адрес для каждого юридического лица, в котором вы будете настраивать розничные магазины. Этот шаг необходимо выполнить для каждого юридического лица, которое вы используете для розничной торговли. Чтобы инициализировать конфигурацию розничной торговли, выполните следующие действия.

1.  Запустите клиент Dynamics 365 for Operations.
2.  Выберите **Розничная торговля и коммерция** &gt; **Настройка центрального офиса** &gt; **Параметры** &gt; **Параметры розничной торговли**.
3.  Щелкните **Инициализировать**.

В результате инициализации создаются следующие данные конфигурации по умолчанию:

-   Задания и подзадания планировщика розничной торговли
-   Схема канала розничной торговли
-   Графики распределения розничной торговли
-   Макеты экранов по умолчанию, которые включают в себя сетки кнопок, изображения и темы
-   Информация о часовом поясе
-   POS-операции
-   POS-разрешения
-   Отчеты по каналу
-   Метаданные атрибута
-   Шаблоны проверки объектов
-   Пакетное задание для очистки истории сессии Commerce Data Exchange

Кроме того, для базы данных Dynamics 365 for Operations включается ведение журналов, связанных с платежными картами (PCI). **Примечание.** Также предусмотрен параметр, позволяющий отдельно сконфигурировать планировщик розничной торговли. Этот параметр позволяет сбросить конфигурацию планировщика розничной торговли к его настройкам по умолчанию. После завершения инициализации необходимо сконфигурировать дополнительные данные розничной торговли. Далее приводятся некоторые примеры.

-   Параметры розничной торговли
-   Параметры модуля "Розничная сеть - Планировщик"
-   Каналы розничной торговли
-   Регистры и устройства
-   Ассортименты




