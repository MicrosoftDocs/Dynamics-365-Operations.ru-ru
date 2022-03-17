---
title: При создании новых клиентов приветственное сообщение электронной почты не отправляется
description: В этой теме содержатся указания по устранению неполадок, которые могут помочь в том случае, если приветственное уведомление по электронной почте не отправлено при создании нового клиента в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349958"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>При создании новых клиентов приветственное сообщение электронной почты не отправляется

[!include [banner](../../includes/banner.md)]

В этой теме содержатся указания по устранению неполадок, которые могут помочь в том случае, если приветственное уведомление по электронной почте не отправлено при создании нового клиента в Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Описание

Когда в Commerce headquarters создается новый клиент, приветственное сообщение электронной почты не отправляется клиенту даже в том случае, когда уведомление по электронной почте настроено для типа уведомления по электронной почте **Создано клиентом**.

## <a name="resolution"></a>Решение

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>Задание правильного значения кода электронной почты для типа созданного клиентом уведомления по электронной почте

Чтобы задать правильное значение параметра **Код электронной почты** для типа уведомления по электронной почте **Создано клиентом**, в Headquarters выполните следующие действия.

1. Перейдите к **Retail и Commerce \> Настройка Headquarters \> Профиль уведомления по электронной почте Commerce**.
1. В области переходов слева выберите профиль уведомления по электронной почте.
1. В разделе **Параметры уведомлений о событии Retail** для типа уведомлений по электронной почте **Создано клиентом** задайте для поля **Код электронной почты** значение **NewCust**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка профиля уведомлений по электронной почте](../email-notification-profiles.md)
