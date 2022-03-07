---
title: Платежи автоматически сопоставляются до выставления накладных или отгрузки заказов
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь при сопоставлении платежа в портале Adyen сразу после размещения заказа, даже если по заказу на продажу не выставлены накладные или не выполнена отгрузка.
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
ms.openlocfilehash: b4fd37a3c45f2559c9659f072ca0b6f02e712f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018268"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Платежи автоматически сопоставляются до выставления накладных или отгрузки заказов

[!include [banner](../../includes/banner.md)]

В этом разделе содержатся указания по устранению неполадок, которые могут помочь при сопоставлении платежа в портале Adyen сразу после размещения заказа, даже если по заказу на продажу не выставлены накладные или не выполнена отгрузка.

## <a name="description"></a>описание

После размещения заказа платеж сразу сопоставляется в портале Adyen, даже если по заказу на продажу не выставлены накладные или не выполнена отгрузка.

## <a name="resolution"></a>Приказ

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Настройка регистрации вручную для платежей электронной коммерции на портале Adyen

Чтобы настроить регистрацию вручную для платежей электронной коммерции на портале Adyen, выполните следующие действия.

1. Выполните вход на портал Adyen.
1. В верхнем правом углу выберите счет продавца для канала электронной коммерции.
1. На верхней панели навигации выберите **Учетная запись**, а затем выберите **Параметры**.
1. В поле **Задержка регистрации** выберите **вручную**.

    ![Параметр "Задержка регистрации" на портале Adyen](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Регистрация платежа Adyen](https://docs.adyen.com/point-of-sale/capturing-payments)

[Соединитель платежей Dynamics 365 для Adyen](../dev-itpro/adyen-connector.md)

[Настройка соединителя платежей Adyen для Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
