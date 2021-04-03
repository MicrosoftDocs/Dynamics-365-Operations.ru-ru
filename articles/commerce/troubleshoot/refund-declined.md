---
title: Возврат по заказу на возврат отклонен
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь, когда возврат по заказу на возврат отклонен, так как кредитная карта, используемая для выставления накладной, отличается от карты, которая использовалась при исходной авторизации платежа.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e202c6b4b9e025d5af1cd5eb6235884aab6444e6
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585507"
---
# <a name="refund-on-a-return-order-is-declined"></a>Возврат по заказу на возврат отклонен

[!include [banner](../../includes/banner.md)]

В этом разделе содержатся указания по устранению неполадок, которые могут помочь, когда возврат по заказу на возврат отклонен, так как кредитная карта, используемая для выставления накладной, отличается от карты, которая использовалась при исходной авторизации платежа.

## <a name="description"></a>описание

Возврат отклоняется, если кредитная карта, используемая для выставления накладной для заказа на возврат, отличается от карты, которая использовалась во время исходной авторизации платежа. Будет выведено следующее сообщение об ошибке: "Некоторые платежи для разноски имеют неправильный статус. Перед выставлением накладных выполните повторную проверку статуса всех платежей".

Данные авторизации платежа будут включать следующее сообщение об ошибке: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"

![Ошибка отклонения возврата по заказу на возврат](media/refund-order-decline.jpg)

## <a name="resolution"></a>Приказ

### <a name="enable-blind-returns-in-adyen"></a>Включить возвраты вслепую в Adyen

Чтобы включить возвраты вслепую, выполните шаги, описанные в разделе [Устранение неполадок с соединитель платежей Dynamics 365 для Adyen](adyen-support.md), чтобы связаться с группой поддержки Adyen, и запросите, что функция возвратов вслепую должна быть включена на вашем счете Adyen.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Соединитель платежей Dynamics 365 для Adyen](../dev-itpro/adyen-connector.md)

[Настройка соединителя платежей Adyen для Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
