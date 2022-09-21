---
title: Вопросы и ответы об асинхронном режиме создания клиента
description: Эта статья содержит ответы на часто задаваемые вопросы об асинхронном режиме создания клиента Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: bd5741aeb3278f1d40d63bb02ca57571a907dc21
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474078"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Вопросы и ответы об асинхронном режиме создания клиента

[!include [banner](includes/banner.md)]

Эта статья содержит ответы на часто задаваемые вопросы об асинхронном режиме (async) создания клиента Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>Почему мне не удается включить функцию "Включить изменение клиентов в асинхронном режиме"?

Перед включением функции **Включить изменение клиентов в асинхронном режиме** необходимо включить следующие функции:

- Повышение производительности при работе с заказами клиентов и проводками клиентов
- Включить расширенное асинхронное создание клиента
- Включить асинхронное создание для адресов клиентов

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>Почему я по-прежнему вижу вызовы служб Real-time Service для Commerce headquarters после включения функции "Включить изменение клиентов в асинхронном режиме"?

Эта проблема возникает, если задания Commerce Data Exchange (CDX) не были запущены, чтобы гарантировать синхронизацию состояния функции и других метаданных канала с каналом. Перед повторной попыткой выполнения сценария убедитесь, что в Commerce headquarters выполняются следующие задания CDX:

- 1110 (Глобальная конфигурация)
- 1010 (Клиенты)
- 1070 (Конфигурация канала)

Данные, которые кэшируются в Commerce Scale Unit (CSU), могут не сразу отражаться в Commerce headquarters после запуска заданий CDX.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Почему в Commerce headquarters не отображается создание или обновление клиентов с POS-терминала или из канала электронной коммерции?

Убедитесь, что указанные ниже действия выполнены в том порядке, в котором они перечислены здесь.

1. Выполните P-задание CDX в Commerce headquarters, чтобы обеспечить Commerce headquarters доступ к асинхронным данным клиентов, сохраненным в таблицах **RETAILASYNCCUSTOMERV2**, **RETAILASYNCADDRESSV2**, **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMERAFFILIATION** и **RETAILASYNCCUSTOMERATTRIBUTEV2**.
1. Выполните пакетное задание **Синхронизация клиентов и запросов каналов** в Commerce Headquarters. После успешного выполнения пакетного задания для всех записей из вышеперечисленных таблиц, которые были успешно обработаны, в поле **OnlineOperationCompleted** будет установлено значение **1**.
