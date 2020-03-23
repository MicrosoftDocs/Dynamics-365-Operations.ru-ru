---
title: Регистрация накладной поставщика и сопоставление с полученными количествами
description: При получении накладной от поставщика за товары или услуги по заказу на покупку для бизнес-процессов может потребоваться, чтобы товары или услуги были получены, прежде чем накладная может утверждена для платежа.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66d84f497775ce4f988242dd2b327bf4854faef5
ms.sourcegitcommit: ba1c76497acc9afba85257976f0d4e96836871d1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2019
ms.locfileid: "2890427"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Регистрация накладной поставщика и сопоставление с полученными количествами

[!include [task guide banner](../../includes/task-guide-banner.md)]

При получении накладной от поставщика за товары или услуги по заказу на покупку для бизнес-процессов может потребоваться, чтобы товары или услуги были получены, прежде чем накладная может утверждена для платежа. Перед началом работы убедитесь, что выбран конфигурационный ключ "Сопоставление накладных". 

На странице "Параметры расчетов с поставщиками" убедитесь, что установлен флажок "Включить проверку сопоставления накладных", в поле "Разнести накладную с несоответствиями" задано значение "Требуется утверждение" и в поле "Политика проверки соответствия строк" задано значение "Трехстороннее сопоставление".

В данной процедуре используется демонстрационная компания USMF. Эти шаги выполняются ролями менеджера по расчету с поставщиками или главного бухгалтера.


## <a name="create-a-purchase-order"></a>Создание заказа на покупку
1. Перейдите в раздел "Все заказы на покупку".
2. Щелкните "Создать".
3. В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
4. В поле "Счет поставщика" введите значение.
5. Нажмите кнопку "OК".
6. Щелкните "Добавить строку".
7. В поле "Код номенклатуры" введите значение.
8. В области действий щелкните "Покупка".
9. Нажмите кнопку "Подтвердить".

## <a name="post-a-product-receipt"></a>Разноска поступления продуктов
1. В области действий щелкните "Получение".
2. Щелкните "Поступление продуктов".
3. В списке пометьте выбранную строку.
4. В поле "Поступление продуктов" введите значение.
5. Нажмите кнопку "OК".

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Регистрация и сопоставление накладной поставщика с поступлением продуктов
1. В области действий щелкните "Накладная".
2. Щелкните "Накладная".
3. В поле "Число" введите значение.
4. Щелкните "По умолчанию из: заказанное количество", чтобы открыть диалоговое окно.
5. В поле "Количество по умолчанию для строк" выберите вариант.
6. Нажмите кнопку "OК".
7. Щелкните Да.
8. Щелкните "Сопоставить поступления продуктов".
9. Нажмите кнопку "OК".
10. В области действий щелкните "Просмотр".
11. Щелкните "Сведения о сопоставлении".
