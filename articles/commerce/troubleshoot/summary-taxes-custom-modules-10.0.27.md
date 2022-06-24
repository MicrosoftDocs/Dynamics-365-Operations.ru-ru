---
title: Промежуточный итог сводки по заказу включает налоги на накладные расходы при использовании настроенных модулей сводки по заказу
description: В этой статье представлено руководство по устранению неполадок, которое может помочь при использовании настраиваемых модулей сводки заказов, а подытог сводки по заказам не включает налоги на расходы в сценарии «Цена включает налог».
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 260dcb6bc1585615195e32adfcd1da6bfbca294e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848845"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>Промежуточный итог сводки по заказу включает налоги на накладные расходы при использовании настроенных модулей сводки по заказу

В этой статье представлено руководство по устранению неполадок, которое может помочь при использовании настраиваемых модулей сводки заказов, а подытог сводки по заказам не включает налоги на расходы в сценарии «Цена включает налог».

## <a name="description"></a>Описание

Начиная с выпуска Microsoft Dynamics 365 Commerce версии 10.0.27, в сценарий «цена включает налог с продаж» были внесены следующие изменения, чтобы обеспечить согласованность модулей сводки заказов на страницах сайта электронной коммерции.

- Добавлены два новых поля: **TaxOnShippingCharge** и **TaxOnNonShippingCharges**.
- Интерфейсы прикладного программирования  **GetSalesOrderBySalesId** и **GetSalesOrderByTransactionId** имеют точные значения для следующих полей в сценарии «цена включает налог с продаж»:

    - SubtotalSalesAmount
    - SubtotalAmountWithoutTax
    - SubtotalAmount
    - ShippingChargeAmount
    - OtherChargeAmount

Однако если используются настраиваемые модули сводки заказов, эти изменения могут повлиять на значения промежуточных итоговых сумм заказов, не включая налоги на расходы.

## <a name="resolution"></a>Решение

Если вы используете настраиваемые модули сводки заказов и не хотите наследовать изменения, внесенные в сценарий «цена включает налог с продаж» в Commerce версии 10.0.27 и более поздних, следуйте инструкциям в этом разделе.

Вернувшись к предыдущему (до версии 10.0.27) сводному поведению заказа для полей **salesTransaction.SubtotalAmount** и **salesTransaction.SubtotalAmountWithoutTax**, вы восстанавливаете включение общей суммы налога (**TaxOnShippingCharge** и **TaxOnNonShippingCharges**) в промежуточных суммах (**SubtotalAmount** и **SubtotalAmountWithoutTax**).

Чтобы вернуться к предыдущему поведению сводки заказов, выполните следующие действия.

1. В модуле Commerce headquarters откройте страницу параметров (**Розница и коммерция \> Настройка Headquarters \> Параметры \> Параметры Commerce**).
1. В левой области навигации выберите **Параметры конфигурации**.
1. Добавьте следующие параметры конфигурации и установите для каждого поля значение **истина**:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryHydrationEnabled

> [!NOTE]
> Если ранее был использован параметр конфигурации **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled** и хотите сохранить такое же поведение для свойства  **order.NetAmountWithoutTax**, вам также следует добавить параметр конфигурации **IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** и задать его значение **true**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Скрытие сведений о разбиении налогов в сводках заказов](../hide-taxes-breakup.md)
