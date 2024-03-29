---
title: Анализ результатов анкеты
description: Статистику анкетирования можно использовать для расчета среднего, итогов и процентов по набору демографических данных.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1da18dd32363308438b7f9da5b2e04e119e840cb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692929"
---
# <a name="analyzing-questionnaire-results"></a>Анализ результатов анкеты


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Статистику анкетирования можно использовать для расчета среднего, итогов и процентов по набору демографических данных. Чтобы начать эту процедуру, перейдите в раздел **Анкета** > **Просмотр и анализ результатов** > **Статистика анкетирования**. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.


## <a name="create-a-questionnaire-statistics-record"></a>Создание записи статистики анкетирования
1. Перейдите в раздел **Статистика анкетирования**.
2. Нажмите кнопку **Создать**.
3. В списке пометьте выбранную строку.
4. В поле **Статистика** введите значение.
5. В поле **Описание** введите значение.
6. В поле **Анкета** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
7. В списке перейдите по ссылке в выбранной строке.
8. Перейдите на вкладку **Общие**.
    * Укажите, следует ли включить анонимные результаты или результаты от работников, контактных лиц и кандидатов.  
9. Установите или снимите флажок **Работник**.
    * Если вы будете просматривать результаты по трудовом стажу или возрасту, укажите интервалы, которые вам хотелось бы использовать для группирования результатов.  
    * Если ввести в качестве возрастного интервала 5, результаты будут сгруппированы по пятилетним интервалам.  
10. В поле **Возраст** введите число.
    * Укажите, следует ли запустить расчет для всей анкеты, для каждой группы результатов, для каждого вопроса или для каждой строки вопроса.  
    * Выберите, как требуется сгруппировать результаты.  
    * Например, при расчете среднего количества баллов на вопрос имеет смысл просматривать вопросы сгруппированными по группе результатов.  
    * Выберите данные, на которых будет основан расчет.  
    * Например, если вы хотите просматривать средний полученный по анкете процент по своим работникам, а не среднее полученное количество баллов по работникам.  
11. Перейдите на вкладку **Диапазон**.
    * Диапазоны позволяют ограничить набор результатов только результатами, отвечающими критериям диапазона.  
12. Перейдите на вкладку **Группировка по**.
    * Группировки используются для определения того, как должны отображаться результаты.  
    * Например, группируйте результаты сначала по полу, а затем по возрасту.  
13. В списке найдите и выберите требуемую запись.
    * Переместите группировки на строну **Выбранные** и расположите их в требуемом порядке.  

## <a name="execute-the-statistics-calculation"></a>Выполнение расчета статистики
1. Щелкните **Выполнить**.
    * Выберите функцию расчета, которую требуется выполнить над результатами.  
    * Например, рассчитайте средние проценты по анкете для выбранных группировок или просуммируйте баллы по группам результатов для выбранных группировок.  
2. Установите или снимите флажок **Удалить результаты предыдущих поисков**.
3. Щелкните **OK**.

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a>Просмотрите результаты расчета статистики анкетирования.
1. Щелкните **Результат**.
2. Щелкните **Результат**.
3. Закройте страницу.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
