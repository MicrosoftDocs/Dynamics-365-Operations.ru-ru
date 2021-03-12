---
title: Расчет и корректировка налога по накладной поставщика
description: Эта тема объясняет, как скорректировать налог в счете-фактуре поставщика в Dynamics 365 Finance.
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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2536e87953267eae13cf3b42c2bd5476fc647c22
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994723"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Расчет и корректировка налога по накладной поставщика

[!include [banner](../../includes/banner.md)]

Эта тема объясняет, как скорректировать налог в счете-фактуре поставщика. Если в исходном документе-источнике отображаются суммы налога, отличные от рассчитанных, эти суммы можно изменить перед разноской. В этой задаче используется демонстрационная компания DEMF.

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

