---
title: Создание расширенных правил для журналов
description: Эта процедура описывает создание дополнительных правил для журналов.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5cc41f19928fd415fb54073fd733f97a3e7aa01
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717428"
---
# <a name="create-advanced-rules-for-journals"></a>Создание расширенных правил для журналов

[!include [banner](../../includes/banner.md)]

Эта процедура описывает создание дополнительных правил для журналов. Сюда входят настройка управления журналом и ограничения разноски по пользователю. В этой процедуре используется компания с демонстрационными данными USMF.


## <a name="set-up-journal-control"></a>Настройка управления журналом
1. В **области перехода** выберите **Модули > Главная книга > Настройки журнала > Наименования журналов**.
2. В списке найдите и выберите требуемую запись.
3. На **панели операций** щелкните **Проверка журнала**.
4. На экспресс-вкладке **Какие типы счетов можно разнести** щелкните **Добавить**.
5. В поле **Компании** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
6. В списке найдите и выберите требуемую запись.
7. В списке перейдите по ссылке в выбранной строке.
8. На экспресс-вкладке **Какие значения сегмента являются допустимыми для этого журнала** щелкните **Добавить**.
9. В поле **Структура счета** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
10. Поиск и выбор требуемой записи в списке.
11. В списке перейдите по ссылке в выбранной строке.
12. В поле **Сегмент** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
13. В списке перейдите по ссылке в выбранной строке.
14. В поле **Со значения** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
15. Поиск и выбор требуемой записи в списке.
16. В списке перейдите по ссылке в выбранной строке.
17. В поле **До значения** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
18. В списке найдите и выберите требуемую запись.
19. В списке перейдите по ссылке в выбранной строке.

## <a name="set-up-posting-restrictions"></a>Настройка ограничений разноски
1. Закройте страницу.
2. Щелкните **Ограничения разноски**.
3. В пункте **Каким образом настроить ограничения разноски?** выберите "По группе пользователя".
4. В дереве установите флажок "Группа, которой следует разрешить разноску для этого наименования журнала".
5. Щелкните **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
