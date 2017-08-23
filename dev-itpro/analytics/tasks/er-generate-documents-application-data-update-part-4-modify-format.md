--- 
title: "Изменение формата для создания документов с обновлением данных приложения для электронной отчетности (ER)"
description: "Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру \"Электронная отчетность — Формирование документов с обновлением данных приложения (Часть 3. Изменение модели и сопоставления)\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: 053accd5b992b5fe1aa1652e0e542b16625485cc
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="modify-format-to-generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Изменение формата для создания документов с обновлением данных приложения для электронной отчетности (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру "Электронная отчетность — Формирование документов с обновлением данных приложения (Часть 3. Изменение модели и сопоставления)".

В этой процедуре поясняется разработка конфигураций электронной отчетности для формирования электронного документа и обновления данных приложения. В этой процедуре вам предстоит изменить конфигурации электронной отчетности, чтобы использовать их не просто для формирования электронных документов, но также для обновления данных приложения. Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности". Действия можно выполнять с использованием набора данных DEMF.


## <a name="modify-format-to-collect-details-of-reporting"></a>Изменение формата для сбора сведений отчетности
1. Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".
2. В дереве разверните узел "Intrastat (model)".
3. В дереве выберите "Intrastat (model)\Intrastat (format)".
4. Выберите Конструктор.
5. В дереве разверните "Файл".
6. В дереве разверните "Файл\Декларация".
7. В дереве выберите "Файл\Декларация\Данные".
8. В поле "Кратность" выберите "Один — много".
    * Настройте этот элемент формата для архивирования сведений о процессе составления отчетности Интрастат. Этот элемент представляет запись заголовка архива.  
9. В дереве разверните "Файл\Декларация\Данные".
10. В дереве выберите "Файл\Декларация\Данные\Номенклатура".
11. В поле "Кратность" выберите "Ноль — много".
    * Настройте этот элемент формата для архивирования сведений о процессе составления отчетности Интрастат. Этот элемент будет представлять список архивированных строк.  
12. В дереве разверните "Файл\Декларация\Данные\Номенклатура".
13. В дереве выберите "Файл\Декларация\Данные\Номенклатура\Dim1".
14. Выберите "Да" в поле "Исключено".
    * Эти данные не будут архивироваться, поэтому этот элемент формата можно исключить из источника данных сведений о составлении отчетности Интрастат.  
15. В дереве разверните "Файл\Декларация\Данные\Номенклатура\Dim1".
16. В дереве выберите "Файл\Декларация\Данные\Номенклатура\Dim1\свойство".
17. Выберите "Да" в поле "Исключено".
18. В дереве выберите "Файл\Декларация\Данные\Номенклатура\Dim1\дата".
19. Выберите "Да" в поле "Исключено".
20. В дереве выберите "Файл\Декларация\Данные\Номенклатура\Dim2".
21. Выберите "Да" в поле "Исключено".
22. В дереве разверните "Файл\Декларация\Данные\Номенклатура\Dim2".
23. В дереве выберите "Файл\Декларация\Данные\Номенклатура\Dim2\свойство".
24. Выберите "Да" в поле "Исключено".
25. В дереве выберите "Файл\Декларация\Данные\Номенклатура\Dim2\код".
26. Выберите "Да" в поле "Исключено".
27. В дереве выберите "Файл\Декларация\Данные\Номенклатура\Dim3".
    * Несколько элементов формата могут иметь одно и то же имя. Например, "Dim". Их нельзя распознать явным образом при использовании этого формата в качестве источника данных для архивирования сведений о составлении отчетности Интрастат, поэтому необходимо определить альтернативные имена для этих элементов формата.   
28. В поле "Имя" введите "Сумма".
    * Сумма, руб.  
29. В поле "Кратность" выберите "Ровно один".
30. В дереве выберите "Файл\Декларация\Данные\Номенклатура\Dim4".
31. В поле "Имя" введите "Номенклатура".
    * Раздел  
32. В поле "Кратность" выберите "Ровно один".
    * В дополнение к элементам формата структуры должны архивироваться следующие сведения о составлении отчетности Интрастат: уникальный идентификатор записи каждой включенной в отчет номенклатуры товара и имя сформированного файла. Поскольку эти данные не будут присутствовать в отчете Интрастат, необходимо добавить формат, связанный с этими элементами сведений в качестве элементов источника данных.  
33. В дереве выберите "Файл\Декларация\Данные".
34. Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.
35. В дереве выберите "Источник данных\Номенклатура".
36. В поле "Имя" введите "Имя файла".
    * Имя файла  
37. В поле "Тип данных" выберите "Строка".
38. Нажмите кнопку "OК".
39. В дереве выберите "Файл\Декларация\Данные\Номенклатура".
40. Щелкните "Добавить элемент".
41. В поле "Имя" введите "Код записи товара".
    * Код записи товара  
42. В поле "Тип данных" выберите "Int64".
43. Нажмите кнопку "OК".
44. Перейдите на вкладку "Сопоставление".
45. В дереве выберите "Файл\Декларация\Данные\Имя файла".
46. Щелкните "Связать".
47. В дереве разверните узел "model".
48. В дереве разверните "модель\Транзакции".
49. В дереве выберите "Файл\Объявление\Данные\Номенклатура = модель.Проводки\Код записи товара".
50. В дереве выберите "модель\Проводки\Код записи товара".
51. Щелкните "Связать".
52. Нажмите кнопку "Сохранить".

