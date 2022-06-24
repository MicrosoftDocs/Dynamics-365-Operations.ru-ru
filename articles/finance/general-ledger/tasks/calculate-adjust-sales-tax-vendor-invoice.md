---
title: Расчет и корректировка налога по накладной поставщика
description: В этой статье объясняется, как скорректировать налог в накладной поставщика в Dynamics 365 Finance.
author: twheeloc
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a1093631688351d065d6b55bc65055b6f92d256
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868383"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Расчет и корректировка налога по накладной поставщика

[!include [banner](../../includes/banner.md)]

Эта статья объясняет, как скорректировать налог в накладной поставщика. Если в исходном документе-источнике отображаются суммы налога, отличные от рассчитанных, эти суммы можно изменить перед разноской. В этой задаче используется демонстрационная компания DEMF.

1. Перейдите в раздел **Расчеты с поставщиками > Накладные > Журнал накладных**.
2. Выберите **Создать**.
3. В поле **Имя** новой строки выберите вариант в раскрывающемся меню.
4. На панели действий выберите **Строки**.
5. В поле **Счет** укажите требуемые значения.
6. В поле **Накладная** введите значение.
7. В поле **Кредит** введите число.
8. В поле **Корр.счет** укажите требуемые значения.
9. Выберите **Налог**.
10. В поле **Общая сумма фактического налога** введите число.
11. На вкладке **Корректировка** можно изменить суммы налога по налоговому коду.
12. Выберите **Сбросить рассчитанные суммы до фактических**.
13. Нажмите **ОК**.
14. Нажмите **Сохранить**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
