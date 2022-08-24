---
title: Учебник Regression Suite Automation Tool
description: В этой статье показано, как использовать средство Regression Suite Automation Tool (RSAT). В нем описываются различные функции и приводятся примеры использования расширенного сценария.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: a270398ddebef0f47a2c31b0ffb022e3df6489c7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277415"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Учебник Regression Suite Automation Tool

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Загрузите и сохраните эту страницу в формате PDF с помощью средств веб-браузера.

В этом учебнике представлено несколько дополнительных функций средства Regression Suite Automation Tool (RSAT), включается демонстрационное назначение, а также описываются стратегия и ключевые моменты обучения.

## <a name="notable-features-of-rsat-and-task-recorder"></a>Важные функции RSAT и регистратора задач

### <a name="validate-a-field-value"></a>Проверка значения поля

RSAT позволяет включить в тестовый случай шаги проверки для проверки ожидаемых значений. Сведения об этой функции см. в статье [Проверка ожидаемых значений](rsat-validate-expected.md).

В следующем примере показано, как можно использовать эту функцию для проверки того, что запасы в наличии больше 0 (нуля).

1. В демонстрационных данных компании **USMF** создайте запись задачи, которая имеет следующие шаги:

    1. Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.
    2. Используйте экспресс-фильтр для поиска записей. Например, отфильтруйте по значению **1000** поле **Номер номенклатуры**.
    3. Выберите **Запасы в наличии**.
    4. Используйте экспресс-фильтр для поиска записей. Например, отфильтруйте поле **Сайт** по значению **1**.
    5. В списке пометьте выбранную строку.
    6. Убедитесь, что значение поля **Доступное общее количество** равно **411,0000000000000000**.

2. Сохраните запись задачи как **запись разработчика** и вложите ее в тестовый случай в Azure DevOps.
3. Добавьте тестовый случай в план испытаний и загрузите тестовый случай в RSAT.
4. Откройте файл параметров Excel и перейдите на вкладку **TestCaseSteps**.
5. Чтобы обеспечить, что запасы в наличии всегда будут больше **0**, перейдите на шаг **Проверить общее доступное количество** и измените значение с **411** на **0**. Измените значение поля **Оператор** со знака равенства (**=**) на знак "больше" (**\>**).
6. Сохраните и закройте файл параметров Excel.
7. Выберите **Отправить**, чтобы сохранить изменения, внесенные в файл параметров Excel, в Azure DevOps.

Теперь если в поле **Доступное общее количество** для указанной номенклатуры в складских запасах значение больше 0 (нуля), тест проходит успешно, независимо от фактического значения запасов в наличии.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Сохраненные переменные и цепочки тестовых случаев

Одной из важнейших функций RSAT является связывание тестовых случаев, то есть, возможность тестов передавать переменные в другие тесты. Дополнительные сведения см. в статье [Копирование переменных в цепочку тестовых случаев](rsat-chain-test-cases.md).

### <a name="derived-test-case"></a>Производный тестовый случай

RSAT позволяет использовать одну запись задач с несколькими тестовыми случаями, что позволяет выполнять задачу с различными конфигурациями данных. Дополнительные сведения см. в статье [Производные тестовые случаи](rsat-derived-test-cases.md).

### <a name="validate-notifications-and-messages"></a>Проверка уведомлений и сообщений

Эта функция может использоваться для проверки, произошло ли действие. Например, когда производственный заказ создается, оценивается, а затем запускается, в приложении отображается сообщение "Производство — начало", уведомляющее о запуске производственного заказа.

![Уведомление "Производство — начало".](./media/use_rsa_tool_05.png)

Вы можете проверить это сообщение через RSAT, вводя текст сообщения на вкладке **MessageValidation** файла параметров Excel для соответствующей записи.

![Вкладка проверки сообщения.](./media/use_rsa_tool_06.png)

После запуска тестового случая сообщение в файле параметров Excel сравнивается с отображаемым сообщением. Если сообщения не совпадают, тестовый случай будет неудачным.

> [!NOTE]
> На вкладке **MessageValidation** в файле параметров Excel можно ввести более одного сообщения. Сообщения также могут быть сообщениями об ошибках или предупреждениями, а не информационными сообщениями.

