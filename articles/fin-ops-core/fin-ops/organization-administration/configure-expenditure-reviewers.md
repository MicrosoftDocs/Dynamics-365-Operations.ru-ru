---
title: Настройка рецензентов расходов
description: В этой теме описывается, как использовать рецензентов расходов для динамического выбора пользователя, которому назначена задача документооборота, утверждение или принятие решения вручную.
author: rachel-profitt
ms.date: 06/25/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2021-06-24
ms.openlocfilehash: b0de3d9280c43fc7e2bb2568d4a57250da4dfebf
ms.sourcegitcommit: 9f3b6c00f82694b5f8eb1bda75411801c0fccf4a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2021
ms.locfileid: "6315687"
---
# <a name="configure-expenditure-reviewers"></a>Настройка рецензентов расходов
[!include[banner](../includes/banner.md)]

Можно настроить динамических рецензентов расходов, чтобы направлять расходы для проверки на основе пользователя, которому назначена роль в проекте или финансовой аналитики, где происходит расход. Workflow-процесс использует указанную роль проекта или владельца финансовой аналитики, чтобы определить, кому направить расход.

Можно определить одну или несколько конфигураций рецензента расходов, а затем выбрать конфигурацию при создании workflow-процесса. Можно настроить значения рецензента расходов для каждого юридического лица вашей организации. После определения конфигурации рецензента расходов назначается конфигурация. Рецензенты расходов могут быть назначены задачам документооборота, утверждениям и ручным решениям.

> [!NOTE]
> Хотя рецензенты расходов не являются обязательными, они могут помочь упростить настройку документооборота. Например, нет необходимости создавать одно условное решение для проверки каждой аналитики центра затрат, а затем создавать другой элемент, чтобы назначить утверждение или задачу конкретному пользователю или группе пользователей. Вместо этого можно настроить владельца аналитики центра затрат и воспользоваться рецензентом расходов для динамического выбора правильного пользователя. Таким образом, при изменении владения или назначения центров затрат необходимо только обновить поле **Владелец** для финансовой аналитики.

## <a name="types-of-expenditure-reviewers"></a>Типы рецензентов расходов

Не все бизнес-правила поддерживают концепцию рецензентов расходов. По умолчанию можно настроить проверяющих расходы для заявок на закупку, заказов на покупку, накладных по покупкам и отчетов о расходах. Каждый из этих типов рабочих процессов требует настройки рецензентов расходов на отдельной странице, относящейся к конкретному компоненту и модулю. Рецензенты расходов для каждого поддерживаемого документа могут использоваться как с рабочими процессами на уровне заголовка, так и с документооборотом на уровне строки.

В следующей таблице показано, как настроить проверяющего расходов для каждого поддерживаемого документа.

| Документ | Путь навигации |
|----------|-----------------|
| Отчеты о расходах | Управление расходами \> Настройка \> Политики \> Рецензенты расходов |
| Заказы на покупку | Закупки и источники \> Настройка \> Политики \> Рецензенты расходов заказа на покупку |
| Заявки на закупку | Закупки и источники \> Настройка \> Политики \> Рецензенты расходов заявки на покупку |
| Счета поставщиков | Расчеты с поставщиками \> Настройка политики \> Рецензенты расходов накладных поставщиков |

## <a name="expenditure-reviewer-assignments"></a>Назначения рецензента расходов

Для каждого рецензента расходов доступны два типа назначений: *распределения проектов* и *распределения организаций*. Для распределения проекта можно выбрать между органами проектов и финансовыми аналитиками. Для распределения организации можно выбрать финансовые аналитики.

В органах проектов содержится руководитель проекта, контроллер проекта и руководитель отдела продаж проектов. Эти органы определяются непосредственно в проекте путем выбора сотрудника в соответствующих полях.

