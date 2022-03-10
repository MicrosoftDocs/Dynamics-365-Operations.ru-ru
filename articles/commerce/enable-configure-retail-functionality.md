---
title: Инициализация начальных данных в новых средах Commerce
description: В этой статье описываются данные, создаваемые в процессе инициализации для Dynamics 365 Commerce.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 14d56636b48d8f8ff15863bb04c762e398f8c370664fbd52f80ed5f05f0e4895
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718739"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a>Инициализация начальных данных в новых средах Commerce

[!include [banner](includes/banner.md)]

В этой статье описываются данные, создаваемые в процессе инициализации для Dynamics 365 Commerce.

После развертывания решения Commerce посредством Microsoft Dynamics Lifecycle Services (LCS) необходимо инициализировать конфигурацию Commerce, чтобы создать базовые данные конфигурации.

> [!IMPORTANT]
> Прежде чем инициализировать конфигурацию Commerce, убедитесь, что вы указали язык и почтовый адрес для каждого юридического лица, в котором вы будете настраивать магазины. Этот шаг необходимо выполнить для каждого юридического лица, которое вы используете для Commerce.

Чтобы инициализировать конфигурацию, выполните следующие действия.

1. Запустите клиент Commerce.
2. Перейдите в раздел **Retail и Commerce** &gt; **Настройка Headquarters** &gt; **Параметры** &gt; **Параметры Commerce**.
3. Щелкните **Инициализировать**.

В результате инициализации создаются следующие данные конфигурации по умолчанию:

- Задания и подзадания планировщика Commerce
- Схема канала коммерции
- Графики распределения Commerce
- Макеты экранов по умолчанию, которые включают в себя сетки кнопок, изображения и темы
- Информация о часовом поясе
- POS-операции
- POS-разрешения
- Отчеты по каналу
- Метаданные атрибута
- Шаблоны проверки объектов
- Пакетное задание для очистки истории сессии Commerce Data Exchange

Кроме того, для базы данных Commerce включается ведение журналов, связанных с платежными картами (PCI).

> [!NOTE]
> Также предусмотрен параметр, позволяющий отдельно сконфигурировать планировщик Commerce. Этот параметр позволяет сбросить конфигурацию планировщика Commerce к его настройкам по умолчанию.

После завершения инициализации необходимо сконфигурировать дополнительные данные Commerce. Далее приводятся некоторые примеры.

- Параметры коммерции
- Параметры планировщика коммерции
- Каналы Commerce
- Регистры и устройства
- Ассортименты


[!INCLUDE[footer-include](../includes/footer-banner.md)]