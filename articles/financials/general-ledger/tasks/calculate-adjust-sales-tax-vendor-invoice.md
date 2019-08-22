---
title: Расчет и корректировка налога по накладной поставщика
description: Эта тема объясняет, как скорректировать налог в счете-фактуре поставщика в Dynamics 365 for Finance and Operations.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 684529087d5348c9e02310f812f8aa6f64c6655f
ms.sourcegitcommit: 016832198c306e8329ad21b5254e7d1cdff74c2f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862622"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Расчет и корректировка налога по накладной поставщика

[!include [task guide banner](../../includes/task-guide-banner.md)]

Эта тема объясняет, как скорректировать налог в счете-фактуре поставщика в Dynamics 365 for Finance and Operations. Если в исходном документе-источнике отображаются суммы налога, отличные от рассчитанных, эти суммы можно изменить перед разноской. В этой задаче используется демонстрационная компания DEMF.

1. В области переходов выберите **Модули > Расчеты с поставщиками > Накладные > Журнал накладных**.
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

