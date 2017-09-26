---
title: "Обзор управления качеством"
description: "Эта статья описывает, как можно использовать управление качеством в Microsoft Dynamics 365 for Finance and Operations, чтобы улучшить качество продукта в вашей цепи поставок."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: c2c7a9c82809bd989eb362995dfe8e6d7829e89d
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---

# <a name="quality-management-overview"></a>Обзор управления качеством

[!include[banner](../includes/banner.md)]


Эта статья описывает, как можно использовать управление качеством в Microsoft Dynamics 365 for Finance and Operations, чтобы улучшить качество продукта в вашей цепи поставок.

Управление качеством может помочь вам управлять периодами оборота, когда вы работаете с несоответствующими продуктами, независимо от их источника происхождения. Поскольку диагностические типы связаны с отчетностью о коррекции, Microsoft Dynamics 365 for Finance and Operations может планировать задачи для исправления проблем и предотвращения их повторения.

В дополнение к функциональности для управляя несоответствием, управление качеством включает функциональность для отслеживания проблем по типу проблемы (даже внутренние проблемы), и для определения решений как краткосрочные или долгосрочные. Статистика по ключевым индикаторам производительности обеспечивает анализ истории предыдущих проблем несоответствия и решений, которые были применены для их исправления. Вы можете использовать исторические данные для просмотра эффективности предыдущих мер по обеспечению качества и определить соответствующие меры для использования в будущем.

При указании сопоставления контроля качества Finance and Operations может сформировать заказы по контролю качества для различных бизнес-процессов, событий и условий. Сопоставление может относиться к определенной номенклатуре, группе или ко всем продуктам.

## <a name="examples-of-the-use-of-quality-management"></a>Примеры использования управления качеством
Управление качеством гибкое и может быть реализована различными способами для соответствия требованиям определенных уровней операций цепочки снабжения. Следующие примеры иллюстрируют возможное использование этих функций.

-   Автоматический запуск процесса контроля качества, основанный на предопределенных критериях (после регистрации на складе заказа на покупку от определенного поставщика).
-   Блокировка запасов во время проверки для исключения использования неутвержденных запасов (полная блокировка количеств по заказу на покупку).
-   Использование выборочного контроля номенклатур в рамках ассоциации качества для того, чтобы определить сумму текущих физических запасов, которые необходимо проверить. Выборочный контроль может быть основан на фиксированных количествах или на процентном объеме.
-   Создайте заказы для контроля качества для частичных приемок. Чтобы создать заказ для контроля качества, основанный на количестве, физически полученном с заказом, необходимо установить флажок **На обновленное количество** в форме **Выборка элементов**.
-   Создание типов испытаний, которые включают минимальные, максимальные и целевые значения испытаний, и выполнение качественного или количественного тестирования с предопределенными результатами проверки.
-   Указание допустимого уровня качества (AQL) для управления допусками измерения качества.
-   Указание ресурсов, которые требуются для контрольной операции, например испытательный участок и инструменты для испытаний.

## <a name="working-with-quality-associations"></a>Работа с сопоставлениями контроля качества
Бизнес-процесс, использующий сопоставления, может быть связан с различными исходными документами, такими как заказы на покупку, заказы на продажу и производственные заказы.

Каждая запись сопоставления качества определяет также набор тестов, AQL и план выборочного контроля, применимые для создаваемых автоматически качественных заказов. Необходимо определить запись сопоставления контроля качества для каждого изменения бизнес-процесса, требующего автоматического создания заказа контроля качества. Например, можно создать сопоставление, которое формирует заказ контроля качества для заказов на продажу, когда обновляется поступление продуктов по заказу на покупку. В зависимости от настройки плана исполнения возможна блокировка самого запускающего процесса, пока имеется открытый заказ для контроля качества, или блокировка следующих процессов, таких как выставление накладной по заказу на покупку.

