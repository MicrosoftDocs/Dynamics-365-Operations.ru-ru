---
title: Создание накладных платежей
description: В этой теме описывается, как создавать ежемесячные накладные по аренде. Можно создать накладные для индивидуальных аренд, или можно использовать процесс пакетной обработки для создания накладных для нескольких аренд.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymentSchedule
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8d0b10993c61c64dadc00046907485f3886e2e01
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881188"
---
# <a name="create-payment-invoices"></a>Создание накладных платежей

[!include [banner](../includes/banner.md)]

Можно создать ежемесячные накладные для индивидуальных аренд, или можно использовать процесс пакетной обработки для создания накладных для нескольких аренд. Следующая процедура показывает, как создать отдельную запись платежа по аренде, когда параметр **Платеж поставщику** на странице **Настройка книги аренды** включен.

1. На странице **Сводка по аренде** выберите аренду, а затем выберите **Книги \> График платежей**.
2. Выберите платеж, который должен быть создан, а затем выберите **Создать журнал**. Вы получите сообщение о том, что для выбранного платежа был создан журнал.
3. Выберите **Журналы накладных**, а затем выберите накладную, которая должна быть оплачена.
4. На вкладке **Строки** проверьте запись журнала до ее разноски в главную книгу.

    > [!NOTE]
    > По умолчанию созданные строки накладной поставщика используют профиль разноски поставщика на странице **Параметры модуля расчетов с поставщиками**.

5. Выберите правильный журнал, а затем выберите накладную, которая должна быть оплачена.

    В данном примере параметр **Платеж поставщику** в книге аренды включен. Поэтому накладная будет в журнале накладных. Раздел **Обзор** содержит сводку записи журнала, а в разделе **Строки** отображаются сведения о фактических строках журнала.

    > [!NOTE]
    > Если параметр **Платеж поставщику** отключен, записи журнала платежей будут перечислены на странице **Аренда активов** для книги аренды, а в системе вместо накладной будет создана запись аренды актива. Запись платежа по аренде будет разнесена по имени журнала, которое указано в поле **Месячный журнал аренды**.

6. После разноски проводки можно просмотреть сведения о проводке и остаточную стоимость обязательств по аренде, выбрав **Проводки по обязательствам** в книге аренды.

    В графике платежей будет установлен флажок **Журнал разнесен**, а в строке будет показан номер журнала накладных. После создания журнала платежей и записи для этого журнала необходимо реверсировать запись, прежде чем ее можно будет создать повторно.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
