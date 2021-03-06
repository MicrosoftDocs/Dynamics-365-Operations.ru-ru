---
title: Вариант "сохранить для следующего платежа" не отображается
description: В этом разделе приведены инструкции по устранению неполадок, которые могут помочь, когда флажок "сохранить для следующего платежа" не появился в разделе "Способ оплаты" на странице оформления заказа сайта электронной коммерции.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: af19a3abd78d543d82f7a8d017e2dc413115a6d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018442"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Вариант "Сохранить для следующего платежа" не отображается

[!include [banner](../../includes/banner.md)]

В этом разделе приведены инструкции по устранению неполадок, которые могут помочь, когда флажок **Сохранить для следующего платежа** не появился в разделе **Способ оплаты** на странице оформления заказа сайта электронной коммерции.

## <a name="description"></a>описание

Флажок **Сохранить для следующего платежа** не отображается в разделе **Способ оплаты** на странице оформления заказа сайта электронной коммерции.

На следующем рисунке показан пример страницы оформления заказа, которая включает флажок **Сохранить для следующего платежа**.

![Флажок "Сохранить для следующего платежа" в Модуле платежа](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Приказ

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Убедитесь, что соединитель платежей Dynamics 365 для Adyen правильно настроен в Commerce headquarters

Чтобы убедиться в том, что соединитель платежей Dynamics 365 для Adyen правильно настроен в Commerce headquarters, выполните следующие действия.

1. Перейдите в раздел **Retail и Commerce \> Каналы \> Интернет-магазины**.
1. Выберите интернет-магазин.
1. На экспресс-вкладке **счета оплаты** убедитесь, что в поле **Разрешить сохранение информации о платеже в электронной коммерции** задано значение **Истина**.

![Разрешить сохранение сведений о платежах в поле электронной коммерции в Commerce headquarters](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Модуль платежа](../payment-module.md)

[Сохранение интерактивных платежных инструментов с помощью соединителя Adyen](../dev-itpro/adyen-connector-listPI.md)