**Примечание.** Пока имеются открытые заказы для контроля качества, количества запасов автоматически блокируются по выдаче. В зависимости от настройки **Полная блокировка** на странице **Выборка номенклатур**, количество равно количеству в заказе для контроля качества или количеству в строке исходного документа.

Сопоставление по контролю качестве указывает событие и условия, при которых формируется заказ на контроль качества для определенного бизнес-процесса. Условия могут быть заданы для определенного места или юридического лица. Заказ по контролю качества, в котором используются разрушающие испытания, может формироваться, только если для данного события имеется складской запас.

Следующие примеры иллюстрируют определение записи сопоставления качества для отклонений в бизнес-процессах. Примеры обобщаются также в следующей таблице в плане событий и условий, определенных записью сопоставления качества.

<table>
<tbody>
<tr>
<th>Тип ссылки</th>
<th>Тип события</th>
<th>Выполнение</th>
<th>Блокировка событий</th>
<th>Ссылка на документ</th>
</tr>
<tr>
<td>Запасы</td>
<td>Неприменимо</td>
<td>Неприменимо</td>
<td>Нет</td>
<td>Все</td>
</tr>
<tr>
<td rowspan="7">Прод.</td>
<td rowspan="4">Процесс комплектации запланирован</td>
<td rowspan="4">До</td>
<td>Нет</td>
<td rowspan="22">Только определенный код, группа или все</td>
</tr>
<tr>
<td>Процесс комплектации</td>
</tr>
<tr>
<td>Отборочная накладная</td>
</tr>
<tr>
<td>Счет</td>
</tr>
<tr>
<td rowspan="3">Отборочная накладная</td>
<td rowspan="3">До</td>
<td>Нет</td>
</tr>
<tr>
<td>Отборочная накладная</td>
</tr>
<tr>
<td>Счет</td>
</tr>
<tr>
<td rowspan="15">Покупка</td>
<td rowspan="7">Список поступлений</td>
<td rowspan="4">До</td>
<td>Нет</td>
</tr>
<tr>
<td>Список поступлений</td>
</tr>
<tr>
<td>Поступление продуктов</td>
</tr>
<tr>
<td>Счет</td>
</tr>
<tr>
<td rowspan="3">После</td>
<td>Нет</td>
</tr>
<tr>
<td>Поступление продуктов</td>
</tr>
<tr>
<td>Счет</td>
</tr>
<tr>
<td rowspan="3">Регистрация</td>
<td rowspan="3">Неприменимо</td>
<td>Нет</td>
</tr>
<tr>
<td>Поступление продуктов</td>
</tr>
<tr>
<td>Счет</td>
</tr>
<tr>
<td rowspan="5">Поступление продуктов</td>
<td rowspan="3">До</td>
<td>Нет</td>
</tr>
<tr>
<td>Поступление продуктов</td>
</tr>
<tr>
<td>Счет</td>
</tr>
<tr>
<td rowspan="2">После</td>
<td>Нет</td>
</tr>
<tr>
<td>Счет</td>
</tr>
<tr>
<td rowspan="8">Производство</td>
<td rowspan="3">Регистрация</td>
<td rowspan="3">Неприменимо</td>
<td>Нет</td>
<td rowspan="12">Все</td>
</tr>
<tr>
<td>Приемка</td>
</tr>
<tr>
<td>Конец</td>
</tr>
<tr>
<td rowspan="5">Приемка</td>
<td rowspan="3">До</td>
<td>Нет</td>
</tr>
<tr>
<td>Приемка</td>
</tr>
<tr>
<td>Конец</td>
</tr>
<tr>
<td rowspan="2">После</td>
<td>Нет</td>
</tr>
<tr>
<td>Конец</td>
</tr>
<tr>
<td rowspan="4">Карантин</td>
<td rowspan="3">Приемка</td>
<td rowspan="2">До</td>
<td>Приемка</td>
</tr>
<tr>
<td>Конец</td>
</tr>
<tr>
<td>После</td>
<td>Конец</td>
</tr>
<tr>
<td>Конец</td>
<td>До</td>
<td>Конец</td>
</tr>
<tr>
<td rowspan="3">Операция маршрута</td>
<td rowspan="3">Приемка</td>
<td rowspan="2">До</td>
<td>Нет</td>
<td rowspan="3">Определенный код, группа или специфичный для ресурса, группа или все</td>
</tr>
<tr>
<td>Приемка</td>
</tr>
<tr>
<td>После</td>
<td>Нет</td>
</tr>
<tr>
<td rowspan="3">Производство сопутствующих продуктов</td>
<td>Регистрация</td>
<td>Неприменимо</td>
<td rowspan="3">Нет</td>
<td rowspan="3">Все</td>
</tr>
<tr>
<td rowspan="2">Приемка</td>
<td>До</td>
</tr>
<tr>
<td>После</td>
</tr>
</tbody>
</table>