Управление финансовой аналитикой осуществляется с помощью структур счетов в каждом юридическом лице. Для каждого юридического лица можно выбрать финансовые аналитики, которые будут использоваться в проверяющем расходах. Аналитики могут быть получены из проекта (в этом случае выбираются аналитики на вкладке **Распределения проектов**) или в документе (в этом случае выбираются аналитики на вкладке **Распределения организации**). В поле **Владелец** на странице **Значения финансовых аналитик** можно выбрать работника для каждой финансовой аналитики.

## <a name="example-1-expenditure-reviewers-based-on-organization-distributions"></a>Пример 1. Проверяющие расходов на основе распределений организаций

Вы работаете на Contoso Appliances, и ваша организация имеет шесть отделов и 10 центров затрат. При отправке новой заявки на закупку ее утверждение должно быть сначала получено от руководителя подразделения, а затем от менеджера центра затрат.

В данном примере настраиваются два *рецензента расходов по заявкам на закупку*:

- Для первого проверяющего назовите подразделение, а затем выберите финансовую аналитику **Подразделение** на вкладке **Распределения организации**. 
- Для второго проверяющего назовите место возникновения затрат, а затем выберите финансовую аналитику **Место возникновения затрат** на вкладке **Распределения организации**.

При настройке workflow-процесса создаются два шага утверждения. Первый — для подразделения, а второй — для места возникновения затрат. Для каждого элемента утверждения вы выбираете **Участник** в поле **Тип назначения** на вкладке **На основе роли**, выберите **Участники расходов** в поле **Тип участника**, а затем выберите соответствующего участника в поле **Участник**.

Когда создается заявка на закупку, финансовые аналитики подразделения и центра затрат назначаются строкам заявки на закупку. При отправке рабочего процесса система сначала оценивает подразделение по заявке на покупку и назначает элемент утверждения пользователю, связанному с работником, выбранным для подразделения. После завершения первого этапа утверждения система оценивает второй этап утверждения и назначает второй элемент утверждения пользователю, связанному с работником, выбранным для места возникновения затрат.

## <a name="example-2-expenditure-reviewers-based-on-project-distributions"></a>Пример 2. Проверяющие расходов на основе распределений проекта

Вы работаете на отдел сервиса Contoso Appliances. Для организации требуется, чтобы менеджер проекта для каждого заказа на покупку обязательно утвердил расходы. Кроме того, менеджер места возникновения затрат для проекта должен утвердить их. Утверждения могут выполняться одновременно. В любом случае оба пользователя должны утвердить заказ на покупку до того, как workflow-процесс сможет продолжить работу.

В этом примере создается один *рецензент расходов по заказу на покупку*, который называется **PM и место возникновения затрат**. Установите флажок **Менеджер проекта** и задайте для параметра **Аналитика места возникновения затрат** значение **Да** на вкладке **Распределения проектов** на странице **Рецензент расходов по заказу на покупку**. В качестве части конфигурации необходимо убедиться, что поле **Менеджер проекта** настроено для всех проектов, а владелец указан для всех мест возникновения затрат на странице **Значения финансовой аналитики**.

При настройке workflow-процесса необходим один элемент утверждения. Вы выбираете **Участник** в поле **Тип назначения**. Затем на вкладке **На основе ролей** в поле **Тип участника** выбираете **Участники расхода**, а в поле **Участник** выбираете менеджера проекта и место возникновения затрат. Чтобы рабочий процесс не продолжался, пока менеджер проекта и владелец центра затрат не утвердит рабочий процесс, установите для поля **Политика завершения** значение **Все утверждающие**.

При создании заказа на покупку поле **Проект** должно быть определено. Если проект не требуется для всех заказов на покупку, следует добавить в бизнес-правило условное решение для проверки проекта до выполнения шага утверждения. Затем система оценивает проект, указанный для заказа на покупку, и назначает элемент утверждения пользователю, связанному с сотрудником, в поле **Менеджер проекта**. Кроме того, система создает задачу и назначает ее пользователю, связанному с сотрудником, выбранным в поле **Владелец** для места возникновения затрат из проекта. Обратите внимание, что в этом примере используется место возникновения затрат проекта, а не место возникновения затрат по заказу на покупку.

