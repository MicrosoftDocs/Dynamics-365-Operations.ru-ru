---
title: Настройка программ непрерывности для центров обработки вызовов
description: В этом статье описывается, как настроить программу непрерывности для центра обработки вызовов.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 39c3e6d740bff2af27a2fba2ac4c406c01b43a87218fdc1dcfe094c147cd3de3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716158"
---
# <a name="set-up-continuity-programs-for-call-centers"></a>Настройка программ непрерывности для центров обработки вызовов

[!include [banner](includes/banner.md)]

В этом статье описывается, как настроить программу непрерывности для центра обработки вызовов.

Согласно программе непрерывности, которая также называется программой повторяющихся заказов, клиенты получают регулярные отгрузки продукта в соответствии с предопределенным графиком. Каждая отгрузка может содержать разные продукты, как в случае книжного клуба, предлагающего новую книгу каждый месяц, или один и тот же продукт. Для настройки программы непрерывности выполните следующие задачи.

1. Настройте параметры непрерывности на странице **Параметры центра обработки вызовов**.
2. Создайте программу непрерывности, в которой определяются сведения, такие как график оплаты, время отгрузки и возможность предварительного выставления накладных. Также необходимо добавить список продуктов, включенных в программу непрерывности. Каждый продукт получает идентификационный код события, назначаемый последовательно, начиная с 1. Коды событий определяют порядок отправки продуктов.

    - Если клиенты получают разные продукты в каждой отгрузке, продукты отправляются в последовательном порядке в соответствии с их кодами событий, начиная с текущего события.
    - Если клиенты получают одинаковый продукт в каждой отгрузке, в списке содержится только один продукт, который имеет один код события. Одно и то же событие происходит повторно. Можно определить, сколько раз повторять каждое событие.

3. Создайте родительский продукт, представляющий программу непрерывности, созданную в ходе задачи 2. При добавлении этого продукта в заказ на продажу откроется страница **Непрерывность**. Затем эту страницу можно использовать для создания фактического непрерывного заказа. Родительский продукт не определяет отдельные продукты, которые клиент получает в каждой отгрузке.

После настройки программы непрерывности, как описано в разделе выше, можно создать непрерывный заказ для клиента. Можно также выполнить следующие дополнительные задачи обслуживания.

- **Обновление периода текущего события непрерывности** — настройка пакетного задания для сообщения системе о периоде текущего события.
- **Создание дочерних непрерывных заказов** — создание дочерних заказов из родительского непрерывного заказа.
- **Обработка платежей непрерывности** — обработка выставления накладных и уведомлений для платежей, связанных с непрерывными заказами на продажу.
- **Расширение строк непрерывности** (при необходимости) — увеличение количества повторов события непрерывности. Количество повторов отгрузки можно увеличить, превысив лимит, установленный в поле **Порог повторения непрерывности** в параметрах центра обработки вызовов.
- **Выполнение обновления непрерывности** (при необходимости)— синхронизация изменений между программой непрерывности и непрерывными родительскими заказами на продажу.
- **Закрытие строк и заказов родительского объекта непрерывности** — закрытие непрерывных заказов.


[!INCLUDE[footer-include](../includes/footer-banner.md)]