В таблице ниже приведены дополнительные сведения о том, как формируются заказы для определенных типов процессов.
<div class="tableSection">

<table>
<tbody>
<tr>
<th>Тип процесса</th>
<th>Когда можно автоматически формировать заказы по контролю качества</th>
<th>Когда можно формировать заказа, если применяются разрушающие испытания</th>
<th>Описание условия</th>
<th>Сведения о ручном формировании</th>
</tr>
<tr>
<td>Заказ на покупку</td>
<td>До или после разноски поступления продуктов получаемого материала</td>
<td>После разноски отборочной накладной на полученные материалы, поскольку материалы должны быть доступны для проведения испытаний с разрушением.</td>
<td>Потребность в заказе на контроль может отражать конкретный объект, номенклатуру или поставщика, либо сочетание этих условий.</td>
<td>Созданный вручную качественный заказ, относящийся к заказу на продажу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</td>
</tr>
<tr>
<td>Карантинный заказ</td>
<td>До или после завершения карантинного заказа</td>
<td>Нельзя формировать заказы с разрушительными испытаниями. Предполагается, что функции карантинного заказа учитывают разрушаемые материалы.</td>
<td>Потребность в заказе на контроль может отражать конкретный объект, номенклатуру или поставщика, либо сочетание этих условий.</td>
<td>Созданный вручную качественный заказ, относящийся к карантинному заказу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</td>
</tr>
<tr>
<td>Заказ на продажу</td>
<td>Перед обновлением запланированного процесса комплектации или отборочной накладной для отгружаемых номенклатур</td>
<td>В любом шаге</td>
<td>Потребность в заказе на контроль может отражать конкретный объект, номенклатуру или заказчика, либо сочетание этих условий.</td>
<td>Созданный вручную качественный заказ, относящийся к заказу на продажу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</td>
</tr>
<tr>
<td>Производственный заказ</td>
<td>До или после регистрации завершенного количества для производственного заказа</td>
<td>После регистрации завершенного количества для производственного заказа</td>
<td>Потребность в заказе на контроль может отражать конкретный объект или номенклатуру, либо сочетание этих условий.</td>
<td>Созданный вручную качественный заказ, относящийся к производственному заказу может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</td>
</tr>
<tr>
<td>Производственный заказ с операцией маршрута</td>
<td>До или после завершения отчета по операции</td>
<td>После регистрации завершения производства по последней операции</td>
<td>Потребность в заказе на контроль может отражать конкретный объект, ресурс операции, либо сочетание этих условий.</td>
<td>Созданный вручную заказ для контроля качества, относящийся к операции маршрута, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</td>
</tr>
<tr>
<td>Запасы</td>
<td>Заказ для контроля качества не может быть создан автоматически для проводки в журнале запасов (например, журнал прибылей и убытков или журнал инвентаризации) или для проводок заказов на перемещение.</td>
<td></td>
<td></td>
<td>Невозможно создать заказ контроля качества для складского количества номенклатуры. Требуются физические запасы в наличии.</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a>Страницы управления качеством
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Страница</th>
<th>Описание</th>
<th>Пример</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Сопоставления контроля качества</td>
<td>См. предыдущие разделы этой статьи.</td>
<td>Ассоциация качества определяет всю следующую информацию для созданного заказа для контроля качества:
<ul>
<li>Событие проводки</li>
<li>Набор проверок, которые необходимо выполнить для номенклатур</li>
<li>Допустимый уровень качества</li>
<li>План выборочного контроля</li>
</ul>
Необходимо определить сопоставление контроля качества для каждого изменения бизнес-процесса, требующего автоматического создания заказов для контроля качества. Например, заказ для контроля качества может создаваться в бизнес-процессах для заказов на покупку, карантинных заказов, заказов на продажу и производственных заказов.</td>
</tr>
<tr class="even">
<td>Тесты</td>
<td>Эта страница используется для назначения и просмотра отдельных испытаний, определяющих соответствие вашей продукции требованиям к качеству. Вы можете назначить одни или несколько индивидуальных испытаний в группе проверки. В этом случае вы также определяете информацию, специфичную для теста, такую как приемлемые значения измерения. Значения измерения используются для испытаний с количественными результатами, и переменные испытания используются для качественных испытаний.
<ul>
<li>Количественное испытание имеет тип испытания <strong>Целое число</strong> или <strong>Дробь</strong>, и также имеет обозначенную единицу измерения. Спецификации качества и результаты теста выражаются числами.</li>
<li>Качественное испытание имеет тип проверки <strong>Параметр</strong>. Для качественных испытаний требуется дополнительная информация об измеряемой тестовой переменной и ее возможных перечислимых вариантах. Спецификации качества и результаты теста выражаются в соответствии с результатом.</li>
</ul></td>
<td>Производственная компания проводит два испытания купленных материалов: количественное испытание качества материала и качественную проверку повреждения упаковки. Компания определяет дополнительную информацию о качественном испытании, чтобы идентифицировать переменную испытания (поврежденная упаковка) и ее результаты. Компания использует страницу <strong>Группы проверки</strong> для того, чтобы назначить два испытания в группу проверки и указать информацию, специфичную для испытания. Группа испытаний назначается заказу контроля качества, таким образом компания может составить отчет по результатам этих двух испытаний.</td>
</tr>
<tr class="odd">
<td>Группы проверки</td>
<td>Эта страница используется для настройки, изменения и просмотра групп проверки и отдельных проверок, включенных в проверочную группу. В верхней области отображаются группы испытаний, а в нижней области отображаются испытания, включенные в выбранную группу испытаний. Группе испытаний назначаются несколько политик, такие как план выборочного контроля, приемлемый уровень качества и потребности для испытаний с разрушением. Когда вы назначаете индивидуальное испытание для контрольной группы, вы определяете дополнительную информацию, такую как последовательность, документы и даты срока действия. Для количественного испытания информация, которую вы определяете, также включает приемлемые значения измерений. Для качественного испытания информация включает переменную испытания и результат по умолчанию. Группа проверок, назначенная заказу на контроль качества, определяет начальный набор испытаний, которые должны выполняться для указанной номенклатуры. Однако можно в заказе для контроля качества можно добавлять, удалять или изменять испытания. Результаты проверок указываются для каждой проверки в заказе контроля качества.</td>
<td>Производственная компания определяет группу испытаний для каждой разновидности своих инструкций по обеспечению качества. Разные группы испытаний отражают различия планов выборочного контроля, наборов испытаний, которые должны быть выполнены совместно, приемлемых уровней качества, а также других коэффициентов. Для испытаний с количественными результатами также имеются различия в приемлемых значениях измерений. Чтобы обеспечить принудительное выполнение инструкций по обеспечению качества, компания назначает проверочную группу для каждого правила автоматического создания заказов контроля качества (на странице <strong>Сопоставления контроля качества</strong>), а также назначает проверочную группу создаваемым вручную заказам для контроля качества.</td>
</tr>
<tr class="even">
<td>Группы контроля качества номенклатуры</td>
<td>Эта страница используется для настройки, изменения и просмотра номенклатур, назначенных группе контроля качества, или групп контроля качества, назначенных номенклатуре. Группа контроля качества определяет общие требования к проверке номенклатур. После определения требованиям к испытанию на странице <strong>Группы проверки</strong> вы можете определить правила для автоматического создания заказов для контроля качества. Для того, чтобы упростить процесс, вы не определяете правила для индивидуальных номенклатур. Вместо этого вы определяете правила для группы качества путем использования страницы <strong>Сопоставления контроля качества</strong>. Вы можете также использовать страницу <strong>Группы контроля качества номенклатуры</strong> для выбранной группы качества, чтобы назначить соответствующие номенклатуры для этой группы. Вы можете также использовать страницу <strong>Группы контроля качества номенклатуры</strong> для выбранной номенклатуры, чтобы назначить соответствующую группу качества для этой номенклатуры.</td>
<td>Производственная компания приобретает различные виды сырья, для которых действуют одинаковые требования по проверке во время входного контроля. Компания определяет группу качества, и после этого назначает коды номенклатур, которые связаны с сырьем, для этой группы. Позднее компания покупает новый тип сырья, которое имеет такие же требования к испытаниям. Вместо настройки новых требований к испытаниям для нового материала компания добавляет код номенклатуры для нового материала к существующей группе качества. Эта же производственная компания также производит номенклатуры, которые имеют одинаковые требования в отношении производственных испытаний и одинаковые требования в отношении проведения испытаний перед отгрузкой. Компания определяет две дополнительные группы контроля качества и назначает соответствующие коды номенклатур каждой группе.</td>
</tr>
<tr class="odd">
<td>Переменные проверки</td>
<td>Используйте эту страницу для определения и просмотра переменных, связанных с качественным испытанием. Для каждой переменной вы определяете перечислимые результаты, которые представляют возможные варианты. Вы определяете испытания на странице <strong>Тесты</strong>. Для качественных тестов вы должны установить тип испытания <strong>Параметр</strong>. Используйте страницу <strong>Группы проверки</strong> для назначения тестовой переменной отдельному тесту.</td>
<td>Производственная компания, выпускающая печенье, использует инспекционный тест для готовой продукции. Этот инспекционный тест имеет несколько переменных. Одна из переменных — вкус, при этом возможные результаты для этой переменной — хороший или плохой. Вторая переменная — цвет, возможные результаты — "слишком темное", "слишком светлое" и "правильный".</td>
</tr>
<tr class="even">
<td>Результаты переменной проверки</td>
<td>Используйте эту страницу для настройки, изменения и просмотра возможных результатов испытаний тестовой переменной, связанной с качественным испытанием. Для каждого результата назначается статус <strong>приемлемый</strong> или <strong>неприемлемый</strong>. Следует определить переменную и ее результаты для каждого качественного испытания, которое определено на странице <strong>Тесты</strong> (Для качественных тестов задается тип испытания <strong>Параметры</strong> на странице <strong>Тесты</strong>.) Используйте страницу <strong>Группы проверки</strong>, чтобы назначить тестовую переменную и результат по умолчанию для отдельного качественного испытания.</td>
<td>Производственная компания, выпускающая печенье, использует инспекционный тест для готовой продукции. Этот инспекционный тест имеет несколько переменных. Одна из переменных — вкус, при этом возможные результаты для этой переменной — хороший или плохой. Вторая переменная — цвет, возможные результаты — "слишком темное", "слишком светлое" и "правильный". Для каждого результата назначен статус <strong>положительного</strong> или <strong>отрицательного</strong> результата. В ходе проверки каждой переменной инспектор создает отчет о результатах, выбирая один из вариантов.</td>
</tr>
</tbody>
</table>



<a name="see-also"></a>См. также
--------

[Процессы управления качеством](quality-management-processes.md)

[Включение управления несоответствиями](enable-nonconformance-management.md)
