---
title: Возврат по заказу на возврат отклонен
description: В этой статье содержатся указания по устранению неполадок, которые могут помочь, когда возврат по заказу на возврат отклонен, так как кредитная карта, используемая для выставления накладной, отличается от карты, которая использовалась при исходной авторизации платежа.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: d8d1c40673d4b159a7b7bf00bf6011ba45f47edd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268241"
---
# <a name="refund-on-a-return-order-is-declined"></a>Возврат по заказу на возврат отклонен

[!include [banner](../../includes/banner.md)]

В этой статье содержатся указания по устранению неполадок, которые могут помочь, когда возврат по заказу на возврат отклонен, так как кредитная карта, используемая для выставления накладной, отличается от карты, которая использовалась при исходной авторизации платежа.

## <a name="description"></a>описание

Возврат отклоняется, если кредитная карта, используемая для выставления накладной для заказа на возврат, отличается от карты, которая использовалась во время исходной авторизации платежа. Будет выведено следующее сообщение об ошибке: "Некоторые платежи для разноски имеют неправильный статус. Перед выставлением накладных выполните повторную проверку статуса всех платежей".

Данные авторизации платежа будут включать следующее сообщение об ошибке: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"

![Ошибка отклонения возврата по заказу на возврат.](media/refund-order-decline.jpg)

## <a name="resolution"></a>Решение

### <a name="enable-blind-returns-in-adyen"></a>Включить возвраты вслепую в Adyen

Чтобы включить возвраты вслепую, выполните шаги, описанные в разделе [Устранение неполадок с соединитель платежей Dynamics 365 для Adyen](adyen-support.md), чтобы связаться с группой поддержки Adyen, и запросите, что функция возвратов вслепую должна быть включена на вашем счете Adyen.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Соединитель платежей Dynamics 365 для Adyen](../dev-itpro/adyen-connector.md)

[Настройка соединителя платежей Adyen для Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
