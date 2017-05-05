---
title: "Создание планов фиксированных компенсаций"
description: "Фиксированная компенсация ссылается на регулярную общую арплату или зарплаты сотрудника регулярную большую. Эта статья описывает компоненты, которые необходимо настроить перед использованием плана фиксированной компенсации и регистрацией сотрудников."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: bbf08a9620dbc8ad928fe40a3ae5e9b2a2fcb373
ms.lasthandoff: 03/31/2017


---

# <a name="create-fixed-compensation-plans"></a>Создание планов фиксированных компенсаций

[!include[banner](includes/banner.md)]


Фиксированная компенсация ссылается на регулярную общую арплату или зарплаты сотрудника регулярную большую. Этот раздел описывает компоненты, которые необходимо настроить перед использованием плана фиксированной компенсации и регистрацией сотрудников.

Суммы фиксированной компенсации можно рассчитать для работников на основании таких факторов, как производительность, регион и увеличения бюджета. Microsoft Dynamics 365 for Operations поддерживает типы компенсации для шага, уровня и диапазона.

## <a name="fixed-compensation-components"></a>Компоненты фиксированной компенсации
### <a name="compensation-levels"></a>Уровни компенсации

Можно использовать **уровни компенсации** для задания компенсации для различных должностей, чтобы гарантировать, что сотрудники, которые занимают эти должности, получают справедливую оплату. На странице **Уровни компенсации** можно настроить уровни компенсации, которые необходимы для каждого плана шага, уровня и диапазона. Кнопками **Вверх** и **Вниз** укажите правильный порядок уровней согласно их типу. Настроив уровни компенсации для задания, вы можете гарантировать, что все сотрудники, которые находятся в должности для выполнения этого задания, будут получать оплату на одном уровне.

### <a name="reference-points"></a>Опорные точки

**Опорные точки** — это столбцы в сетке, которые определяют диапазоны компенсации для каждого уровня. Уровень компенсации — это строка в сетке. Типичными опорными точками для плана типа уровня являются минимальное, среднее и максимальное значения. Опорные точки создаются на странице **Установки опорных точек**.

### <a name="compensation-grids"></a>Сетка компенсации

После настройки уровней и опорных точек их можно объединить для создания **сетки компенсации**. На странице **Сетки компенсаций** определите информацию о решетке. Например, укажите, для чего предназначена сетка, с каким типом плана она будет использоваться и какие опорные точки или столбцы необходимы в сетке. После ввода этой информации щелкните **Структура компенсации**, чтобы добавить уровни и суммы в сетку. 

**Подсказка.** Используйте функцию **Массовые изменения** в структуре компенсации, чтобы задать исходные суммы, а затем выполните приращение по процентам или суммам на уровнях или в опорных точках.

### <a name="pay-frequencies"></a>Частота оплат

**Частота оплат** используется для определения способа указания зарплаты сотрудников (например, 10 долларов США в час, а не 50 000 долларов США в год), и преобразования между почасовыми, еженедельными, ежемесячными (12 месяцев) и годовыми ставками. Например, компания, которая использует 38-часовую рабочую неделю для сотрудников с почасовой оплатой, настраивает частоту оплаты, которая имеет почасовую ставку 1, еженедельную ставку 38, ежемесячную ставку 164,6666666667 и годовую ставку 1 976. Эти преобразования используются для расчета различных ставок оплаты, которые отображаются в записи фиксированной компенсации сотрудника.

## <a name="fixed-compensation-plans"></a>Планы фиксированной компенсации
Вы разработать план фиксированной компенсации для объединения всех настроенных компонентов. Чтобы создать план фиксированной компенсации, перейдите на страницу **Планы фиксированной компенсации**. Здесь можно присвоить плану имя и добавить для него описание, выбрать тип плана (пошаговый, ступенчатый или ленточный), выбрать частоту оплаты, которая будет использоваться для ставки платы сотрудника (количество в час, в год и так далее) и настроить некоторые параметры, которые управляют обработкой компенсации. 

Параметр **Вне допустимого диапазона** позволяет указать, насколько важно, чтобы суммы компенсации находились в пределах между минимальной и максимальной суммами. Допуск **Жестко** требует, чтобы компенсация находилась в пределах диапазона, определенного для данного уровня. Допуск **Мягко** предупреждает вас, когда сумма компенсации выходит за пределы диапазона, но позволяет продолжать работу. Если задать для допуска значение **Нет**, можно ввести любую сумму компенсации для сотрудника, не получая предупреждения или сообщения об ошибках. 

Параметр **Правило найма** позволяет указать, должны ли все сотрудники получить одинаковое повышение независимо от даты найма (**Правило найма** = **Нет**) или должны ли сотрудники получать процент от вознаграждения на основании продолжительности их занятости в цикле (**Правило найма** = **Процент**). 

