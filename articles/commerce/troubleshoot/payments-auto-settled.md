---
title: Платежи автоматически сопоставляются до выставления накладных или отгрузки заказов
description: В этой статье содержатся указания по устранению неполадок, которые могут помочь при сопоставлении платежа в портале Adyen сразу после размещения заказа, даже если по заказу на продажу не выставлены накладные или не выполнена отгрузка.
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
ms.openlocfilehash: 6fdaf48600edc22b5423e0167177616758e2dc6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282716"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Платежи автоматически сопоставляются до выставления накладных или отгрузки заказов

[!include [banner](../../includes/banner.md)]

В этой статье содержатся указания по устранению неполадок, которые могут помочь при сопоставлении платежа в портале Adyen сразу после размещения заказа, даже если по заказу на продажу не выставлены накладные или не выполнена отгрузка.

## <a name="description"></a>описание

После размещения заказа платеж сразу сопоставляется в портале Adyen, даже если по заказу на продажу не выставлены накладные или не выполнена отгрузка.

## <a name="resolution"></a>Приказ

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Настройка регистрации вручную для платежей электронной коммерции на портале Adyen

Чтобы настроить регистрацию вручную для платежей электронной коммерции на портале Adyen, выполните следующие действия.

1. Выполните вход на портал Adyen.
1. В верхнем правом углу выберите счет продавца для канала электронной коммерции.
1. На верхней панели навигации выберите **Учетная запись**, а затем выберите **Параметры**.
1. В поле **Задержка регистрации** выберите **вручную**.

    ![Параметр "Задержка регистрации" на портале Adyen.](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Регистрация платежа Adyen](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365 Payment Connector для Adyen](../dev-itpro/adyen-connector.md)

[Настройка соединителя платежей Adyen для Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
