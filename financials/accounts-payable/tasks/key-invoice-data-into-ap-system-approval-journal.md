--- 
title: "Ввод данных счета в модуль расчетов с поставщиками с использованием журнала утверждения"
description: "В этом руководстве по задаче показано, как использовать регистр накладных для создания накладных и последующего использования журнала утверждения для обновления счетов расходов."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d7cf810f1d8eabb9989fdd858585afcdf2e9574b
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Ввод данных счета в модуль расчетов с поставщиками с использованием журнала утверждения

[!include[task guide banner](../../includes/task-guide-banner.md)]

В этом руководстве по задаче показано, как использовать регистр накладных для создания накладных и последующего использования журнала утверждения для обновления счетов расходов.


## <a name="create-and-post-and-invoice"></a>Создание и разноска накладной
1. Перейдите в раздел "Расчеты с поставщиками" > "Накладные" > "Регистр накладных".
2. Щелкните "Создать".
3. Выберите имя регистра накладных для использования.
4. В списке перейдите по ссылке в выбранной строке.
5. Щелкните "Строки", чтобы открыть регистр и ввести строки расходов.
6. Выберите поставщика. Например, введите или выберите US-104.
7. В поле "Накладная" введите значение.
8. В поле "Описание" введите значение.
9. В поле "Кредит" введите число.
10. В поле "Кем утверждено" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
11. Выделите утверждающее лицо и нажмите кнопку "Выбрать", чтобы выбрать его.
12. Щелкните "Разнести".
13. Закройте страницу.
14. Закройте страницу.

## <a name="approve-an-invoice"></a>Утверждение накладной
1. Перейдите в раздел "Расчеты с поставщиками" > "Накладные" > "Утверждение накладной".
2. Щелкните "Создать".
3. Выберите имя журнала утверждений накладных для использования.
4. В списке перейдите по ссылке в выбранной строке.
5. Щелкните строки для отображения страницы, на которой можно будет выбрать накладные, которые требуется утвердить.
6. Выберите "Найти ваучеры" для отображения всех накладных, готовых к утверждению.
7. Пометьте созданную накладную.
8. Щелкните Выбрать.
    * Выбранные выше ваучеры перемещаются в этот список после их выбора.  
9. Нажмите кнопку "OК".
10. Щелкните поле "Номер счета" для добавления счета расходов в накладную.
11. Введите номер счета и выйдите из поля. Например, введите 600120.
12. Щелкните "Разнести".
13. Щелкните "Ваучер" для просмотра разнесенных записей.
    * Счет утверждения ожидающих накладных реверсируется и заменяется на счет фактических расходов.  

