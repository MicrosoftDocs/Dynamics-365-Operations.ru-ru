---
title: Контрольные списки обслуживания
description: В этой статье описываются контрольные списки обслуживания в управлении активами.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderChecklist, EntAssetMobileWorkOrderLineChecklistDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 70b83de50105cf664bbc6b6095203d01d83cd79b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016691"
---
# <a name="maintenance-checklists"></a>Контрольные списки обслуживания

[!include [banner](../../includes/banner.md)]



Контрольные списки обслуживания настраиваются для типов заданий обслуживания. Заполните контрольные списки обслуживания как часть процесса выполнения заказа на работу. Для получения дополнительных сведений о настройке контрольных списков обслуживания для типов заданий обслуживания на странице **Значения по умолчанию для типа заданий обслуживания** см. раздел [Категории типов заданий обслуживания и типы заданий обслуживания, варианты типов заданий обслуживания, торговля заданий обслуживания, контрольные списки обслуживания](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

При работе с контрольными списками обслуживания в заказе на работу можно заполнить предопределенные контрольные списки обслуживания, которые связаны с типами заданий обслуживания. Также можно добавить дополнительные контрольные списки обслуживания.


## <a name="fill-in-a-maintenance-checklist"></a>Заполните контрольный список обслуживания

1. Щелкните **Управление активами** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.

2. Выберите заказ на работу, а затем в области действий на вкладке **Заказ на работу** в группе **строки** выберите **контрольный список обслуживания**.

3. **Контрольный список задания обслуживания для заказа на работу** отображает контрольные списки обслуживания для всех заданий заказов на работу. Если задания заказа на обслуживание имеют различные типы заданий обслуживания, контрольные списки обслуживания могут различаться для каждого задания заказа на работу. Выберите задание заказа на работу для работы с соответствующим контрольным списком обслуживания. Сведения о выбранной строке контрольного списка обслуживания показаны на экспресс-вкладке **Сведения по строке**.

4. Заполните все строки контрольного списка обслуживания, по одной за раз, в порядке, в котором они отображаются. Чтобы выполнить строку контрольного списка обслуживания, необходимо заполнить поля на экспресс-вкладке **Сведения по строке**. Сведения, необходимые для заполнения строки, могут различаться в зависимости от типа строки. Например, в строке типа **Текст** добавляется примечание, объясняющее, что было результатом вашей проверки. В строке с типом **Измерение** вводится значение счетчика, считанное с оборудования, и также, если это необходимо, можно добавить примечание. Строка контрольного списка обслуживания типа **Заголовок** используется в качестве заголовка для группировки строк контрольного списка обслуживания, которые появляются ниже. Нет необходимости заполнять заголовок. Что касается всех других типов строк контрольного списка обслуживания, можно добавить примечание к строке типа **заголовка**.

5. Если инструкции связаны с строкой контрольного списка обслуживания, установлен флажок **Инструкции**. Прочитайте инструкции для выбранной строки контрольного списка обслуживания в поле **Инструкции** на экспресс-вкладке **Сведения по строке**.

6. После выполнения строки контрольного списка обслуживания установите флажок **Проверено** в строке, чтобы пометить ее как завершенную. Чтобы отменить строку контрольного списка обслуживания, поскольку она не имеет отношения к заданию заказа на работу, установите флажок **Н/Д** для данной строки. Если в строке контрольного списка обслуживания установлен флажок **Обязательный**, необходимо установить флажок **Отмечено** или **Н/Д**.

>[!NOTE]
>Регистрации контрольного списка обслуживания можно обновлять только в том случае, если этот заказ на работу находится в состоянии жизненного цикла [Активен](../setup-for-work-orders/work-order-lifecycle-states.md).  


## <a name="add-a-maintenance-checklist-line"></a>Добавление строки контрольного списка обслуживания

Контрольные списки обслуживания создаются из определения значений по умолчанию для типа задания обслуживания и переносятся в задание заказа на работу. Если необходимо, можно добавить строки контрольного списка обслуживания в задание заказа на работу. Строки контрольного списка обслуживания, добавленные вручную, получают ссылку **Вручную**.

1. На странице **Контрольный список задания обслуживания для заказа на работу** выберите задание заказа на работу, для которого требуется добавить контрольный список обслуживания.

2. На экспресс-вкладке **Строки контрольного списка обслуживания** выберите строку контрольного списка обслуживания. Затем, чтобы вставить новую строку после выделенной строки, нажмите клавишу **СТРЕЛКА ВНИЗ**. Следующий номер в последовательности автоматически вводится в поле **Номер строки**. Чтобы вставить новую строку перед выбранной строкой, выберите **добавить строку**. 

3. Введите имя для строки контрольного списка обслуживания в поле **Имя**.

4. В поле **Тип** выберите тип для строки контрольного списка обслуживания. Для каждого типа контрольного списка обслуживания на экспресс-вкладке **Сведения по строке** содержатся соответствующие поля.
    - **Текст** — этот тип используется для добавления строки контрольного списка обслуживания, которая содержит текст с описанием того, что должно быть сделано. Например, можно использовать этот тип контрольного списка обслуживания, если требуется, чтобы работник выполнил проверку или осмотрел что-то, но не предполагается конкретный (измеримый) результат. После выбора этого типа на экспресс-вкладке **сведения по строке** в поле **инструкции** введите текст, описывающий, что должно быть сделано.
    - **Заголовок** — строка контрольного списка обслуживания этого типа используется в качестве заголовка для группировки строк контрольного списка обслуживания, которые появляются ниже. Этот тип полезен, если имеется несколько строк контрольного списка обслуживания, которые могут быть разделены на определенные области. После выбора данного типа введите описательное имя в поле **Имя**.
    - **Шаблон** — этот тип не применяется при добавлении строки контрольного списка обслуживания вручную в задание заказа на работу.  
    - **Переменная** — этот тип используется для определения возможного результата в диапазоне для строки контрольного списка обслуживания. Дополнительные сведения о настройке переменных контрольного списка обслуживания см. в разделе [Категории типов заданий обслуживания и типы заданий обслуживания, варианты типов заданий обслуживания, торговля заданий обслуживания, контрольные списки обслуживания](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). После выбора данного типа введите описательное имя для переменной в поле **Имя**. На экспресс-вкладке **сведения по строке** в поле **переменная** выберите переменную. В поле **Инструкции** введите текст, описывающий то, что должно быть сделано.
    - **Измерение** — этот тип используется для записи определенного измерения в строке контрольного списка обслуживания. После выбора данного типа введите имя для измерения в поле **Имя**. На экспресс-вкладке **сведения по строке** в полях **Счетчик** и **Единица измерения**, выберите соответствующие значения. В поле **Инструкции** введите текст, описывающий то, что должно быть сделано.

5. После завершения добавления вручную строк контрольных списков обслуживания заполните строки, как описано в разделе **заполнение контрольных списков обслуживания** выше.

>[!NOTE]
>На странице **Контрольный список задания обслуживания для заказа на работу** нельзя удалить строки контрольного списка обслуживания со ссылкой **Тип задания**. Удалить можно только строки контрольного списка обслуживания, которые вы или другие специалисты по обслуживанию создали вручную, и которые имеют ссылку **Вручную**.

Иллюстрация ниже показывает пример контрольного списка обслуживания.

![Рисунок 1.](media/14-work-orders.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]