### <a name="snapshot"></a>Снимок

Эта функция делает снимки экрана шагов, которые были выполнены во время записи задачи. Это полезно для целей аудита или отладки.

- Для использования этой функции при выполнении RSAT с пользовательским интерфейсом откройте файл **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** в папке установки RSAT (например, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) и измените значение следующего элемента с **false** на **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- Для использования этой функции при выполнении RSAT с помощью интерфейса командной строки (например, Azure DevOps) откройте файл **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config** в папке установки RSAT (например, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) и измените значение следующего элемента с **false** на **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

При выполнении тестовых случаев RSAT создает снимки (изображения) шагов и сохраняет их в папке воспроизведения тестовых случаев в рабочем каталоге. В папке воспроизведения отдельная вложенная папка создается с именем **StepSnapshots**. Эта папка содержит снимки для выполняемых тестовых случаев.

## <a name="assignment"></a>Назначение

### <a name="scenario"></a>Сценарий

1. Конструктор продуктов создает новый выпущенный продукт.
2. Менеджер производства запускает производственный заказ, чтобы восстановить уровень запасов в две единицы.
3. Производство начинается и завершает производственный заказ, и проверяет, что количество в наличии равно двум единицам.
4. Группа продавцов получает заказ на четыре единицы нового продукта. Поэтому группа продаж обновляет чистые потребности с помощью динамического плана. Поскольку дополнительные мощности отсутствуют, для политики заказа по умолчанию устанавливается значение "купить вместо создания". Поэтому создается спланированный заказ на покупку.
5. Покупатель добавляет поставщика, подтверждает запланированный заказ на покупку, затем утверждает заказ на покупку.
6. Когда купленные товары поступают в магазин, оператор магазина выполняет поиск товаров соответствующих заказов на покупку и получает товары. Так как заказ готов, товары могут комплектоваться и упаковываться по заказу на продажу.
7. Финансовый отдел выполняет разноску накладной по покупке и накладной по продаже.

На следующем рисунке показана последовательность операций для этого сценария.

![Последовательность операций для демонстрационного сценария.](./media/use_rsa_tool_14.png)

На следующем рисунке показана иерархия бизнес-процессов для этого сценария в средстве моделирования бизнес-процессов LCS.

