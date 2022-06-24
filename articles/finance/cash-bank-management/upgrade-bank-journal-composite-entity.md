---
title: Обновление составного объекта журнала банка
description: В этой статье перечислены шаги, которые требуются, чтобы добавить дополнительное поле BankTransactionType в составной объект BankJournalEntity.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: db5f01af6b21b4dc5ff633ee9c11bb6ed41df048
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868557"
---
# <a name="update-the-bank-journal-composite-entity"></a>Обновление составного объекта журнала банка

[!include [banner](../includes/banner.md)]

В этой статье перечислены шаги, которые требуются, чтобы добавить дополнительное поле BankTransactionType в составной объект BankJournalEntity.

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






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
