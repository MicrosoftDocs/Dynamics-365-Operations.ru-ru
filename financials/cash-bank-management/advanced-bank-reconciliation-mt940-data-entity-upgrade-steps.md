---
title: "Импорт расширенной банковской выверки MT940 — обновление составного информационного объекта"
description: "Порядковый номер должен быть добавлен в объект импорта банковской выписки для поддержки формата MT940."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 672697254c1bf06e193a51c5c7c83c467a220ce8
ms.contentlocale: ru-ru
ms.lasthandoff: 05/25/2017


---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Импорт расширенной банковской выверки MT940 — обновление составного информационного объекта

[!include[banner](../includes/banner.md)]


Порядковый номер должен быть добавлен в объект импорта банковской выписки для поддержки формата MT940. 

Следующие шаги используются для добавления объекта импорта банковской выписки для поддержки формата MT940.

1.  Выполните компиляцию и синхронизацию следующего:
    -   Составной объект\\BankStatementImportEntity
    -   Объект\\BankStatementBalanceEntity
    -   Объект\\BankStatementDocumentEntity
    -   Объект\\BankStatementEntity
    -   Объект\\BankStatementLineEntity
    -   Таблицы\\BankStatementStaging

2.  Управление данными\\проекты данных.
    1.  Загрузка проектов импорта MT940
        1.  Измените XSLT.
            -   Щелкните **Просмотр карты**.
            -   Щелкните **Просмотр карты** на документе банковской выписки.
            -   Щелкните **Преобразования**
            -   Удалите файл BankReconiliation-to-Composite.xslt.
            -   Добавьте новую версию файла BankReconiliation-to-Composite.xsl.

        2.  Выведите **Порядковый номер** в макете **Исходные данные**.
            1.  Формат исходных данных = XML-элемент.
            2.  Имя объекта = Банковские выписки.
            3.  Отправите файл данных = новая версия SampleBankCompositeEntity.xml.
            4.  Нажмите кнопку **Да**, чтобы перезаписать существующий файл.
            5.  Нажмите **Да** для создания нового сопоставления.
            6.  Убедитесь, что **SequenceNumber** сопоставлен.
                -   Щелкните **Просмотр карты** на объекте выписки.
                -   Убедитесь, что **SequenceNumber** составлен с "Источник" на "Промежуточное хранение".

3.  Импортируйте новую выписку.





