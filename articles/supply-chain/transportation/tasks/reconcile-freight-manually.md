---
title: Выверка фрахта вручную
description: Эта процедура показывает, как выверять фрахт вручную.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee2d114b0a725b947add3e155cc6445021fee998
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556742"
---
# <a name="reconcile-freight-manually"></a>Выверка фрахта вручную

[!include [task guide banner](../../includes/task-guide-banner.md)]

Эта процедура показывает, как выверять фрахт вручную. Обычно это делает координатор транспортировки. Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.


## <a name="select-a-load-to-reconcile"></a>Выберите груз для выверки
1. Перейдите в раздел "Управление транспортировкой" > "Планирование" > "Рабочее место планирования загрузки".
2. Снимите флажок "Скрыть отгруженные и полученные". 
3. В списке выберите груз с кодом груза 00006.

## <a name="create-a-carrier-invoice"></a>Создайте накладную перевозчика
    * Если выполняется сверка фрахт вручную, и вы не получаете накладные перевозчика автоматически, можно создать накладную на основе счета за фрахт.  
1. Щелкните "Связанные сведения".
2. Щелкните "Сведения векселя фрахта".
3. Щелкните "Создать накладную по векселю фрахта".
4. В поле "Накладная" введите значение.
5. Нажмите кнопку "OК".

## <a name="reconcile-the-invoice"></a>Выверка накладной
    * Сверка накладной перевозчика и счета за фрахт выполняется построчно.  
1. Щелкните "Сопоставить вексели фрахта с накладными".
2. Разверните раздел "Сведения о накладной".
3. Разверните раздел "Несовпадающие сведения векселя фрахта".
4. В списке пометьте выбранную строку.
5. Щелкните "Сопоставить".
6. Разверните раздел "Совпадающие сведения векселя фрахта".

## <a name="submit-the-invoice-for-approval"></a>Отправить накладную на утверждение
1. Щелкните "Отправить для утверждения".
2. Закройте страницу.
3. Снимите флажок "Скрыть утвержденные". 
4. Щелкните "Журналы накладных поставщиков".
5. Щелкните для перехода по ссылке в поле "Номер ссылочного журнала".
6. Щелкните "Строки".

