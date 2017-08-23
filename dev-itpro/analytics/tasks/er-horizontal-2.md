--- 
title: "Выполнение формата, использующего горизонтально разворачивающиеся диапазоны для динамического добавления столбцов в отчеты Excel для электронной отчетности (ER)"
description: "Следующие шаги описывают, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для создания отчетов в виде файлов листов OPENXML (Excel), в которых необходимые столбцы можно создавать динамически как горизонтально расширяемые диапазоны."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4b859151edd28e39c1f97b2f600da6e304b1d065
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a>Выполнение формата, использующего горизонтально разворачивающиеся диапазоны для динамического добавления столбцов в отчеты Excel для электронной отчетности (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Следующие шаги описывают, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для создания отчетов в виде файлов листов OPENXML (Excel), в которых необходимые столбцы можно создавать динамически как горизонтально расширяемые диапазоны. Эти шаги можно выполнить в компании DEMF.

Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel (Часть 1. Разработка формата)".

Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.


## <a name="find-created-format"></a>Найдите созданный формат
1. Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".
2. В дереве разверните узел "Пример модели финансовых аналитик".
3. В дереве выберите "Пример модели финансовых аналитик\Пример отчета с горизонтально расширяемыми диапазонами".

## <a name="execute-format-to-create-excel-output"></a>Выполните формат для создания выходных данных Excel
1. Щелкните "Выполнить".
2. В поле "Имя аналитики" введите "BusinessUnit;CostCenter;Department".
    * В поле "Имя аналитики" введите или выберите значение.  Чтобы выбрать все аналитики для текущей компании, введите следующие сведения:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. Разверните раздел "Записи для добавления".
4. Щелкните "Фильтр".
5. Выберите строку для таблицы "Журнал ГК" и поля "Номер партии журнала".
6. В поле "Критерии" введите "00057..00058".
    * 00057..00058  
7. Нажмите кнопку "OК".
8. Нажмите кнопку "OК".
    * Просмотрите созданные выходные данные. Обратите внимание, что вновь созданный файл Excel содержит то же число столбцов, которое было выбрано для финансовых аналитик. Заголовок отчета в этих столбцах представляет имена финансовых аналитик. Строки проводок в этих столбцах представляют финансовые аналитики. Выполните этот отчет и выберите другие аналитики, чтобы убедиться, что отчет не зависит от количества выбранных аналитик или количества аналитик, настроенных для данного экземпляра Dynamics 365 for Finance and Operations, Enterprise edition.  

