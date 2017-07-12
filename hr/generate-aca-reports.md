---
title: "Создание отчетов по закону Affordable Care"
description: "Функция доступна для помощи работодателям, которым необходимо отслеживать информацию в отчетах по формах 1095 B и 1095-C для поддержки части предписаний для работодателей по закону Affordable Care. Обратите внимание, что эта функция включена только для компаний в США."
author: kherr
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 61fa5dd3580c769457ea2cfdc669f68bd3b30980
ms.contentlocale: ru-ru
ms.lasthandoff: 06/13/2017


---
# <a name="generate-affordable-care-act-reports"></a>Создание отчетов по закону Affordable Care
Функция доступна для помощи работодателям, которым необходимо отслеживать информацию в отчетах по формах 1095 B и 1095-C для поддержки части **предписаний для работодателей** по закону Affordable Care. Обратите внимание, что эта функция включена только для компаний в США.

## <a name="getting-started"></a>Начало работы
При начале отслеживания информации в отчетах по формам 1095 B и 1095 C сначала необходимо создать одну или несколько группы покрытия по закону Affordable Care. Эти группы покрытия Affordable Care будут использоваться для указания предложения покрытия, предоставленного сотруднику, доли сотрудника от минимального ежемесячного вознаграждения (если затраты превышают федеральный уровень бедности), а также Safe Harbor, если используется работодателем. С помощью групп Affordable Care можно управлять информацией для этих полей без необходимости работы с записью каждого сотрудника, если условия одинаковые. Кроме того, группы покрытия Affordable Care можно легко назначить одному или нескольким сотрудникам с помощью функции массового назначение на странице.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Поддержка нескольких версий группы покрытия
Можно поддерживать несколько версий любой группы покрытия, которая позволяет вносить изменения для поддержания актуальной информации о группе без создания новой группы и переназначения сотрудников в нее при появлении каких-либо изменений в вашей организации или предлагаемых льгот. 

После создания необходимых групп покрытия Affordable Care можно выбрать массовое назначение групп для сотрудников с помощью функции **Массовое назначение** на странице или можно перейти к каждому сотруднику и указать, нужно ли отслеживать информацию ACA и вести отчетность для этого сотрудника, а также назначить сотруднику группу покрытия Affordable Care.

Если не для сотрудника нет необходимости отслеживать и учитывать информацию о покрытии Affordable Care, к примеру, если это сотрудник с частичной занятостью, в поле **Включать покрытие в отчет** можно задать значение "Нет". Несмотря на то что каждому сотруднику, для которого необходимо отслеживать сведения ACA, следует назначить группу покрытия Affordable Care, по-прежнему можно изменить параметры **Предложение покрытия**, **Доля затрат сотрудника** и **Safe Harbor** для любого месяца или месяцев, которые могут иметь разные значения по сравнению с указанными в группе покрытия Affordable Care.

Для ввода исключений для какого-либо из значений группы покрытия Affordable Care щелкните ссылку "Покрытие Affordable Care" на странице сведений работника, под разделом дополнительной информации на вкладке "Занятость".

## <a name="reporting-health-care-coverage"></a>Отчетность по покрытию здравоохранения
Помимо отслеживания того, распространяется ли медицинская страховка на сотрудника с полной занятостью, если работодатель предлагает сотруднику с самостоятельной страховкой, которая назначена сотруднику (независимо от способа занятости, полная или частичная), необходимо внести дополнительную информацию в 1095-C. Каждый работник (в том числе иждивенец), на которого распространяются планы льгот, должен быть включен в отчет за месяцы, которые были покрыты. 

Можно указать, должен ли план льгот вносится в отчетность, установив флажок **Для отчета ACA**.

Кроме того, если у сотрудника есть иждивенцы, которые подпадают под льготы, можно указать даты покрытия для каждого сотрудника на странице "Ведение льгот". Для указания того, что на иждивенца распространяются льготы, нажмите кнопку "Редактировать" в области действий на экспресс-вкладке "Иждивенцы".

На странице **Диспетчер дат покрытия для иждивенцев** можно указать даты, когда на иждивенца распространялись льготы. При вводе дат на этой странице автоматически будет поставлен флажок **Охвачено** на странице **Ведение льгот**.

## <a name="generate-1095b-and-1095c-forms"></a>Создание форма 1095B и 1095C
Можно также создать формы 109-B и 1095-C из продукта и распределить их по каждому сотруднику. Созданные электронным способом файлы 1095-C и соответствующие файлы 1094-C для передачи, которые могут быть использованы для отправки в IRS, можно также создавать в системе.  

При создании формы 1095-C введите в соответствующий календарный год или налоговый год, а также если требуется распечатать форму из двух или трех страниц. Трехстраничная форма нужна только в том случае, если работодатель покрытие самостоятельно застрахованному работнику и у работника больше шести иждивенцев, включая самого работника. При создании формы из двух страниц система автоматически определит, если у сотрудника имеется более чем 6 иждивенцев, охватываемых страховкой, и не будет включать сотрудника при создании формы. Кроме того, при создании трехстраничной формы система включит только сотрудников, имеющие более шести иждивенцев, охватываемых страховкой.

## <a name="viewing-information"></a>Просмотр сведений
Можно использовать страницу **Покрытие по закону Affordable Care работника** для просмотра сотрудников, для которых были назначены группы покрытия, где сотрудники не должны включаться в отчетность, и какие сотрудники не назначены.

Если какие-либо значения по умолчанию для группы покрытия Affordable Care были переопределены, рядом со значением, которое было изменено, появится звездочка. Если значения для всех 12 месяцев одинаковы и не были переопределены, значение будет указано в столбце **Все 12 месяцев**.

Также можно использовать окно запроса, чтобы понять, какие сотрудники были помечены как "Не для отчета ACA", что означает, что не требуется отслеживать, было ли им предложено покрытие, и для них не требуется выпускать 1095-C в конце года. Выбрав **Не для отчета ACA** в поле **Фильтр по**, можно создать список всех сотрудников, которые помечены как не получающие 1095-C.

Кроме просмотра списка сотрудников "Не для отчета ACA", можно также просмотреть сотрудников, не назначенных (поле **Покрытие отчетов ACA** пустое) или назначенных для группы покрытия Affordable Care, срок действия которой истек за год, выбранный в поле **Год**.

Можно экспортировать списки сотрудников, которые были созданы с одним из параметров фильтрации в Excel.

Если необходимо вставить в отчет, покрытых страховкой лиц, поскольку работодатель предлагает самостоятельное покрытие, можно также просмотреть иждивенцев, на которых распространяются планы льгот, которые были помечены как **Для отчета ACA**, выбрав действие "Просмотр покрытия иждивенца" на полосе области действий.

**Примечание:** только льготы, план которых был помечен как **Для отчета ACA** будет отображаться в окне запроса.
