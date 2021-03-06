---
title: Возможности сетки
description: В этом разделе описываются несколько функциональных возможностей элемента управления "сетка". Необходимо включить новую функцию сетки для доступа к этим возможностям.
author: jasongre
ms.date: 01/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b7a1809a3012af86ad9ba39da8721c63b3c4b885
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923606"
---
# <a name="grid-capabilities"></a>Возможности сетки

[!include [banner](../includes/banner.md)]


Новый элемент управления "сетка" предоставляет несколько полезных и мощных возможностей, которые могут использоваться для улучшения производительности пользователя, создания более интересных представлений данных и получения осмысленных аналитических данных. В этой статье рассматриваются следующие возможности: 

-  Рассчитываемые итоги
-  Опережающий ввод системы
-  Оценка математических выражений 
-  Группировка табличных данных (включается отдельно с помощью функции **(Предварительная версия) Группировка в сетках**)
-  Закрепление столбцов

## <a name="calculating-totals"></a>Рассчитываемые итоги
В приложениях Finance and Operations пользователи имеют возможность просматривать итоговые значения в нижней части числовых столбцов в сетках. В разделе нижнего колонтитула в нижней части сетки отображаются эти итоги. 

### <a name="showing-the-grid-footer"></a>Отображение нижнего колонтитула сетки
В нижней части каждой табличной сетки в приложениях Finance and Operations имеется область нижнего колонтитула. В нижнем колонтитуле могут отображаться полезные сведения, имеющие отношение к данным, отображаемым в сетке. Ниже приведены несколько примеров таких сведений:

- Число выбранных строк в таблице (когда вы выбрали более одной записи)
- Общие итоги внизу настроенных числовых столбцов
- Количество строк в наборе данных 

