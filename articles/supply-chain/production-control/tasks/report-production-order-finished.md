---
title: Сообщение о завершении производственного заказа
description: В этой процедуре показано, как составить отчет по производственному заказу как "завершено".
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4848093bd4901d3aa801fc09d7ee3e79d65ebb0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204473"
---
# <a name="report-a-production-order-as-finished"></a>Сообщение о завершении производственного заказа

[!include [banner](../../includes/banner.md)]

В этой процедуре показано, как составить отчет по производственному заказу как "завершено". В качестве компании с демонстрационными данными для создания этой процедуры используется USMF. Это шестая из семи процедур, которая объясняет жизненный цикл производственного заказа.


## <a name="report-a-production-order-as-finished"></a>Сообщение о завершении производственного заказа
1. Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".
    * Выберите производственный заказ со статусом "Начато".  
2. В области действий щелкните "Производственный заказ".
3. Щелкните "Приемка".
    * На этой странице можно подтвердить количество готовой продукции как "принято".  
4. Перейдите на вкладку "Общие".
5. Установите "Количество правильных" равным "18".
6. Установите "Количество ошибочных" равным "2".
7. В поле "Причина ошибки" выберите "Материал".
8. Установите или снимите флажок "Заключительное задание".
9. Установите или снимите флажок "Ошибка приема".
10. Нажмите кнопку "OК".

## <a name="verify-the-report-as-finished-journal"></a>Проверка журнала "Приемка"
1. В области действий щелкните "Показать".
2. Щелкните "Принятые".
3. В списке пометьте выбранную строку.
4. В списке перейдите по ссылке в выбранной строке.
    * Выполняется разноска журнала "Приемка". Если вы хотите выполнить корректировки в журнале, можно вручную создать новый журнал, в котором можно внести изменения.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]