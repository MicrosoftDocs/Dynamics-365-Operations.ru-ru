---
title: "Действия персонала [часто задаваемые вопросы]"
description: "В этом разделе содержатся ответы на вопросы, которые могут возникнуть, если в организации используются действия персонала. Действия персонала представляют собой дополнительные действия, которые необходимо выполнить при выполнении некоторых задач, связанных с персоналом."
author: shielas
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 4c17441b70a75f032c900c9360da6c0730cf89ba
ms.contentlocale: ru-ru
ms.lasthandoff: 06/13/2017


---

# <a name="personnel-actions-faq"></a>Действия персонала [часто задаваемые вопросы]
В этом разделе содержатся ответы на вопросы, которые могут возникнуть, если в организации используются действия персонала. Действия персонала представляют собой дополнительные действия, которые необходимо выполнить при выполнении некоторых задач, связанных с персоналом. К примерам задач, для которых могут потребоваться действий персонала, относится создание новых должностей, изменение значений имеющихся должностей, прием на работу новых работников, перевод работников, изменение компенсации работников, изменение назначений должности или увольнение работников.

**Примечание.** Действия персонала доступны, только если выбран конфигурационный ключ "Действия персонала". 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>Как определить, включены ли в организации действия персонала?
Действия персонала включены в организации, если выводится запрос на выбор действия персонала при создании новых должностей, изменении существующих должностей, приеме на работу новых работников, переводе работников, изменении компенсации работников, изменении назначений должностей, увольнении сотрудников или вводе сведений по отпускам работников. 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>Что разница между действием должности и действием работника?
Существует два типа действий персонала:

- Действие должности — действие должности выполняется для существующих или новых должностей. Например, действие должности может потребоваться при изменении значения существующей должности или при создании новой сезонной должности. Подробные сведения об использовании действий должностей см. в разделах "Основные задачи: Существующие должности работника" или "Основные задачи: Новые должности работника".

- Действие работника — действие работника выполняется для существующих или новых сотрудников. Например, действие работника может потребоваться при найме на работу нового сотрудника или повышении существующего сотрудника. Подробные сведения об использовании действий работника см. в разделе "Назначение действий персонала работникам".

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>Что означают статусы действий персонала?
У действий персонала могут быть следующие статусы:

- **Черновик** — если используется workflow-процесс, действие не отправлено. Если workflow-процесс не используется, действие не заполнено.
- **На рассмотрении** — действие персонала отправлено в workflow-процесс, но workflow-процесс не завершен.
- **Утвержденное ожидание** — workflow-процесс завершен, но все изменения еще обрабатываются. Отменено — workflow-процесс отменен или действие персонала отозвано. Отклонено — запрос действия отклонен утверждающим лицом.
- **Обработка действия** — запрос действия утвержден, и изменения обрабатываются.
- **Workflow-процесс завершен** — workflow-процесс завершен, и изменения обработаны. Сбой — workflow-процесс завершился с ошибкой, поскольку использовалась устаревшая информация. Щелкните "Повторно активировать", чтобы отобразить последние сведения и продолжить.
- **Завершено** — должность была успешно создана или изменена, сотрудник был успешно нанят на работу, переведен или уволен, либо была изменена компенсация сотрудника. Ошибка — возникла проблема, не связанная с устаревшей информацией. Откройте журнал сообщений действий персонала, чтобы определить причину ошибки.
- **Отклонено** — запрос действия отклонен утверждающим лицом.

## <a name="can-i-delete-a-personnel-action"></a>Можно ли удалить действие персонала?
Да, можно удалить действия персонала, имеющие статус **Черновик**, **Ошибка**, **Сбой** или **Отменено**.

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>Как быстрее всего проверить статус запроса действия персонала?
Откройте любую страницу списка действий персонала и выберите действие персонала.

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>Что делать, если запрос действия персонала завершился с ошибкой?
Если запрос действия персонала завершился с ошибкой, выполните следующие действия, чтобы устранить ошибку и повторно отправить запрос.

> 1. В разделе **Область действий** нажмите кнопку **Текст ошибки**, чтобы просмотреть текст сообщения с описанием проблемы.

> 2. В разделе **Область действий** щелкните **Повторно активировать**, чтобы загрузить последнюю информацию и изменить статус действия персонала на **Черновик**.

> 3. Устраните ошибку и щелкните **Завершить** или **Отправить**.

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>Что происходит с действием персонала, использующим workflow-процесс по завершении процедуры окончательного утверждения?
Если нет ошибок, действие персонала становится доступным только для чтения. (Можно просмотреть историю на странице списка **Все действия работника**, но нельзя изменить действие персонала.) Если действие персонала имеет статус **Завершено**, запись должности или работника уже обновлена. Чтобы просмотреть внесенные изменения, откройте страницу списка **Должности** или **Работники**.

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>Почему выдается следующее сообщение об ошибке при вводе ненулевого значения в поле "Ставка оплаты"? "Значение выходит за границы допустимого для него диапазона, оно должно быть между 0,00 и 0,00"
Это сообщение отображается, поскольку в поле "Уровень" формы "Задание" не задано значение для задания, связанного с выбранной должностью.

Для устранения этой ошибки выполните следующие действия.

> 1. В поле "Назначения должности работника" щелкните поле "Должность".  
> 2. Щелкните значение поля "Задание", чтобы открыть страницу "Задание".
> 3. В области действий щелкните "Правка".
> 4. Нажмите вкладку "Компенсация".
> 5. В поле "Уровень" введите уровень.
> 6. Закройте страницу "Задание".
> 7. Закройте страницу "Должность".
> 8. Вернитесь на вкладку "Компенсация" на странице "Работник", выберите "Постоянное вознаграждение".  Выберите "Создать", введите должность сотрудника в поле "Должность".  Введите значение в поле "План" и затем введите компенсацию сотрудника в поле "Ставка оплаты".

## <a name="why-cant-i-change-the-effective-date-in-the-header-of-the-worker-action-form"></a>Почему я не могу изменить дату вступления в силу в заголовке формы действия работника?
Дату вступления в силу невозможно изменить, поскольку в поле вводится самая логическая дата для данного типа действия.

Рассмотрим пример.

- Дата в заголовке для вступления в силу действия **Увольнение работника** является датой, введенной в поле **Дата увольнения** для работника.
- Дата в заголовке для вступления в силу действия **Прием на работу работника** является датой, введенной в поле **Дата приема сотрудника на работу** для работника.
- Дата в заголовке для вступления в силу действия **Перенести работника** является датой, введенной в поле **Назначить дату начала** для работника.

