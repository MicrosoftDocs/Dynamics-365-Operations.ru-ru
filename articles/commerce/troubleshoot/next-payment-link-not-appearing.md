---
title: Вариант "сохранить для следующего платежа" не отображается
description: В этой статье приведены инструкции по устранению неполадок, которые могут помочь, когда флажок "сохранить для следующего платежа" не появился в разделе "Способ оплаты" на странице оформления заказа сайта электронной коммерции.
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
ms.openlocfilehash: d0b398a4ffc5fb698ea04ba8642d05ccd4caf04c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287493"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Вариант "Сохранить для следующего платежа" не отображается

[!include [banner](../../includes/banner.md)]

В этой статье приведены инструкции по устранению неполадок, которые могут помочь, когда флажок **Сохранить для следующего платежа** не появился в разделе **Способ оплаты** на странице оформления заказа сайта электронной коммерции.

## <a name="description"></a>описание

Флажок **Сохранить для следующего платежа** не отображается в разделе **Способ оплаты** на странице оформления заказа сайта электронной коммерции.

На следующем рисунке показан пример страницы оформления заказа, которая включает флажок **Сохранить для следующего платежа**.

![Флажок "Сохранить для следующего платежа" в Модуле платежа.](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Решение

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Убедитесь, что соединитель платежей Dynamics 365 для Adyen правильно настроен в Commerce headquarters

Чтобы убедиться в том, что соединитель платежей Dynamics 365 для Adyen правильно настроен в Commerce headquarters, выполните следующие действия.

1. Перейдите в раздел **Retail и Commerce \> Каналы \> Интернет-магазины**.
1. Выберите интернет-магазин.
1. На экспресс-вкладке **счета оплаты** убедитесь, что в поле **Разрешить сохранение информации о платеже в электронной коммерции** задано значение **Истина**.

![Разрешить сохранение сведений о платежах в поле электронной коммерции в центральном офисе Commerce.](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Модуль платежа](../payment-module.md)

[Сохранение интерактивных платежных инструментов с помощью соединителя Adyen](../dev-itpro/adyen-connector-listPI.md)
