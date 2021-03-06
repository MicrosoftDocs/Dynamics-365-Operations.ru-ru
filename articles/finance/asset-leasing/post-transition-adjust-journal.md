---
title: Разноска записей журнала корректировки перехода в аренде активов
description: В этой теме описываются функции, которые позволяют перевести портфель аренды в новые стандарты учета аренды, тема 842 кодификации стандартов бухгалтерского учета (ASC 842) и международный стандарт финансовой отчетности 16 (МСФО 16).
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ea61a0d6e30695a2ef6b93529fcf3d21882c9cd2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819778"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>Разноска записей журнала корректировки перехода в аренде активов

[!include [banner](../includes/banner.md)]

В этой теме описываются функции, которые позволяют перевести портфель аренды в новые стандарты учета аренды: тема 842 кодификации бухгалтерских стандартов (ASC 842), которая является стандартом в общепринятых принципах учета в США (US GAAP), и международный стандарт финансовой отчетности 16 (МСФО 16).

Сведения о порядке настройки книги для перехода к новым стандартам см. в разделе [Настройка книг аренды](set-up-lease-books.md).

При создании записи журнала корректировок перехода создается запись журнала. Эта запись отражает влияние на балансовый отчет записи аренды на новые новых стандартов на эту дату. Соответствующий счет актива дебетуется на учетную сумму на эту дату, а счет обязательств кредитуется. Разница дебетуется или кредитуется на нераспределенную прибыль.

Чтобы разнести корректировку перехода в соответствие с новыми стандартами учета, выполните следующие действия.

1. На странице **Сводка по аренде** выберите аренду, а затем выберите **Книги**.
2. В книге выберите **График оплаты**.
3. В диалоговом окне **График оплаты** выберите **Подтвердить**. Затем закройте диалоговое окно.
4. Выберите **Корректировка перехода**.

    > [!NOTE]
    > Корректировка перехода может быть создана только для тех книг аренды, которые назначены книге, в которой доступно поле **Книга перехода**. Если значение в поле **Начало аренды** позже даты перехода, значение в поле **Корректировка перехода** не обновляется.

5. Для просмотра записи журнала выберите **Журналы аренды активов**.
6. Выберите новый журнал, затем выберите **Разнести**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]