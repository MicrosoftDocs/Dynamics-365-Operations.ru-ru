---
title: Возврат для модуля отправки
description: В этой статье описывается модуль прибытия для отправки, а также описывается, как настраивать его в Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 7002db893da1802063148a9b800ffa92f3e5f065
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885483"
---
# <a name="check-in-for-pickup-module"></a>Возврат для модуля отправки

[!include [banner](includes/banner.md)]

В этой статье описывается модуль прибытия для отправки, а также описывается, как настраивать его в Microsoft Dynamics 365 Commerce.

Модуль прибытия для отправки содержит страницу подтверждения для клиентов, использующих возможности прибытия клиента Dynamics 365 Commerce для уведомления магазина о своем прибытии. Модуль прибытия для отправки также позволяет настроить форму, которая собирает дополнительную информацию от клиентов, чтобы упростить доставку заказа. Эти сведения включают номер места парковки клиента, а также марку и модель автомобиля. 

## <a name="module-properties"></a>Свойства модуля

| Имя свойства | Значения | описание |
|---------------|--------|-------------|
| Текст подтверждения | Текстовая строка | Содержимое заголовка, которое отображается на странице подтверждения прибытия. |
| Показать QR-код | **True** или **False** | Если это свойство задано как **Истина**, страница подтверждения прибытия показывает QR-код, который представляет код подтверждения заказа. |
| Заголовок дополнительных сведений | Текстовая строка | Содержимое заголовка, которое появляется при настройке полей дополнительных сведений. |
| Ключи дополнительных сведений | Пара код ресурса/значение ресурса | Каждый ключ создает поле формы и связанную с ним метку, которые используются для сбора дополнительной информации от клиентов. |
| Ключ дополнительных сведений \> код ресурса | Текстовая строка | Каждый ключ информации создает поле формы и связанную с ним метку, которые используются для сбора дополнительной информации от клиентов. Это свойство определяет ключ дополнительной информации. В задаче, созданной в POS, значение этого свойства отображается как метка в поле инструкций. |
| Ключ дополнительных сведений \> Значение ресурса | Текстовая строка | Метка для текстового поля в задаче в POS. |
| Ключи дополнительных сведений \> Требуемый | **True** или **False** | Это свойство определяет, должны ли клиенты заполнять поле формы до того, как они смогут продолжать работу. Если это свойство имеет значение **Истина**, рядом с подписью формы отображается звездочка, а проверка пустого значения выполняется, чтобы предотвратить продолжение работы клиента, если не введено значение. |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a>Добавление модуля прибытия для отправки на страницу

Модуль прибытия для отправки необходимо добавить на новую страницу, созданную для подтверждения прибытия. Эта страница будет служить в качестве подтверждения прибытия для клиентов, которые выбирают **Я здесь** или кнопку в их электронной почте. 

## <a name="configure-the-additional-information-form"></a>Настройка формы дополнительной информации

По умолчанию, если не настроены ключи дополнительной информации, в модуле отображается страница подтверждения прибытия клиента. Когда отображается подтверждение прибытия, в POS создается задача для магазина, в котором выполняется комплектация заказа.

Когда настроен один или несколько ключей дополнительной информации, клиентам сначала выводится запрос на ввод данных. При выборе **Отправить** они отображаются с подтверждением прибытия, и задача создается в POS. 

## <a name="additional-resources"></a>Дополнительные ресурсы

[Включение уведомлений о прибытии клиентов в POS](enable-customer-check-in.md)
