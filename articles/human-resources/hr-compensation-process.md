---
title: Обработка компенсаций
description: Обработка компенсаций позволяет рассчитывать новые суммы базовой компенсации для сотрудников на основе корректировки размеров зарплат, целевых значений надбавок за успешную работу, а также эффективности работы сотрудников.
author: andreabichsel
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 05f7be778857380d40a73d068e2b0b4fc7d1d1f6
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010337"
---
# <a name="process-compensation"></a>Обработка компенсаций

Обработка компенсаций позволяет рассчитывать новые суммы базовой компенсации для сотрудников на основе корректировки размеров зарплат, целевых значений надбавок за успешную работу, а также эффективности работы сотрудников. В этой статье рассматривается базовая процедура обработки компенсаций для планов фиксированной компенсации без учета эффективности работы сотрудников.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Планирование новых сумм и бюджетов компенсации
Чтобы дать своим сотрудникам надбавку за хорошую работу, вы должны настроить бюджет фиксированного увеличения для каждого из ваших подразделений: "Управление компенсациями" > "Ссылки" > "Целевые значения увеличения надбавки за успешную работу". (Кроме того, можно открыть эту форму через подразделение: "Организация" > "Подразделения".) Здесь также можно дополнительно указать, должны ли сотрудники, относящиеся к тому или иному профсоюзу или местонахождению, получить другой процент увеличения. Поля **Бюджет** и **Валюта** являются информационными и могут использоваться для записи суммы в валюте для бюджета.

## <a name="set-up-the-compensation-process"></a>Настройка процесса обработки компенсаций
Событие процесса позволяет указать параметры для обработки компенсации. Сюда входит период дат, который должен оцениваться для определения сумм компенсаций, а также дата, когда новые суммы компенсаций должны вступить в силу.

При необходимости можно включить дату приема на работу с пропорциональным распределением фиксированной оплаты, если в каком-либо из ваших планов фиксированной компенсации используется правило приема на работу "Процент". В таких планах сотрудники, принятые на работу после даты начала цикла и до даты приема на работу с пропорциональным распределением фиксированной оплаты, получат 100% своей рассчитанной надбавки или общего увеличения. Сотрудники, принятые на работу после даты приема на работу с пропорциональным распределением фиксированной оплаты и до даты окончания цикла, получат часть своего рассчитанного увеличения в зависимости от того, в течение скольких дней из общего количества дней цикла они были трудоустроены. Например, если цикл начинается с 1 января и заканчивается 31 декабря, а дата приема на работу с пропорциональным распределением фиксированной оплаты — 1 апреля, сотрудник, нанятый в марте, получит рассчитанное увеличение полностью, тогда как сотрудник, нанятый 1 июля, получит примерно половину рассчитанного увеличения.

Событие процесса **Дата момента времени** используется только для обработки определенных планов переменной компенсации, и не рассматривается здесь. **Крайний срок проверки** — это крайний срок для вынесения всех рекомендаций, чтобы новые суммы компенсаций можно было загрузить в запись сотрудника. Дата проверки носит исключительно информационный характер.

После сохранения параметров события процесса можно нажать кнопку **Настройка**, чтобы указать планы, которые требуется включить в этот запуск обработки, и какие действия фиксированной компенсации необходимо предпринять для каждого плана.

Нажмите кнопку **Добавить** на вкладке **Планы**, чтобы добавить план компенсации в событие процесса. Столбцы **Использовать другой коэффициент**, **Коэффициент увеличения прибыли** и **Описание коэффициента** используются только для планов переменной компенсации, и в этой статье рассматриваться не будут.

Сохраните запись, а затем нажмите кнопку **Добавить** на вкладке **Действия**, чтобы добавить действия фиксированной компенсации для выбранного плана. Используйте параметр **Включить рекомендации** , если вы хотите иметь возможность ввести сумму, отличную от рассчитанного предписываемого увеличения для действия. Чтобы рассчитать действие, основанное на результате предыдущего действия, для связи нескольких действий компенсации, установите флажок **Использовать предыдущий результат**. Действия фиксированной компенсации — это типы логики компенсации, которым можно давать описательные имена. Для ступенчатых и ленточных планов можно добавить только действия фиксированной компенсации следующих типов:

| Тип действия по постоянной компенсации | Функциональность                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Собственный капитал                        | Действия по основной части зарплаты сравнивают ставку оплаты сотрудника на дату окончания цикла с самой нижней опорной точкой для уровня, указанного в должности сотрудника. Если ставка оплаты сотрудника ниже минимальной опорной точки, рассчитывается увеличение, необходимое для поднятия оплаты сотрудника до минимальной точки в диапазоне.                                                                                |
| Заслуга                         | Действия по надбавкам за успешную работу будут рассчитывать увеличение на основании ставки оплаты сотрудника на дату окончания цикла и процента увеличения, указанного в бюджете фиксированного увеличения для подразделения, профсоюза и местонахождения сотрудника.                                                                                                                                                                                         |
| Общие                       | Общие действия будут рассчитывать увеличение либо на основании процента, либо исходя из предоставления сотрудникам фиксированной суммы. Это определяется на основании параметров **Фиксированная компенсация** на вкладке **Общие**.                                                                                                                                                                                                                        |
| Развитие                     | Действия по повышению дают возможность получить именованное место, где можно назначить увеличение, поэтому обязательно установите флажок **Включить рекомендации**, чтобы вы могли ввести рекомендацию для сотрудников, которые получат повышение.  У сотрудников без рекомендованного увеличения действие **Продвижение** не будет добавлено в записи фиксированной компенсации.                                                                       |
| Изменение другого уровня            | В предыдущем примере **Понижение** — название действия **Фиксированная компенсация** с типом **Изменение другого уровня**. Это приводит к нулевому предписываемому увеличению, чтобы вы могли ввести сумму рекомендации для корректировки ставки оплаты сотрудника. (Не забудьте установить флажок **Включить рекомендации**.) У сотрудников без рекомендации это действие добавлено в записи фиксированной компенсации не будет. |

Добавить действия **Фиксированная компенсация** типа "Шаг" можно только в пошаговый план.

| Тип действия фиксированной компенсации | Функциональность                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Шаг                           | На вкладке "Общие" укажите, на сколько шагов это действие шага должно перемещать сотрудников вперед: на 0 шагов, на 1 шаг или на 2 шага.                                                                                  |
|                                | **0 шагов** — сотрудники получат ставку оплаты для текущего шага, на котором они находятся.                                                                                                                      |
|                                | **1 шаг** — система проверит, находится ли сотрудник уже на последней опорной точке для своего порога.                                                                                             |
|                                | **2 шага** — система переместит сотрудника на два шага вперед на его текущем уровне. Если сотрудник достиг последней опорной точки на своем уровне, система сможет переместить его только на один или ноль шагов. |

## <a name="run-the-compensation-process"></a>Запуск процесса компенсации
После настройки события процесса путем заполнения необходимых полей дат и задания планов и действий вы можете щелкнуть **Запустить процесс** на странице **Событие процесса**. При этом откроется диалоговое окно **Запустить процесс компенсации**. В этом диалоговом окне можно щелкнуть **Показать результаты обработки**, чтобы увидеть рассчитанные суммы компенсации для каждого сотрудника. При нажатии кнопки **ОК** процесс обработки компенсации будет запущен для всех сотрудников, находящихся в выбранных планах компенсации на дату окончания цикла.

## <a name="view-the-process-results"></a>Просмотр результатов обработки
Чтобы просмотреть результаты процесса, откройте страницу **Результаты обработки**. При каждом запуске события процесса создается новое событие компенсации. Так можно выполнять пробные запуски, вносить корректировки и запускать событие компенсации несколько раз, чтобы увидеть, как различные изменения влияют на компенсацию сотрудников.

На странице **Результаты обработки** содержится информация о запуске процесса, включая время запуска, пользователя, запустившего процесс, а также возникли ли в ходе выполнения процесса какие-либо ошибки. Можно также установить флажок **Блокировано**, чтобы сделать неактивной кнопку **Загрузить компенсацию**; в этом случае никто не сможет загрузить события компенсации в записи сотрудников. При нажатии кнопки **Результаты сотрудников** отобразится список сотрудников, включенных в этот запуск.

В параметре **Результаты сотрудника** отображается информация о самом процессе, а также действия компенсации, выполненные в процессе. В разделе **Фиксированная компенсация** содержится по записи для каждого действия, включенного в событие процесса для плана компенсации. В столбцах **Текущее предписание** и **Рекомендация** отображается дополнительная информация по действию, выбранному в разделе **Фиксированная компенсация**. Если для действия установлен флажок **Включить рекомендации**, поля "Рекомендация" будут доступны для редактирования. Это позволит вручную корректировать суммы для сотрудника. Примечание. Если в событии процесса вы отметили для действия флажок **Использовать предыдущий результат**, вы должны вручную обновить суммы для всех зависимых действий.

После проверки сумм компенсации для сотрудника и внесения необходимых корректировок в рекомендуемые значения, можно изменить **Статус** в строке **Событие сотрудника**, чтобы указать, было событие утверждено или его следует игнорировать. При необходимости можно стереть все изменения, внесенные в рекомендацию по сотруднику, нажатием кнопки **Пересчитать**. При этому существующему событию сотрудника будет присвоен статус "Игнорировать", и будет создано новое событие сотрудника с пересчитанными значениями.

## <a name="loading-approved-compensation-changes"></a>Загрузка утвержденных изменений компенсации
После того как статус одного или нескольких событий сотрудников будет изменен на "Утверждено", их можно загрузить в записи фиксированной компенсации сотрудников. Это можно сделать либо путем поочередного выбора каждого события сотрудника и нажатия кнопки **Загрузить компенсацию для сотрудника** на странице **Результаты сотрудников**, либо путем нажатия кнопки **Загрузить компенсацию** на странице **Результаты обработки** для одновременной загрузки всех событий сотрудников.

После нажатия кнопки **ОК** в диалоговом окне **Загрузить компенсацию** ненулевые строки действий компенсации будут добавлены на страницу **Постоянное вознаграждение работнику**.