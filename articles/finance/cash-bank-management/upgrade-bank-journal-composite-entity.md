---
title: Обновление составного объекта журнала банка
description: Следующие шаги требуются, чтобы добавить дополнительное поле BankTransactionType в составной объект BankJournalEntity.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e6c990208f26dde26b7adc306198f7cd16e0e69b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978922"
---
# <a name="update-the-bank-journal-composite-entity"></a>Обновление составного объекта журнала банка

[!include [banner](../includes/banner.md)]

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