**Матрица использования диапазона** полезна, если требуется сократить время, которое необходимо сотрудникам для достижения средней точки их диапазона, или увеличить время, которое необходимо сотрудникам для достижения максимальной опорной точки в диапазоне. Например, вы хотите дать сотрудникам, которые находятся в нижних 25 процентах их диапазона, 110 процентов елевого вознаграждения, при этом вы хотите дать сотрудникам, которые находятся в верхних 25 процентах их диапазона только 80 процентов целевого вознаграждения, чтобы не дать им достигнуть максимума так быстро. 

После определения базовых данных для плана фиксированной компенсации можно настроить структуру компенсации для плана. Щелкните **Установить компенсацию**. Открывается диалоговый слайдер, который предоставляет три возможности:

-   Создание новой сетки компенсации путем выбора настройки опорной точки и предоставления имени сетки.
-   Создание новой сетки компенсации путем создания копии существующей сетки, которую можно использовать как начальную точку.
-   Использование существующей сетки компенсации, которая уже определена. Все планы компенсации, которые используют одну и ту же сетку, получают обновления при изменении этой сетки.

После выбора варианта откроется страница **Структура компенсации**, и вы сможете внести изменения в новую или существующую сетку компенсации.

## <a name="fixed-compensation-enrollment"></a>Регистрация фиксированной компенсации
### <a name="determine-who-is-eligible-for-the-plan"></a>Определение лиц для регистрации в плане

Первым шагом регистрации сотрудников в плане фиксированной компенсации является определение того, кто имеет право получать компенсацию, которая определена в плане. Пока не будет определено право на компенсацию, будет невозможно назначить план сотруднику. Чтобы настроить права, откройте страницу **Правила приемлемости**. Здесь создаются новые правила приемлемости для плана компенсации и определяются критерии, которым должен отвечать сотрудник, чтобы иметь право на план. Право на план можно ограничить на основании подразделения, профсоюза, региона компенсации (расположения), должности, функциональных обязанностей или уровня компенсации. Сотрудники могут зарегистрироваться в плане компенсации, только если они отвечают всем условиям, заданным в правиле приемлемости. 

**Примечание.** Правила приемлемости используются для определения приемлемости как в планах фиксированной, так и переменной компенсации. 

Правило приемлемости учитывает значение определенных полей в записях заданий, должности и сотрудника для определения того, имеет ли сотрудник право на план компенсации.

-   На странице **Задание** правило приемлемости учитывает следующие поля:
    -   Поле **Задание**
    -   На вкладке **Классификация задний** поля **Функция** и **Тип задания**
    -   На вкладке **Компенсация** поле **Уровень**
-   На странице **Должности** правило приемлемости учитывает поля **Подразделение** и **Регион компенсации**.

Правило приемлемости также учитывает профсоюзы, которые связаны с сотрудником (на странице **Сотрудники** на вкладке **Работник** щелкните **Личные данные** &gt; **Профсоюзы**).

### <a name="define-fixed-compensation-actions"></a>Определение действий по фиксированной компенсации

**Действия по фиксированной компенсации** используются при внесении или применении изменений к фиксированной компенсации сотрудника. Действия по фиксированной компенсации позволяют давать описательные имена типам действий, которые может выполнять менеджер по компенсациям и льготам. Различные типы действий имеют специальную логику, чтобы их можно было использовать в определенных ситуациях. 

Например, при настройке фиксированной компенсации для сотрудника можно использовать только действия, которые имеют **Прием на работу/Повторный прием на работу**. В этом случае может потребоваться создать три различных действия типа **Прием на работу/Повторный прием на работу** и назвать их **Прием на работу**, **Повторный прием на работу** и **Перевод**. После этого вы будете иметь более описательное объяснение того, почему фиксированная компенсация была предоставлена сотруднику или почему она была изменена.

### <a name="enroll-the-employee"></a>Регистрация сотрудника

Теперь можно назначить сотрудника плану фиксированной компенсации. Откройте страницу **Сотрудники** и выберите сотрудника для регистрации в плане компенсации. В области действий щелкните **Компенсация** &gt; **Фиксированный план**. Теперь можно создать новое действие фиксированной компенсации для этого сотрудника. 

**Примечание.** В поле плана компенсации отображаются только планы, на которые сотрудник имеет право согласно правилам приемлемости, настроенным для каждого плана. Если правила приемлемости не настроены для плана, то никакие сотрудники не будут иметь право на этот план. 

Система проверяет, что сумма компенсации, указанная для плана компенсации ступенчатого или ленточного типа, находится в пределах минимальной и максимальной опорных точек для данного уровня компенсации в задании сотрудника. Если сумма компенсации выходит за пределы допустимого диапазона, отображается предупреждение или сообщение об ошибке в зависимости от уровня допуска, заданного для плана фиксированной компенсации.

<a name="see-also"></a>См. также
--------

[Планы компенсации](compensation-plans.md)