## <a name="modify-format-to-memorize-details-of-reporting"></a>Изменение формата для запоминания сведений отчетности
1. Щелкните "Сопоставить формат модели".
2. Щелкните "Создать".
3. В поле "Определение" введите или выберите корневой элемент "Для обновления данных приложения".
    * Для обновления данных приложения  
4. В поле "Имя" введите "Сопоставление для обновления данных".
    * Сопоставление для обновления данных  
5. Нажмите кнопку "Сохранить".
    * Это сопоставление определяет, как будет происходить сбор сведений об отчете Интрастат в модели данных, структура которой задается выбранным корневым элементом "Для обновления данных приложения". Эти сведения, сопоставление модели с тем же корневым элементом "Для обновления данных приложения" и направление "В место назначения" будут использоваться для обновления данных приложения. Обновление данных начинается сразу же после формирования исходящего отчета Интрастат. Обратите внимание, что обновление данных приложения можно пропустить во время выполнения, однако модель данных должна быть пустой (содержащей пустой список записей).   
6. Выберите Конструктор.
    * Обратите внимание, что формат исходящего отчета Интрастат по умолчанию добавляется в качестве источника данных для этого сопоставления модели.  
    * Привяжите элементы разработанного отчета (представленного как источник данных) к элементам модели данных, которая фильтруется на основании выбранного корневого элемента модели.  
7. В дереве разверните "Заголовок архива".
8. В дереве разверните "Заголовок архива\Строки архива".
9. В дереве разверните "формат".
10. В дереве разверните "формат\Декларация: XML-элемент(Декларация)".
11. В дереве разверните "формат\Декларация: XML-элемент(Декларация)\Данные: XML-элемент 1..* (Данные)".
12. В дереве разверните "формат\Декларация: XML-элемент(Декларация)\Данные: XML-элемент 1..* (Данные)\Номенклатура: XML-элемент 0..* (Номенклатура)".
13. В дереве разверните "формат\Декларация: XML-элемент(Декларация)\Данные: XML-элемент 1..* (Данные)\Номенклатура: XML-элемент 0..* (Номенклатура)\Dim3: XML-элемент 1..1 (Сумма)'.
14. В дереве разверните "формат\Декларация: XML-элемент(Декларация)\Данные: XML-элемент 1..* (Данные)\Номенклатура: XML-элемент 0..* (Номенклатура)\Dim4: XML-элемент 1..1 (Номенклатура)'.
15. В дереве выберите "Заголовок архива\Число строк".
16. Щелкните "Изменить".
17. В дереве выберите "Список\COUNT".
18. Щелкните "Добавить функцию".
19. В дереве разверните "формат".
20. В дереве разверните "формат\Декларация: XML-элемент(Декларация)".
21. В дереве разверните "формат\Декларация: XML-элемент(Декларация)\Данные: XML-элемент 1..* (Данные)".
22. В дереве выберите "формат\Декларация: XML-элемент(Декларация)\Данные: XML-элемент 1..* (Данные)\Номенклатура: XML-элемент 0..* (Номенклатура)".
23. Щелкните "Добавить источник данных".
24. В поле "Формула" введите "COUNT(формат.Декларация.Данные.Номенклатура)".
    * COUNT (формат.Объявление.Данные.Номенклатура)  
25. Нажмите кнопку "Сохранить".
26. Закройте страницу.
27. В дереве выберите "Заголовок архива\Имя файла".
28. В дереве выберите "формат\Декларация: XML-элемент(Декларация)\Данные: XML-элемент 1..* (Данные)\Имя файла: Номенклатура String(Имя файла)'.
29. Щелкните "Связать".
30. В дереве выберите "формат\Декларация: XML-элемент(Декларация)\Данные: XML-элемент 1..* (Данные)\Номенклатура: XML-элемент 0..* (Номенклатура)\Dim4: XML-элемент 1..1 (Номенклатура)\номер: String(номер)".
31. В дереве выберите "Заголовок архива\Строки архива\Код номенклатуры".
32. Щелкните "Связать".
33. В дереве выберите "формат\Декларация: XML-элемент(Декларация)\Данные: XML-элемент 1..* (Данные)\Номенклатура: XML-элемент 0..* (Номенклатура)\Dim3: XML-элемент 1..1 (Сумма)\значение: Numeric Real(значение)".
34. В дереве выберите "Заголовок архива\Строки архива\Сумма".
35. Щелкните "Связать".
36. В дереве выберите "формат\Декларация: XML-элемент(Декларация)\Данные: XML-элемент 1..* (Данные)\Номенклатура: XML-элемент 0..* (Номенклатура)\Код записи товара: Номенклатура Int64(Код записи товара)'.
37. В дереве выберите "Заголовок архива\Строки архива\Код записи товара".
38. Щелкните "Связать".
39. В дереве выберите "Заголовок архива\Строки архива".
40. В дереве выберите "формат\Декларация: XML-элемент(Декларация)\Данные: XML-элемент 1..* (Данные)\Номенклатура: XML-элемент 0..* (Номенклатура)".
41. Щелкните "Связать".
42. В дереве выберите "Заголовок архива".
43. В дереве выберите "format\Declaration: XML Element(Declaration)Data: XML Element 1..* (Data)".
44. Щелкните "Связать".
45. Нажмите кнопку "Сохранить".
46. Закройте страницу.
47. Закройте страницу.
48. Закройте страницу.

