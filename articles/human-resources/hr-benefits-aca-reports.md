---
title: Создание отчетов по закону Affordable Care (ACA)
description: Предусмотрена функциональность для помощи работодателям, которым необходимо отслеживать информацию в отчетах по формах 1095 B и 1095-C для выполнения предписаний для работодателей (Employer Mandate), предусмотренных законом Affordable Care. Обратите внимание, что эта функциональность включена только для компаний в США.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 47532861203fedbffc49aa92d25fc99de9d25376
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010353"
---
# <a name="generate-affordable-care-act-aca-reports"></a>Создание отчетов по закону Affordable Care (ACA)

Предусмотрена функциональность для помощи работодателям, которым необходимо отслеживать информацию в отчетах по формах 1095 B и 1095-C для выполнения предписаний для работодателей (**Employer Mandate**), предусмотренных законом Affordable Care. Обратите внимание, что эта функциональность включена только для компаний в США.

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

При создании формы 1095-C введите соответствующий налоговый год и укажите, должен ли скрываться номера социального страхования. При печати форм 1095-C для более чем 500 сотрудников вы получите несколько файлов PDF. Рекомендуется увеличить значение параметра **Максимальный размер файла** в окне **Параметры управления документами** до 150 МБ.

## <a name="viewing-information"></a>Просмотр сведений
Можно использовать страницу **Покрытие по закону Affordable Care работника** для просмотра сотрудников, для которых были назначены группы покрытия, где сотрудники не должны включаться в отчетность, и какие сотрудники не назначены.

Если какие-либо значения по умолчанию для группы покрытия Affordable Care были переопределены, рядом со значением, которое было изменено, появится звездочка. Если значения для всех 12 месяцев одинаковы и не были переопределены, значение будет указано в столбце **Все 12 месяцев**.

Также можно использовать окно запроса, чтобы понять, какие сотрудники были помечены как "Не для отчета ACA", что означает, что не требуется отслеживать, было ли им предложено покрытие, и для них не требуется выпускать 1095-C в конце года. Выбрав **Не для отчета ACA** в поле **Фильтр по**, можно создать список всех сотрудников, которые помечены как не получающие 1095-C.

Кроме просмотра списка сотрудников "Не для отчета ACA", можно также просмотреть сотрудников, не назначенных (поле **Покрытие отчетов ACA** пустое) или назначенных для группы покрытия Affordable Care, срок действия которой истек за год, выбранный в поле **Год**.

Можно экспортировать списки сотрудников, которые были созданы с одним из параметров фильтрации в Excel.

Если необходимо вставить в отчет, покрытых страховкой лиц, поскольку работодатель предлагает самостоятельное покрытие, можно также просмотреть иждивенцев, на которых распространяются планы льгот, которые были помечены как **Для отчета ACA**, выбрав действие "Просмотр покрытия иждивенца" на полосе области действий.

**Примечание:** только льготы, план которых был помечен как **Для отчета ACA** будет отображаться в окне запроса.