Этот нижний колонтитул по умолчанию скрыт, но вы можете включить его. Чтобы показать нижний колонтитул для сетки, щелкните правой кнопкой мыши заголовок столбца в сетке и выберите пункт **Показать нижний колонтитул**. После включения нижнего колонтитула для определенной сетки этот параметр будет сохранен до тех пор, пока пользователь не решит скрыть нижний колонтитул. Чтобы скрыть нижний колонтитул, щелкните правой кнопкой мыши заголовок столбца и выберите **Скрыть нижний колонтитул**.  (Расположение действия **Показать/скрыть нижний колонтитул** может измениться в будущем обновлении. 

### <a name="specifying-columns-with-totals"></a>Указание столбцов с итогами
В настоящее время ни в каких столбцах не отображаются итоговые значения по умолчанию. Вместо этого это считается однократным действием настройки, аналогичным настройке ширины столбцов в сетках. После того как вы укажете, что хотите просмотреть итоговые значения для столбца, этот параметр будет сохранен при следующем посещении страницы.  

Имеется два способа настройки столбца для отображения итогового значения: 

- Щелкните правой кнопкой мыши столбец для просмотра итогов и затем выберите **Итоговое значение этого столбца**. Это действие приводит к возникновению трех событий:

    1. Нижний колонтитул становится видимым. 
    2. Ваше предпочтение просмотреть итоги по этому столбцу сохранено. 
    3. Вычисление итогов инициируется для этого столбца и всех остальных, для которых вы ранее настроили просмотр итогов. Время, необходимое для отображения итога, зависит от размера набора данных, для которого выполняется подведение итога.

- После отображения нижнего колонтитула выберите **Показать итог** в области нижнего колонтитула в нижней части столбца, для которого нужно просмотреть итог. Если настроенные столбцы отсутствуют, кнопка **Показать итог** будет доступна для всех числовых столбцов. 

    Как только хотя бы один столбец настроен для итогов, кнопки **Показать итоги** будут доступны только при наведении курсора или при фокусе. При выборе команды **Показать итог** просто сохраняется предпочтение для просмотра итогов в этом столбце, так что во время последующих посещениях страницы этот параметр будет применен. В нижнем колонтитуле это состояние обозначается тире, которое отображается в столбце. (В качестве альтернативы, если набор данных достаточно мал, сразу отображается итог.)

Если вы сделали ошибку и больше не нужно просматривать итог в определенном столбце, щелкните правой кнопкой мыши столбец и выберите **Скрыть итог** или выберите кнопку **Скрыть итог** в нижнем колонтитуле этого столбца. Этот параметр также будет сохранен для последующих посещений страницы. 

### <a name="calculating-totals"></a>Рассчитываемые итоги
При переходе к странице с видимым нижним колонтитулом и столбцами с настроенным итогом, итоговые значения в нижнем колонтитуле могут быть отображены или могут отсутствовать. Поведение зависит от размера набора данных на странице. Если набор данных достаточно мал, итоговые значения будут отображаться автоматически вместе с количеством строк в наборе данных. Если в нижнем колонтитуле в столбцах, настроенных для итогов, имеются тире, то набор данных слишком велик для того, чтобы система отображала итоговые значения немедленно, а для расчета итоговых сумм требуется явное действие. Для этого нажмите кнопку **Рассчитать** в нижнем колонтитуле или щелкните правой кнопкой мыши столбец, для которого нужно получить итог, и выберите **Итоговое значение этого столбца**.  

Если вычисление занимает слишком много времени, можно отменить операцию, нажав кнопку **Отмена**. Однако иногда набор данных будет слишком большим для расчета итоговых сумм (пределы, накладываемые вашей организацией), и вы будете извещены о необходимости фильтрации данных.

Итоги будут обновляться автоматически при обновлении, удалении или создании строк в наборе данных.  

## <a name="typing-ahead-of-the-system"></a>Опережающий ввод системы
Во многих бизнес-сценариях возможность быстрого ввода данных в систему очень важна. Перед тем как новый элемент управления сетки был введен, пользователи могли изменить данные только в текущей строке. Перед тем как они смогут создать новую строку или перейти в другую строку, они вынуждены ожидать, пока система не сможет успешно выполнить проверку всех изменений. При попытке уменьшить количество времени, в течение которого пользователи ожидают завершения этих проверок, и повышения производительности пользователей новая сетка корректирует эти проверки так, чтобы они были асинхронными. Таким образом, пользователь может перейти к другим строкам, чтобы внести изменения, пока ожидаются предыдущие проверки строк. 

Для поддержки этого нового поведения новый столбец для статуса строки был добавлен в правую часть столбца выбора строки, когда сетка находится в режиме редактирования. Этот столбец указывает один из следующих статусов:

- **Пусто** — изображение без статуса указывает, что строка успешно сохранена системой.
- **Ожидание обработки** — этот статус указывает, что изменения в строке еще не были сохранены сервером, но находятся в очереди изменений, которые должны быть обработаны. Перед выполнением действия вне сетки необходимо дождаться, чтобы все ожидающие изменения были обработаны. Кроме того, текст в этих строках отображается курсивом, чтобы обозначить несохраненный статус строк. 
- **Недопустимое состояние** — этот статус означает, что во время обработки строки появилось какое-либо предупреждение или сообщение, которое могло помешать системе сохранить изменения в этой строке. В старой сетке вы принудительно возвращались в строку, если операция сохранения завершалась неудачно. Однако в новой сетке будет выдано сообщение о том, что обнаружена проблема проверки, но вы можете решить, когда следует исправить ошибки в строке. Когда вы готовы устранить проблему, вы можете переместить фокус обратно в эту строку вручную. Кроме того, можно выбрать действие **Исправить проблему**. Это действие сразу же переводит фокус обратно в строку, которая содержит проблему, и позволяет вносить изменения внутри сетки или за ее пределами. Обратите внимание, что обработка последующих ожидающих строк останавливается до тех пор, пока не будет исправлено данное предупреждение проверки. 
- **Приостановлено** — этот статус указывает на то, что обработка сервером приостановлена, так как выполняется проверка строки, которая вызвала всплывающее диалоговое окно, требующее ввода данных пользователем. Так как пользователь может вводить данные в какую-либо другую строку, всплывающее диалоговое окно не становится немедленно видимым для этого пользователя. Вместо этого оно будет представлено, когда пользователь решит возобновить обработку. Этот статус сопровождается уведомлением, которое информирует пользователя о ситуации. Уведомление включает действие **Возобновить обработку**, которое запускает всплывающее диалоговое окно.  
    
Когда пользователи вводят данные перед тем местом, которое обрабатывается сервером, они могут ожидать некоторого ухудшения в опыте ввода данных, такого как отсутствие подстановок, проверка на уровне элементов управления и ввод значений по умолчанию. Пользователям, которым требуется раскрывающийся список для поиска значения, рекомендуется подождать, пока сервер не дойдет до текущей строки. Проверка на уровне элемента управления и ввод значений по умолчанию также будут выполняться, когда сервер обрабатывает эту строку.   

### <a name="pasting-from-excel"></a>Вставка из Excel
Пользователи всегда могли экспортировать данные из сеток в приложениях Finance and Operations в Excel, используя механизм **Экспорт в Excel**. Однако возможность опережающего ввода данных до обработки системой позволяет новой сетке поддерживать копирование таблиц из Excel и их вставку непосредственно в сетки в приложениях Finance and Operations. Ячейка сетки, из которой запускается операция вставки, определяет место, с которого начинается вставка копируемой таблицы. Содержимое сетки перезаписывается содержимым скопированной таблицы, за исключением двух случаев:

- Если число столбцов в копируемой таблице превышает число столбцов, остающихся в сетке, начиная с места вставки, пользователь получает уведомление о том, что лишние столбцы были пропущены. 
- Если количество строк в копируемой таблице превышает число строк в сетке, начиная с места вставки, существующие ячейки перезаписываются вставленным содержимым, а все дополнительные строки скопированной таблицы вставляются в конце сетки как новые строки. 

## <a name="evaluating-math-expressions"></a>Оценка математических выражений
В качестве ускорителя производительности пользователи могут вводить в сетке математические формулы в виде числовых ячеек. Они не должны выполнять расчет в приложении вне системы. Например, если ввести **=15\*4**, а затем нажать клавишу **Tab**, чтобы переместиться из поля, система выполнит оценку выражения и сохранит значение **60** для поля.

Чтобы система распознавала значение как выражение, следует начинать значение со знака равенства (**=**). Дополнительную информацию о поддерживаемых операторах и синтаксисе см. в разделе [Поддерживаемые математические символы](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Группирование табличных данных
Бизнес-пользователям часто приходится выполнять нерегламентированный анализ данных. Хотя это можно сделать, если экспортировать данные в Microsoft Excel и с помощью сводных таблиц, функция **Группировка в сетках**, которая стала общедоступной в версии 10.0.16/обновление платформы 40 и зависит от новой функции элемента управления сетки, позволяет пользователям организовывать свои табличные данные нужным образом в приложениях Finance and Operations. Поскольку эта функция расширяет функцию **Итог**, **Группирование** позволяет получить осмысленные сведения о данных, представляя промежуточные итоги на уровне группы.

Для использования этой функции щелкните правой кнопкой мыши столбец, по которому необходимо выполнить группировку, и выберите **Группировать по этому столбцу**. Это действие сортирует данные по выбранному столбцу, добавит новый столбец **Группировать по** в начало сетки и вставит "строки заголовков" в начало каждой группы. В этих строках заголовка содержится следующая информация о каждой группе: 
-  Значение данных для группы 
-  Имя столбца (эта информация особенно полезна при наличии нескольких уровней группировки)  
-  Число строк данных в этой группе
-  Промежуточные итоги для любого столбца, настроенного для отображения итогов

Когда включено [Сохраненные представления](saved-views.md), это группирование можно сохранить как персонализацию в виде части представления для быстрого доступа при следующем посещении страницы.  

### <a name="multiple-levels-of-grouping"></a>Несколько уровней группировки
После группировки данных по одному столбцу можно группировать данные по другому столбцу, выбрав **Группировать по этому столбцу** в нужном столбце. Этот процесс может повторяться до тех пор, пока не будет достигнуто 5 вложенных уровней группировки, что является максимально допустимой глубиной. На этом этапе будет невозможно сгруппировать по дополнительным столбцам.  

В любой момент можно удалить группировку по любому столбцу, щелкнув правой кнопкой мыши этот столбец и выбрав команду **Разгруппировать**. Можно также удалить группировку из всех столбцов, выбрав **Параметры сетки**, а затем **Разгруппировать все**.   

Примечание. До версии 10.0.16/обновление платформы 40 поддерживается только один уровень группировки. В этих версиях если данные сгруппированы и выбрано значение **Группировать по этому столбцу** для другого столбца, исходная группа будет заменена.  


### <a name="expanding-and-collapsing-groups"></a>Развертывание и свертывание групп
При начальной группировке данных все группы будут развернуты. Можно создать обобщенные представления данных, сворачивая отдельные группы, или можно использовать развертывание и свертывание групп, чтобы облегчить перемещение по данным. Чтобы развернуть или свернуть группу, нажмите кнопку со знаком "Шеврон" (>) в соответствующей строке заголовка группы. Обратите внимание, что состояние развертывания/свертывания отдельных групп **не** сохраняется в персонализации.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Выбор и отмена выбора строк на уровне группы
Тем же способом, каким можно выбрать (или отменить выбор) все строки в сетке, установив флажок в верхней части первого столбца сетки, можно также быстро выбрать (или отменить выбор) все строки в группе, установив флажок в соответствующей строке заголовка группы. Флажок в строке заголовка группы будет всегда отражать текущее состояние выбора строк в этой группе, независимо от того, выбраны ли все строки, не выбраны никакие строки или выбраны только некоторые строки.

### <a name="hiding-column-names"></a>Скрытие имен столбцов
При группировании данных поведением по умолчанию является отображение имени столбца в строке заголовка группы. Начиная с версии 10.0.14/обновления платформы 38 можно отключить вывод имени столбца в строках заголовка группы, выбрав **Параметры сетки** > **Скрыть имя столбца группы**.

## <a name="freezing-columns"></a>Закрепление столбцов
Некоторые столбцы в сетке могут быть достаточно важными для контекста, чтобы вы не хотели, чтобы они скрывались при прокрутке. Вместо этого необходимо, чтобы значения в этих столбцах всегда отображались. В версии 10.0.17 функция **Закрепить столбцы в сетке** обеспечивает гибкие возможности для пользователей. 

Чтобы закрепить столбец, щелкните правой кнопкой мыши заголовок столбца, затем выберите команду **Закрепить столбец**. При первом выполнении этого шага выбранный столбец становится первым столбцом и больше не будет скрываться из виду при прокрутке. Все последующие столбцы, которые закрепляются, будут добавлены справа от последнего закрепленного столбца. Можно использовать стандартные функции перемещения для изменения порядка закрепленных столбцов, как это требуется. Однако закрепленные столбцы нельзя переместить, чтобы они отображались среди незакрепленных столбцов. Аналогично, незакрепленные столбцы нельзя переместить, чтобы они отображались среди закрепленных столбцов.

Чтобы отменить закрепление столбца, щелкните правой кнопкой мыши заголовок закрепленного столбца, затем выберите команду **Отменить закрепление столбца**. 

Обратите внимание, что столбцы выбора строк и статуса строки в новой сетке всегда закреплены как первые два столбца. Таким образом, если эти столбцы включены в сетку, они всегда будут видны пользователям, независимо от позиции прокрутки в сетке по горизонтали. Невозможно изменить порядок этих двух столбцов.

## <a name="frequently-asked-questions"></a>Вопросы и ответы
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Как включить новый элемент управления сетки в моей среде? 

**10.0.9 / Обновление платформы 33 и позднее**

Функция **Создать элемент управления сетки** доступна непосредственно в управлении функциями в любой среде. Как и другие общие функции предварительного просмотра, включение этой функции в производство осуществляется в рамках [Дополнительные условия договора об использовании](public-preview-terms.md).  

**10.0.8/обновление платформы 32 и 10.0.7/обновление платформы 31**

Функция **Создать элемент управления сетки** может быть включена в средах уровня 1 (разработка/тестирование) и 2 (песочница) для обеспечения дополнительной проверки и изменения структуры с помощью описанных ниже шагов.

1.  **Включить рейс**: Выполните следующий оператор SQL: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. **Сброс IIS** для очистки кэша статического фокус-тестирования. 

3.  **Найти функцию**: перейдите к рабочей области **Управление функциями**. Если **Новый элемент управления сетки** не отображается в списке всех функций, выберите **Проверить наличие обновлений**.   

4.  **Включить функцию**: найдите функцию **Новый элемент управления сетки** в списке функций, и выберите **Включить сейчас** в области сведений. Обратите внимание, что необходимо обновление браузера. 

Все последующие сеансы пользователя начнутся с включенным новым элементом управления "Сетка".

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Разработчик] Отдельные страницы отказа от использования новой сетки 
Если в организации обнаруживается страница, в которой есть несколько проблем с использованием новой сетки, начиная с версии 10.0.13/обновление платформы 37 предусмотрен API, позволяющий конкретной форме использовать стандартный элемент управления DataGrid, тем самым разрешая остальным системам использование нового элемента управления "сетка". Чтобы явно отказаться от отдельной страницы в новой сетке, добавьте следующую запись вызова `super()` в метод `run()` для формы.

 ```this.forceLegacyGrid();```

Этот API будет обрабатываться до выпуска в октябре 2021 года, когда новый элемент управления "сетка" станет обязательным. Если какие-либо проблемы требуют использования этого API, сообщите об этом в корпорацию Microsoft.

## <a name="developer-size-to-available-width-columns"></a>[Разработчик] Столбцы "размера по доступной ширине"
Если разработчик задает для свойства **WidthMode** значение **SizeToAvailable** для столбцов в новой сетке, эти столбцы первоначально имеют одинаковую ширину, которую бы они имели, если бы для этого свойства было задано значение **SizeToContent**. Однако они растягиваются, чтобы использовать любую дополнительную доступную ширину в сетке. Если свойство имеет значение **SizeToAvailable** для нескольких столбцов, все эти столбцы совместно используют любую дополнительную доступную ширину в сетке. Однако если пользователь вручную изменяет размеры одного из этих столбцов, столбец становится статическим. Он останется этой ширины и не будет растягиваться, чтобы занять дополнительную доступную ширину сетки.  

## <a name="known-issues"></a>Известные проблемы
В этом разделе ведется список известных проблем для нового элемента управления сетки.  

### <a name="open-issues"></a>Открытые проблемы
-  После включения функции **Новый элемент управления сетки** для некоторых страниц будет использоваться существующий элемент управления "сетка". Это произойдет в следующих ситуациях:  
    -  На странице есть список карточек, отображаемый в нескольких столбцах.
    -  На странице есть сгруппированный список карточек.
    -  Столбец сетки с расширяемым элементом управления без реакции.

    Когда пользователь впервые встречает одну из этих ситуаций, будет выведено сообщение об обновлении страницы. После появления этого сообщения на странице будет по-прежнему использоваться существующая сетка для всех пользователей до тех пор, пока не будет обновлена следующая версия продукта. Более качественное управление этими сценариями, чтобы использовать новую сетку, будет учитываться при будущем обновлении.    
    
-  [KB 4582758] Если изменить масштаб со 100 на любой другой процент, записи будут размыты
-  [KB 4592012] Непредвиденная ошибка клиента в IE11 при вставке нескольких строк из Excel
    -  Корпорация Майкрософт не пытается исправить эту проблему

### <a name="fixed-as-part-of-10016"></a>Исправлено как часть 10.0.16

-  [KB 4598335] Многострочные строковые элементы управления не учитывают свой параметр DisplayHeights в списках/карточках 
-  [KB 4591891] При снятии отметки строк строки предложений по накладной исчезают
-  [KB 4592104] Невозможно изменить записи после нажатия кнопки "Исправить проблему" и перехода в другую строку без исправления ошибки проверки
-  [KB 4594449] В элементе управления "Выбор даты" отсутствуют кнопки "Никогда" и "Сброс" 
-  [KB 4594448] Ввод времени по-разному обрабатывается новой сеткой
-  [KB 4600059] Неожиданная ошибка клиента при регулировке электронной почты
-  [KB 4574584] Предварительный просмотр вложений расходов недоступен при наведении указателя на значок чека

### <a name="fixed-as-part-of-10015"></a>Исправлено как часть 10.0.15    

-  (Обновление качества) [KB 4594444] Неожиданная ошибка клиента с предварительным просмотром для элемента управления сегментированного ввода
-  [KB 4582723] Параметры отображения не отображаются, если заданы позже в жизненном цикле формы
-  [KB 4591988] Проблемы с использованием клавиатуры для выбора значения из подстановки ReferenceGroup
-  [KB 4588958] Проверка Regression Suite Automation Tool (RSAT) завершается с ошибкой: TypeError: не удается прочитать свойство "текст" для неопределенного значения
-  [KB 4591970] Неожиданная ошибка клиента, если вставка из Excel была выполнена сразу после щелчка в сетке
-  [KB 4591904] Изменения данных не сохраняются, если после редактирования элемента управления пользователь сразу щелкнул мышкой и открыл подстановку другого элемента управления
-  [KB 4584752] Неожиданная ошибка клиента со страницей предложения по накладным по проекту
-  [KB 4584540] Не удается покинуть сетку после вставки одной строки в строку журнала
-  [KB 4591908] При создании новой строки фокус остается в столбце, в котором вы находились

### <a name="fixed-as-part-of-10014"></a>Исправлено как часть 10.0.14

-  (Обновление качества) [KB 4584752] Неожиданная ошибка клиента со страницей предложения по накладным по проекту
-  [KB 4583880] Тесты Regression Suite Automation Tool (RSAT) завершаются ошибкой при выполнении действия OpenLookup с сообщением "Не удается прочитать свойство RowIndex неопределенного"
-  [KB 4583847] Неожиданная ошибка клиента при переходе по подстановкам

### <a name="fixed-as-part-of-10013"></a>Исправлено как часть 10.0.13

-  (Обновление качества) [KB 4584752] Неожиданная ошибка клиента со страницей предложения по накладным по проекту
-  (Обновление качества) [KB 4583880] Тесты Regression Suite Automation Tool (RSAT) завершаются ошибкой при выполнении действия OpenLookup с сообщением "Не удается прочитать свойство RowIndex" неопределенного"
-  (Обновление качества) [KB 4583847] Неожиданная ошибка клиента при переходе по подстановкам 
-  (Обновление качества) [Ошибка 471777] Невозможно выбрать поля в сетке для редактирования или создания мобильного приложения
-  [KB 4582727] Сетка зависает после того, как пользователь получает диалог для элементов с несколькими количествами
-  [Ошибка 474851] Гиперссылки в элементах управления группы ссылок не работают 
-  [Ошибка 474848] Расширенный предварительный просмотр с сетками не отображается
-  [KB 4582726] Свойство RotateSign не учитывается  
-  [Ошибка 470173] Флажки в неактивных строках переключаются при нажатии на пробел в ячейке
-  [Ошибка 474848] Расширенный предварительный просмотр с сетками не отображается
-  [Ошибка 474851] Гиперссылки в элементах управления группы ссылок не работают 
-  [Ошибка 471777] Невозможно выбрать поля в сетке для редактирования или создания мобильного приложения
-  [KB 4569441] Вопросы, связанные с отрисовкой списка карточек с несколькими столбцами, всплывающие подсказки для изображений и параметры отображения в некоторых полях
-  [KB 4575279] Не все помеченные строки удаляются в общем журнале
-  [KB 4575233] Параметры дисплея не восстанавливаются после перехода в другую строку
-  [Ошибка 477884] Подстановка возвращает неправильное значение или запись, если активирован новый элемент управления сеткой
-  [KB 4571095] Разноска поступлений продуктов происходит при случайном нажатии клавиши "Ввод" (коррекция обработки действия по умолчанию для страницы)
-  [KB 4575437] Поиск с редактируемыми элементами управления неожиданно закрывается
-  [KB 4569418] Повторяющаяся строка создана в форме расписания поставки
-  [KB 4575435] Расширенный просмотр иногда сохраняется даже в том случае, когда указатель мыши не находится рядом с полем
-  [KB 4575434] Поиск не фильтруется, когда поле было изменено
-  [KB 4575430] Значения в полях пароля не маскируются в сетке
-  [KB 4569438] "Обработка остановлена из-за проблемы проверки" после маркировки строки при сопоставлении проводок поставщика
-  [KB 4569434] При обновлении формы юридических лиц число записей уменьшается
-  [KB 4575297] При редактировании и переходе по сетке фокус остается перемещенным в область регистратора задач
-  [KB 4566773] Корректирующие проводки не отображаются как отрицательные в запросе по проводкам по ваучеру 
-  [KB 4575288] При выборе границы между строками простого списка фокус переустанавливается на активную строку
-  [KB 4575287] Фокус не возвращается в первый столбец при использовании стрелки вниз для создания новой строки в журналах
-  [KB 4564819] Невозможно удалить строки накладной с произвольным текстом (так как источник данных ChangeGroupMode=ImplicitInnerOuter)
-  [KB 4563317] Подсказки/расширенное представление на показываются для изображений

### <a name="fixed-as-part-of-10012"></a>Исправлено как часть 10.0.12

- [KB 4558545] Элементы управления таблицы не обновляют содержимое отображаемых элементов.
- [KB 4558570] После удаления записи пункты все равно отображаются на странице.
- [KB 4558572] Стили, связанные с панелью списка **ExtendedStyle**, не применяются.
- [KB 4558573] Ошибки проверки не могут быть исправлены, если требуемое изменение находится вне сетки.
- [KB 4558584] Отрицательные числа отображаются неправильно.
- [KB 4560726] Возникала "Неожиданная ошибка клиента" после переключения между списками с помощью элемента управления "представление списка".
- [KB 4562141] Индексы сетки отключены после добавления новой записи.
- [KB 4562151] Параметры регистратора задач **Проверить** и **Копировать** недоступны для элементов управления даты или числа. 
- [KB 4562153] Флажки множественного выбора не отображаются в сетках списка/карт.
- [KB 4562646] Иногда невозможно щелкнуть вне сетки после выбора нескольких строк в сетке.
- [KB 4562647] После добавления новой строки в сетку ролей безопасности сбрасывается фокус на первый элементу управления в диалоговом окне **Публикация**.
- [KB 4563310] Расширенный предварительный просмотр не закрывается после изменения строки.
- [KB 4563313] При выборе значения в поиске возникает происходит "Непредвиденная ошибка клиента" в Internet Explorer.
- [KB 4564557] Поиск и раскрывающиеся меню не будут открываться в Internet Explorer
- [KB 4563324] Переход не работает после открытия рабочей области **Управление персоналом**.

### <a name="fixed-as-part-of-10011"></a>Исправлено как часть 10.0.11

- [Проблема 432458] Пустые или повторяющиеся строки отображаются в начале некоторых дочерних коллекций.
- [KB 4549711] Строки в предложении по оплате не могут быть удалены правильно после включения нового элемента управления сетки.
- [KB 4558374] Записи, для которых требуется диалоговое окно полиморфного селектора, создать невозможно.
- [KB 4558375] Текст справки не отображается в столбцах новой сетки.
- [KB 4558376] Сетки панели списка не отображаются с нужной высотой в Internet Explorer.
- [KB 4558377] Столбцы с полем со списком, ширина которых равна **SizeToAvailable**, не отображаются на некоторых страницах.
- [KB 4558378] Детализация иногда открывает неправильную запись.
- [KB 4558379] Ошибка возникает при открытии подстановки там, где **ReplaceOnLookup**=**No**.
- [KB 4558380] Доступное место в сетке не заполняется сразу после сворачивания части страницы.
- [KB 4558381] Отрицательные числа отображаются неправильно/пользователи иногда ничего не могут сделать после возникновения ошибок проверки.
- [KB 4558382] Возникли неожиданные ошибки клиента.
- [KB 4558383] Элементы управления вне сетки не обновляются после удаления последней записи.
- [KB 4558587] В ссылочных группах, имеющих поля со списком для полей замены, не отображаются значения.
- [KB 4562143] Поля не обновляются после того, как обработка изменения строки или сетки зависает после удаления строки.
- [KB 4562645] Возникает исключение при открытии поиска во время выполнения тестов Regression Suite Automation Tool (RSAT).

### <a name="fixed-as-part-of-10010"></a>Исправлено как часть 10.0.10

- [Проблема 414301] При создании новых строк некоторые данные из предыдущих строк исчезают.
- [Ошибка 417044] Для сеток в стиле списка отсутствует сообщение о пустой сетке.
- [KB 4539058] Некоторые сетки (обычно на экспресс-вкладках) иногда не отображаются (однако они будут отображаться при уменьшении).
- [KB 4549734] Активные строки не обрабатываются как отмеченные, если столбец с отметками скрыт.
- [KB 4549796] Нельзя изменять значения в сетке, когда она находится в режиме просмотра.
- [KB 4558367] Выбор текста не согласован при изменении строк.
- [KB 4558368] Множественный выбор с помощью клавиатуры разрешен в сценариях с одиночным выбором.
- [KB 4558369] Изображения состояния исчезают в иерархической сетке.
- [KB 4558370] Новая строка не прокручивается в представлении.
- [KB 4558372] Новая сетка зависает в режиме обработки, если число столбцов во вставляемом содержимом превышает количество оставшихся столбцов в сетке.
- [KB 4562631] Значения времени форматируются неправильно.

### <a name="quality-update-for-1009platform-update-33"></a>Обновление качества для 10.0.9/Platform update 33

- [KB 4550367] Значения времени форматируются неправильно.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