## <a name="set-up-expenditure-reviewers"></a>Настройка рецензентов расходов

В данном примере показана настройка рецензента расходов по заявкам на закупку. Чтобы настроить другие типы рецензентов расходов, замените путь перехода на этапе 1 на соответствующий путь из таблицы в разделе [Типы рецензентов расходов](configure-expenditure-reviewers.md#types-of-expenditure-reviewers) ранее в этой теме.

1. Перейдите **Закупки и источники \> Настройка \> Политики \> Рецензенты расходов заявки на покупку**.
2. На странице **Рецензенты расходов по заявкам на покупку** выберите **Создать**.
3. В поле **Имя** введите имя конфигурации рецензента расходов, например **место возникновения затрат**.
4. На экспресс-вкладке **Рецензенты расходов по юридическому лицу** выберите юридическое лицо для настройки.
5. Для распределения проекта установите флажок для каждого органа проекта и выберите **Да** для каждой финансовой аналитики, которую необходимо включить. 
6. Для распределения организации на вкладке **Распределения организации** выберите **Да** для каждой финансовой аналитики, которую необходимо включить.
7. Повторите шаги с 4 по 6 для каждого дополнительного юридического лица.

## <a name="assign-owners-to-financial-dimensions"></a>Назначение владельцев финансовым аналитикам

Чтобы назначить владельца финансовой аналитике, выполните следующие действия.

1. Перейдите в раздел **Главная книга \> План счетов \> Аналитики \> Финансовые аналитики**.
2. В списке выберите финансовую аналитику, которой необходимо назначить владельцев.
3. Выбрать **Значения аналитики**.
4. Выберите **Правка**, чтобы внести изменения в значения аналитики.
5. В списке выберите значение аналитики, которой необходимо назначить владельца.
6. В поле **Владелец** выберите работника, которому необходимо назначить аналитику.

## <a name="configure-project-distributions"></a>Настройка распределений проектов

Для назначения органов проекта проекту, выполните следующие действия.

1. Перейдите в раздел **Управление и учет по проектам \> Проекты \> Все проекты**.
2. Выберите проект, которому требуется назначить органы.
3. Выберите **Правка**, чтобы внести изменения в проект.
4. На экспресс-вкладке **Общее** в разделе **Ответственный** выберите работника в полях **Менеджер по продажам**, **Менеджер проекта** и **Контролер проекта**, как требуется.
5. На экспресс-вкладке **Финансовые аналитики** выберите для своего проекта необходимые финансовые аналитики.

## <a name="assign-expenditure-reviewers-to-a-workflow-task"></a>Назначение рецензентов расходов для задачи workflow-процесса

В этом примере показано, как настроить workflow-процесс заявок на покупку таким образом, чтобы он использовал рецензента расходов по заявкам на покупку. Для настройки других типов workflow-процессов страница workflow-процесса, которую необходимо открыть на шаге 1, может находиться в модуле **Управление расходами** или **Расчеты с поставщиками** вместо модуля **Закупки и источники**.

Чтобы назначить рецензентов расходов для заявки на покупку задаче workflow-процесса, выполните следующие действия.

1. Выберите **Закупки и источники \> Настройка \> Workflow-процессы модуля "Закупки и источники"**.
2. Дважды коснитесь (или двойной щелчок) существующего workflow-процесса или создайте новый workflow-процесс.
3. В редакторе workflow-процессов на панели **Workflow-процесс** выберите задачу, которой требуется назначить конфигурацию рецензента расходов. Затем на **панели операций** в группе **Показать** нажмите **Свойства**.
4. В левой области страницы **Свойства** выберите **Назначение**.
5. На вкладке **Тип назначения** выберите **Участник**.
6. На вкладке **На основе ролей** в поле **Тип участника** выберите **Участники расходов**. Затем в поле **Участник** выберите конфигурацию рецензента расходов, которую необходимо использовать для задачи workflow-процесса.