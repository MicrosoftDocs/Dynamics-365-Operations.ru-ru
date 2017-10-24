---
title: "Обновление составного объекта журнала банка"
description: "Следующие шаги требуются, чтобы добавить дополнительное поле BankTransactionType в составной объект BankJournalEntity."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 18b2b228f287a946eb18536b1ea93b0d6af6900c
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="update-the-bank-journal-composite-entity"></a>Обновление составного объекта журнала банка

[!include[banner](../includes/banner.md)]


Следующие шаги требуются, чтобы добавить дополнительное поле BankTransactionType в составной объект BankJournalEntity.

Используйте следующие шаги, чтобы добавить дополнительное поле BankTransactionType в составной объект BankJournalEntity.

1.  Скомпилируйте и синхронизируйте следующие составные объекты, объекты и промежуточные таблицы журнала банка:
    -   Составной объект\\BankJournalEntity
    -   Объект\\BankJournalHeaderEntity
    -   Объект\\BankJournalLineEntity
    -   Таблица\\BankJournalHeaderStaging
    -   Таблица\\BankJournalLineStaging

2.  Управление данными\\проекты данных
    -   Сделайте доступным тип **Банковская проводка** в макете **Исходные данные**.
        -   Формат исходных данных = XML-элемент
        -   Имя объекта = Банковский журнал
        -   Отправьте файл данных = новая версия SampleBankJournalCompositeEntity.xml
        -   Нажмите кнопку **Да**, чтобы перезаписать существующий файл.
        -   Нажмите **Да** для создания сопоставления с самого начала.
        -   Убедитесь, что тип "Банковская проводка" сопоставлен.
            -   Щелкните **Просмотр карты** на объекте "Строка".
            -   Убедитесь, что тип "Банковская проводка" составлен с "Источник" на "Промежуточное хранение".

3.  Импортируйте новую выписку.





