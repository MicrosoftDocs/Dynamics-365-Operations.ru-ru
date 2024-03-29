---
title: Указание кросс-курса
description: В этой статье представлены сведения о кросс-курсах в Microsoft Dynamics 365 Finance.
author: abruer
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efb01948af2bcba9ca740e8bd0e12584cf021fce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889971"
---
# <a name="specify-the-cross-rate"></a>Указание кросс-курса

[!include [banner](../includes/banner.md)]

В этой статье описывается предназначение кросс-курса и то, как указать кросс-курс при сопоставлении платежа с накладной. Используйте кросс-курс, когда соблюдаются следующие условия. 
-   Платеж сопоставляется с накладной. 
-   В строке платежа и строке накладной используются разные валюты. 
-   Ни одна из валют не является валютой учета. 

Кросс-курс не используется для вычисления трансляции валюты транзакции платежа в валюту учета платежа. Вместо этого извлекаются валютные курсы из таблиц валютных курсов, чтобы вычислить значение суммы в валюте транзакции по оплате и значение суммы в валюте для учета платежа. 

Например, валюта учета — американский доллар, валюта накладной — канадский доллар, а валюта платежа — евро. Кросс-курс позволяет ввести валютный курс для конвертации непосредственно из канадского доллара в евро, минуя американский доллар. Выбирая накладную и основной платеж, можно ввести кросс-курс для строки накладной. Кросс-курс - это обменный курс между валютами для этих проводок на дату сопоставления.

1.  Перейдите на одну из следующих страниц:
- **Расчеты с клиентами > Общее > Клиенты > Все клиенты** 
- **Расчеты с поставщиками > Общее > Поставщики > Все поставщики** 
- **Закупки и источники > Общее > Поставщики > Все поставщики**
2.  Выберите клиента или поставщика, чьи открытые транзакции сопоставляются. 
3.  Для клиента на странице списка **Все клиенты** последовательно выберите пункты **Собрать > Сопоставлять открытые транзакции**. Для поставщика на странице списка **Все поставщики** последовательно выберите пункты **Накладная > Сопоставлять открытые транзакции**. 
4.  Выберите транзакции, являющиеся основным платежом, и щелкните кнопку **Пометить оплату**. Будет установлен флажок в столбце **Пометка**, а в столбце **Основной платеж** будет показан информационный значок. 
5.  В поле **Кросс-курс** введите обменный курс между валютами накладной и платежа на дату сопоставления. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
