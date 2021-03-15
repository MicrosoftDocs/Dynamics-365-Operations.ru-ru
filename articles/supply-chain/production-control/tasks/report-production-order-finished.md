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
ms.openlocfilehash: 5d9dcdbcb89df6430fb286c253ebecfc6d885af8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011155"
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