![Бизнес-процессы для демонстрационного сценария.](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Стратегия — ключевое обучение

### <a name="data"></a>Данные

- Убедитесь в том, что имеются репрезентативные объемы данных (копия производственных/золотых данных конфигурации и перенесенные данные).
- При создании новых данных с помощью регистратора задач создайте имена тестов, которые не будут конфликтовать с существующими именами (например, используйте префикс, такой как **RSATxxx**).
- Для повторного выполнения тестов в средах без уровней 1 используйте функцию восстановление на момент времени Azure.
- Хотя можно использовать функции Excel **RANDOM** и **NOW** для создания уникальной комбинации, усилия весьма высоки. Рассмотрим пример:

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>Регистратор задач

- Прежде чем начать запись, определите сценарии. Хорошо управляемый проект имеет предопределенные сценарии тестирования. Чтобы создать тестовый случай, необходимо оценить, насколько предсказуемым являются результаты этих сценариев тестирования.
- Разделите записи, если они выполняются другими ролями, или если имеется время ожидания или внешнее событие до следующего шага.
- Не следует выбирать значения в списках. Вместо этого используйте текстовые форматы, такие как **FIFO**, **AudioRM** и **SiteWH**. При выборе в списке записывается позиция значения в списке, а не само значение. Если в этот список добавлены элементы, положение значения может измениться Поэтому запись будет использовать другой параметр, и остальная часть сценария может быть изменена.
- Подумайте о поведении нескольких пользователей. Например, не следует предполагать, что вновь созданный заказ на продажу всегда будет выбран автоматически. Вместо этого для поиска правильного заказа обязательно следует использовать фильтр.
- Используйте функцию копирования в регистраторе задач для сохранения имени вновь созданного продукта, чтобы его можно было использовать в связанных тестовых случаях.
- Используйте функцию проверки в регистраторе задач для установки контрольных точек, которые проверяют правильность выполнения шагов.

### <a name="rsat"></a>RSAT

- Чтобы выполнить тест в другой компании, можно изменить эту компанию на вкладке **Общие** файла параметров Excel. Убедитесь, что параметры и данные доступны в новой выбранной компании.
- Тестового пользователя можно изменить на вкладке **Общие** файла параметров Excel. Укажите код электронной почты пользователя, который будет выполнять тестовый случай. Таким образом, тестовый случай может быть выполнен с помощью разрешений безопасности указанного пользователя.
- Чтобы подождать, пока начнется тест, можно определить паузу на вкладке **Общие** файла параметров Excel. Эта пауза может использоваться в пакетном задании (например, если рабочий процесс должен выполняться до того, как будет выполнен следующий шаг).

## <a name="advanced-scripting"></a>Дополнительные сценарии

### <a name="cli"></a>CLI

RSAT можно вызывать из окна **Командная строка** или **PowerShell**.

> [!NOTE]
> Убедитесь, что для переменной среды **TestRoot** установлен путь установки RSAT. (В Microsoft Windows откройте **Панель управления**, выберите пункт **Система и безопасность \> Система \> Дополнительные параметры системы**, затем выберите **Переменные среды**.)

1. Откройте окно **Командная строка** или **PowerShell** от имени администратора.
2. Перейдите в каталог установки RSAT.

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Выведите список всех команд.

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Перечисление всех команд или отображение справки для конкретной команды вместе с доступными параметрами.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Необязательные параметры

`command`: где ``[command]`` — это одна из команд в предыдущем списке.

#### <a name="about"></a>о программе

Отображается версия установленного RSAT.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Очищает экран.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>загрузить

Загружает вложения (запись, выполнение и файлы параметров) для указанного тестового случая из Azure DevOps в выходной каталог. Можно использовать команду ``list`` для возврата всех доступных тестовых случаев и использовать любое значение из первого столбца в качестве параметра **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>download: необязательные ключи

+ `/retry[=seconds]`: если этот ключ указан и тестовые случаи обращения блокируются другими экземплярами RSAT, процесс загрузки будет ожидать указанное число секунд, а затем будет выполнена повторная попытка. Значение по умолчанию для \[seconds\] составляет 120 секунд. Без этого ключа процесс будет отменен сразу же после блокирования тестовых случаев.

##### <a name="download-required-parameters"></a>загрузить: обязательные параметры

+ `test_case_id`: представляет идентификатор тестового случая.

##### <a name="download-optional-parameters"></a>download: необязательные параметры

+ `output_dir`: представляет выходной рабочий каталог. Каталог должна существовать. Если этот параметр не указан, будет использоваться рабочий каталог из параметров.

##### <a name="download-examples"></a>загрузить: примеры

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>downloadsuite

Загружает вложения (файлы записи, выполнения и параметров) для всех тестовых случаев в указанном комплекте тестовых случаев из Azure DevOps в выходной каталог. Можно использовать команду ``listtestsuitenames`` для возврата всех доступных тестовых комплектов и использовать любое значение в качестве параметра **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>downloadsuite: необязательные ключи

+ `/retry[=seconds]`: если этот ключ указан и тестовые случаи обращения блокируются другими экземплярами RSAT, процесс загрузки будет ожидать указанное число секунд, а затем будет выполнена повторная попытка. Значение по умолчанию для \[seconds\] составляет 120 секунд. Без этого ключа процесс будет отменен сразу же после блокирования тестовых случаев.
+ `/byid`: этот ключ указывает, что требуемый комплект тестов определяется его идентификатором Azure DevOps, а не именем комплекта тестов.

##### <a name="downloadsuite-required-parameters"></a>downloadsuite: обязательные параметры

+ `test_suite_name`: представляет имя набора тестов. Этот параметр является обязательным, если ключ /byid **не** указан. Это имя является именем комплекта тестов Azure DevOps.
+ `test_suite_id`: представляет идентификатор набора тестов. Этот параметр является обязательным, если ключ /byid **указан**. Этот код является идентификатором комплекта тестов Azure DevOps.

##### <a name="downloadsuite-optional-parameters"></a>downloadsuite: необязательные параметры

+ `output_dir`: представляет выходной рабочий каталог. Каталог должна существовать. Если этот параметр не указан, будет использоваться рабочий каталог из параметров.

##### <a name="downloadsuite-examples"></a>downloadsuite: примеры

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>изменить

Позволяет открыть файл параметров в программе Excel и изменить его.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>изменить: обязательные параметры

+ `excel_file`: должен содержать полный путь к существующему файлу Excel.

##### <a name="edit-examples"></a>изменить: примеры

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>создать

Создает для указанного тестового случая в выходном каталоге параметры выполнения тестов и файлы параметров. Можно использовать команду ``list`` для извлечения всех доступных тестовых случаев. Используйте любое значение из первого столбца в качестве параметра **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>generate: необязательные ключи

+ `/retry[=seconds]`: если этот ключ указан и тестовые случаи обращения блокируются другими экземплярами RSAT, процесс создания будет ожидать указанное число секунд, а затем будет выполнена повторная попытка. Значение по умолчанию для \[seconds\] составляет 120 секунд. Без этого ключа процесс будет отменен сразу же после блокирования тестовых случаев.
+ `/dllonly`: создание только файлов выполнения тестов. Не создавать повторно файл параметров Excel.
+ `/keepcustomexcel`: обновление существующего файла параметров. Также повторно создает файлы выполнения.

##### <a name="generate-required-parameters"></a>создать: обязательные параметры

+ `test_case_id`: представляет идентификатор тестового случая.

##### <a name="generate-optional-parameters"></a>generate: необязательные параметры

+ `output_dir`: представляет выходной рабочий каталог. Каталог должна существовать. Если этот параметр не указан, будет использоваться рабочий каталог из параметров.

##### <a name="generate-examples"></a>создать: примеры

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

Создает новый производный тестовый случай (дочерний тестовый случай) от предоставленного тестового случая. Новый тестовый случай также добавляется к указанному набору тестов. Можно использовать команду ``list`` для возврата всех доступных тестовых случаев и использовать любое значение из первого столбца в качестве параметра **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>generatederived: необязательные ключи

+ `/retry[=seconds]`: если этот ключ указан и тестовые случаи обращения блокируются другими экземплярами RSAT, процесс создания будет ожидать указанное число секунд, а затем будет выполнена повторная попытка. Значение по умолчанию для \[seconds\] составляет 120 секунд. Без этого ключа процесс будет отменен сразу же после блокирования тестовых случаев.

##### <a name="generatederived-required-parameters"></a>generatederived: обязательные параметры

+ `parent_test_case_id`: представляет идентификатор родительского тестового случая.
+ `test_plan_id`: представляет идентификатор плана тестирования.
+ `test_suite_id`: представляет идентификатор набора тестов.

##### <a name="generatederived-examples"></a>generatederived: примеры

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Создает только файлы выполнения тестов для указанного тестового случая. Не создает файл параметров Excel. Файлы создаются в указанном выходном каталоге. Можно использовать команду ``list`` для возврата всех доступных тестовых случаев и использовать любое значение из первого столбца в качестве параметра **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: необязательные ключи

+ `/retry[=seconds]`: если этот ключ указан и тестовые случаи обращения блокируются другими экземплярами RSAT, процесс создания будет ожидать указанное число секунд, а затем будет выполнена повторная попытка. Значение по умолчанию для \[seconds\] составляет 120 секунд. Без этого ключа процесс будет отменен сразу же после блокирования тестовых случаев.

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: обязательные параметры

+ `test_case_id`: представляет идентификатор тестового случая.

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: необязательные параметры

+ `output_dir`: представляет выходной рабочий каталог. Каталог должна существовать. Если этот параметр не указан, будет использоваться рабочий каталог из параметров.

##### <a name="generatetestonly-examples"></a>generatetestonly: примеры

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

Создает файлы автоматизации тестов для всех тестовых случаев в указанном комплекте тестов. Можно использовать команду ``listtestsuitenames`` для возврата всех доступных тестовых комплектов и использовать любое значение в качестве параметра **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>generatetestsuite: необязательные ключи

+ `/retry[=seconds]`: если этот ключ указан и тестовые случаи обращения блокируются другими экземплярами RSAT, процесс создания будет ожидать указанное число секунд, а затем будет выполнена повторная попытка. Значение по умолчанию для \[seconds\] составляет 120 секунд. Без этого ключа процесс будет отменен сразу же после блокирования тестовых случаев.
+ `/dllonly`: создание только файлов выполнения тестов. Не создавать повторно файл параметров Excel.
+ `/keepcustomexcel`: обновление существующего файла параметров. Также повторно создает файлы выполнения.
+ `/byid`: этот ключ указывает, что требуемый комплект тестов определяется его идентификатором Azure DevOps, а не именем комплекта тестов.

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: обязательные параметры

+ `test_suite_name`: представляет имя набора тестов. Этот параметр является обязательным, если ключ /byid **не** указан. Это имя является именем комплекта тестов Azure DevOps.
+ `test_suite_id`: представляет идентификатор набора тестов. Этот параметр является обязательным, если ключ /byid **указан**. Этот код является идентификатором комплекта тестов Azure DevOps.

##### <a name="generatetestsuite-optional-parameters"></a>generatetestsuite: необязательные параметры

+ `output_dir`: представляет выходной рабочий каталог. Каталог должна существовать. Если этот параметр не указан, будет использоваться рабочий каталог из параметров.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: примеры

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>справка

Идентично значению [?](#section) команда.

#### <a name="list"></a>список

Список всех доступных тестовых случаев в текущем плане тестирования.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Список всех доступных планов тестирования.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Перечисляет тестовые случаи для указанного набора тестов. Можно использовать команду ``listtestsuitenames`` для возврата всех доступных тестовых комплектов и использовать любое значение из списка в качестве параметра **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: обязательные параметры

+ `test_suite_name`: имя нужного комплекта.

##### <a name="listtestsuite-examples"></a>listtestsuite: примеры

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestsuitebyid

Перечисляет тестовые случаи для указанного набора тестов.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestsuitebyid: обязательные параметры

+ `test_suite_id`: идентификатор нужного комплекта.

##### <a name="listtestsuitebyid-examples"></a>listtestsuitebyid: примеры

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Список всех доступных комплектов тестов в текущем плане тестирования.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>воспроизведение

Воспроизводит тестовый случай, связанный с указанным файлом параметров Excel. Эта команда использует существующие локальные файлы автоматизации и не загружает файлы с Azure DevOps. Эта команда не поддерживается для тестовых случаев для POS Commerce.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>playback: необязательные ключи

+ `/retry[=seconds]`: если этот ключ указан и тестовые случаи обращения блокируются другими экземплярами RSAT, процесс воспроизведения будет ожидать указанное число секунд, а затем будет выполнена повторная попытка. Значение по умолчанию для \[seconds\] составляет 120 секунд. Без этого ключа процесс будет отменен сразу же после блокирования тестовых случаев.
+ `/comments[="comment"]`: предоставьте пользовательскую информационную строку, которая будет включена в поле **Комментарии** на страницах сводки и результатов тестов для выполнений тестовых случаев Azure DevOps.

##### <a name="playback-required-parameters"></a>воспроизведение: обязательные параметры

+ `excel_parameter_file`: полный путь к файлу параметров Excel. Этот файл должен существовать.

##### <a name="playback-examples"></a>воспроизведение: примеры

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Воспроизведение нескольких тестовых случаев одновременно. Тестовые случаи определяются по их идентификатору. Эта команда загружает файлы из Azure DevOps. Можно использовать команду ``list`` для возврата всех доступных тестовых случаев и использовать любое из значений из первого столбца в качестве параметра **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>playbackbyid: необязательные ключи

+ `/retry[=seconds]`: если этот ключ указан и тестовые случаи обращения блокируются другими экземплярами RSAT, процесс воспроизведения будет ожидать указанное число секунд, а затем будет выполнена повторная попытка. Значение по умолчанию для \[seconds\] составляет 120 секунд. Без этого ключа процесс будет отменен сразу же после блокирования тестовых случаев.
+ `/comments[="comment"]`: предоставьте пользовательскую информационную строку, которая будет включена в поле **Комментарии** на страницах сводки и результатов тестов для выполнений тестовых случаев Azure DevOps.

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: обязательные параметры

+ `test_case_id1`: идентификатор существующего тестового случая.
+ `test_case_id2`: идентификатор существующего тестового случая.
+ `test_case_idN`: идентификатор существующего тестового случая.

##### <a name="playbackbyid-examples"></a>playbackbyid: примеры

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Воспроизведение нескольких тестовых случаев одновременно. Тестовые случаи определяются файлами параметров Excel. Эта команда использует существующие локальные файлы автоматизации и не загружает файлы с Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>playbackmany: необязательные ключи

+ `/retry[=seconds]`: если этот ключ указан и тестовые случаи обращения блокируются другими экземплярами RSAT, процесс воспроизведения будет ожидать указанное число секунд, а затем будет выполнена повторная попытка. Значение по умолчанию для \[seconds\] составляет 120 секунд. Без этого ключа процесс будет отменен сразу же после блокирования тестовых случаев.
+ `/comments[="comment"]`: предоставьте пользовательскую информационную строку, которая будет включена в поле **Комментарии** на страницах сводки и результатов тестов для выполнений тестовых случаев Azure DevOps.

##### <a name="playbackmany-required-parameters"></a>playbackmany: обязательные параметры

+ `excel_parameter_file1`: полный путь к файлу параметров Excel. Этот файл должен существовать.
+ `excel_parameter_file2`: полный путь к файлу параметров Excel. Этот файл должен существовать.
+ `excel_parameter_fileN`: полный путь к файлу параметров Excel. Этот файл должен существовать.

##### <a name="playbackmany-examples"></a>playbackmany: примеры

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Воспроизведение всех тестовых случаев из одного или нескольких указанных комплектов тестов. Если указан ключ /local, для воспроизведения будут использоваться локальные вложения. В противном случае вложения будут загружены из Azure DevOps. Можно использовать команду ``listtestsuitenames`` для возврата всех доступных тестовых комплектов и использовать любое значение из первого столбца в качестве параметра **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>playbacksuite: необязательные ключи

+ `/updatedriver`: если этот ключ указан, WebDriver Интернет-браузера будет обновлен как требуется до начала процесса воспроизведения.
+ `/local`: этот ключ указывает на необходимость использования локальных вложений для воспроизведения вместо загрузки файлов из Azure DevOps.
+ `/retry[=seconds]`: если этот ключ указан и тестовые случаи обращения блокируются другими экземплярами RSAT, процесс воспроизведения будет ожидать указанное число секунд, а затем будет выполнена повторная попытка. Значение по умолчанию для \[seconds\] составляет 120 секунд. Без этого ключа процесс будет отменен сразу же после блокирования тестовых случаев.
+ `/comments[="comment"]`: предоставьте пользовательскую информационную строку, которая будет включена в поле **Комментарии** на страницах сводки и результатов тестов для выполнений тестовых случаев Azure DevOps.
+ `/byid`: этот ключ указывает, что требуемый комплект тестов определяется его идентификатором Azure DevOps, а не именем комплекта тестов.

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: обязательные параметры

+ `test_suite_name1`: представляет имя набора тестов. Этот параметр является обязательным, если ключ /byid **не** указан. Это имя является именем комплекта тестов Azure DevOps.
+ `test_suite_nameN`: представляет имя набора тестов. Этот параметр является обязательным, если ключ /byid **не** указан. Это имя является именем комплекта тестов Azure DevOps.
+ `test_suite_id1`: представляет идентификатор набора тестов. Этот параметр является обязательным, если ключ /byid **указан**. Этот код является идентификатором комплекта тестов Azure DevOps.
+ `test_suite_idN`: представляет идентификатор набора тестов. Этот параметр является обязательным, если ключ /byid **указан**. Этот код является идентификатором комплекта тестов Azure DevOps.

##### <a name="playbacksuite-examples"></a>playbacksuite: примеры

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>playbacksuitebyid

Выполнение всех тестовых случаев в указанном комплекте тестов Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>playbacksuitebyid: необязательные ключи

+ `/retry[=seconds]`: если этот ключ указан и тестовые случаи обращения блокируются другими экземплярами RSAT, процесс воспроизведения будет ожидать указанное число секунд, а затем будет выполнена повторная попытка. Значение по умолчанию для \[seconds\] составляет 120 секунд. Без этого ключа процесс будет отменен сразу же после блокирования тестовых случаев.
+ `/comments[="comment"]`: предоставьте пользовательскую информационную строку, которая будет включена в поле **Комментарии** на страницах сводки и результатов тестов для выполнений тестовых случаев Azure DevOps.
+ `/byid`: этот ключ указывает, что требуемый комплект тестов определяется его идентификатором Azure DevOps, а не именем комплекта тестов.

##### <a name="playbacksuitebyid-required-parameters"></a>playbacksuitebyid: обязательные параметры

+ `test_suite_id`: представляет идентификатор комплекта тестов в том виде, в котором он существует в Azure DevOps.

##### <a name="playbacksuitebyid-examples"></a>playbacksuitebyid: примеры

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>закрыть

Закрывает приложение. Эта команда полезна только в том случае, если приложения выполняются в интерактивном режиме.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>quit: примеры

`quit`

#### <a name="upload"></a>отправить

Отправка файлов вложений (файлы записи, выполнения и параметров), относящихся к определенному комплекту тестов или тестовым случаям, в Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>отправить: обязательные параметры

+ `test_suite_name`: все файлы, которые относятся к определенному набору тестов, будут отправлены.
+ `test_case_id1`: представляет первый идентификатор тестового случая, который должен быть отправлен. Используйте этот параметр только в том случае, если не указано имя комплекта тестов.
+ `test_case_idN`: представляет последний идентификатор тестового случая, который должен быть отправлен. Используйте этот параметр только в том случае, если не указано имя комплекта тестов.

##### <a name="upload-examples"></a>отправить: примеры

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Отправляет только файл записи, принадлежащий к одному или нескольким указанным тестовым случаям, в Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: обязательные параметры

+ `test_case_id1`: представляет идентификатор первого тестового случая для записи, который должен быть отправлен в Azure DevOps.
+ `test_case_idN`: представляет идентификатор последнего тестового случая для записи, который должен быть отправлен в Azure DevOps.

##### <a name="uploadrecording-examples"></a>uploadrecording: примеры

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>использование

Отображение трех режимов использования данного приложения.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

Выполнение приложения в интерактивном режиме:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

Выполнение приложения путем указания команды:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

Выполнение приложения путем указания файла параметров:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

### <a name="windows-powershell-examples"></a>Примеры Windows PowerShell

#### <a name="run-a-test-case-in-a-loop"></a>Выполнение тестового случая в цикле

Имеется тестовый сценарий, создающий нового клиента. С помощью сценариев этот тестовый случай можно выполнить в цикле путем случайного выбора следующих данных перед выполнением каждой итерации:

- Код клиента
- Наименование Клиента
- Адрес клиента

Код клиента будет иметь формат *ATCUS\<number\>*, где \<number\> представляет собой значение в диапазоне от **000000001** до **999999999**.

В следующем примере для определения первого используемого номера используется один параметр, **start**. Второй параметр **nr** служит для определения числа клиентов, которые должны быть созданы. Для каждой итерации параметры в файле параметров Excel изменяются с помощью функции UpdateCustomer. После этого командная строка RSAT вызывается в функции RunTestCase.

Откройте интегрированную среду сценариев Microsoft Windows PowerShell (ISE) в режиме администратора и вставьте следующий код в окно с именем **Untitled1.ps1**.

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>Выполнение сценария, который зависит от данных в Microsoft Dynamics 365

В следующем примере для поиска статуса заказа на покупку используется вызов по протоколу OData (Open Data Protocol). Если статус не равен **выставлена накладная**, можно, например, вызвать тестовый случай RSAT, который разносит накладную.

```powershell
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
