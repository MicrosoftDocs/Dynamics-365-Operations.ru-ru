---
title: Электронная отчетность — Создание требуемой конфигурации для импорта данных из внешнего файла
description: В этой статье описывается, как разрабатывать конфигурации электронной отчетности для импорта данных в приложение Microsoft Dynamics 365 Finance из внешнего файла.
author: kfend
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
ms.openlocfilehash: 199873af83ec14d441aa3927dc84509486e4927a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290165"
---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a>Электронная отчетность — Создание требуемой конфигурации для импорта данных из внешнего файла

[!include [banner](../../includes/banner.md)]

В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать конфигурации электронной отчетности для импорта данных в приложение из внешнего файла. В этом примере вам предстоит создать необходимые конфигурации ER для примера компании Litware, Inc. Чтобы выполнить следующие шаги, вам необходимо выполнить шаги в проводнике по задаче "Электронная отчетность — Создание поставщика конфигурации и пометка его как активного". Эти шеги можно выполнить с использованием набора данных USMF. Кроме того, необходимо загрузить и сохранить следующие файлы локально: 

| Описание содержания                       | Имя файла                                     |
|-------------------------------------------|-----------------------------------------------|
| Конфигурации модели данных электронной отчетности - 1099 | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)                  |
| Конфигурация формата электронной отчетности - 1099    | [1099format.xml](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)                  |
| Пример входящего документа в формате XML                          | [1099entries.xml](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)        |
| Пример книги для управления данными входящего документа                          | [1099entries.xlsx](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx) |

ER предоставляет бизнес-пользователям возможность настраивать процесс импорта внешних файлов данных в таблицы в формате XML или TXT. Во-первых, абстрактная модель данных и конфигурация модели данных ER должны быть созданы таким образом, чтобы представлять импортируемые данные. Затем необходимо определить структуру импортируемого файла и метод, который будет использоваться для переноса данных из файла в абстрактную модель данных. Необходимо создать конфигурацию формата ER, которая будет соответствовать созданной модели данных для этой абстрактной модели данных. После этого необходимо расширить конфигурацию модели данных, добавив сопоставление, которое описывает, как импортируемые данные сохраняются как данные абстрактной модели данных и как они используются для обновления таблиц.  В конфигурацию модели данных ER должно быть добавлено новое сопоставление модели, описывающее привязку модели данных к местам назначения приложения.  

Следующий сценарий показывает возможности импорта данных ER. Сюда входят проводки по поставщику, которые отслеживаются извне, а затем импортируются, чтобы позже включаться в отчеты в сопоставлении поставщика для формы 1099.   

## <a name="add-a-new-er-model-configuration"></a>Добавление новой конфигурации модели ER
1. Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".

    Проверьте, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как активные. Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Электронная отчетность — создание поставщика конфигурации и пометка его как активного".   

2. Щелкните "Конфигурации отчетности".

    Вместо того чтобы создавать новую модель для поддержки импорта данных, загрузите файл 1099model.xml, загруженный ранее. Этот файл содержит модель пользовательских данных проводок по поставщику. Эта модель данных сопоставляется с компонентами данных, которые находятся в объекте данных AOT.   

3. Щелкните "Обменять".
4. Щелкните "Загрузить из XML-файла".

    Нажмите кнопку "Обзор" и перейдите к ранее загруженному файлу 1099model.xml.  

5. Нажмите кнопку "OК".
6. В дереве выберите "Модель платежей по форме 1099".

## <a name="review-data-model-settings"></a>Проверка параметров модели данных
1. Выберите Конструктор.

    Эта модель предназначена для представления проводок по поставщикам с точки зрения бизнеса и не связана с реализацией.   

2. В дереве разверните узел ''1099-MISC".
3. В дереве выберите "1099-MISC\Проводки".
4. В дереве разверните узел "1099-MISC\Проводки".

    Элемент "Проводки" этой модели представляет отдельные проводки. Дочерние элементы используются для указания требуемых сведений, таких как счет поставщика и дата проводки для каждой проводки.   

5. Закройте страницу.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Добавление новой конфигурации формата ER, поддерживающей импорт данных
Шаги в этой подзадаче показывают, как можно создать новую конфигурацию формата для управления импортом данных из внешних файлов.   
1. Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.
2. В поле "Создать" введите «Формат, основанный на модели данных "Модель платежей по форме 1099"».
3. Выберите "Да" в поле "Поддерживает импорт данных".
4. Нажмите клавишу ESC, чтобы закрыть эту страницу.

    Вместо того чтобы создавать новый формат для поддержки импорта данных, загрузите файл 1099format.xml, загруженный ранее. Этот файл содержит определенную структуру импортируемого файла и сопоставление структуры с моделью пользовательских данных проводок по поставщикам.   
5. Щелкните "Обменять".
6. Щелкните "Загрузить из XML-файла".
    Нажмите кнопку "Обзор" и перейдите к ранее загруженному файлу 1099format.xml.  
7. Нажмите кнопку "OК".
8. В дереве разверните узел "Модель платежей по форме 1099".
9. В дереве выберите "Модель платежей по форме 1099\Формат для импорта проводок поставщиков".

## <a name="review-format-settings"></a>Проверка параметров формата
1. Выберите Конструктор.
2. Установите переключатель "Показать сведения" в положение "Вкл.".
3. Щелкните "Развернуть/свернуть".
4. Щелкните "Развернуть/свернуть".

    Созданный формат представляет ожидаемую структуру внешнего файла. Этот файл должен быть в формате XML и иметь корневой элемент сопоставления. Проводка по каждому поставщику представлена элементом проводки, который определяется как имеющий кратность ноль ко многим. Это означает, что входящий файл может содержать от нуля до нескольких проводок. Вложенные элементы элемента "проводка" представляют атрибуты одной проводки. Обратите внимание, что все атрибуты, кроме страны, помечены как обязательные, что означает, что они должны присутствовать в импортируемом файле.   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a>Проверка параметров сопоставления формата с моделью данных
1. Щелкните "Сопоставить формат модели".

    Сопоставление "Для импорта проводок поставщиков" содержит правила переноса данных из входящего XML-файла в выбранную часть модели настраиваемых данных, которая определяется выбором определения 1099-MISC.  

2. Выберите Конструктор.
3. Установите переключатель "Показать сведения" в положение "Вкл.".
4. В дереве разверните "формат: Запись".
5. В дереве выберите "формат: Запись".

    Обратите внимание, что созданный формат представляется как компонент источника данных.  

6. В дереве разверните узел `format: Record\*settlement: XML Element 1..1 (settlement): Record`.
7. В дереве разверните узел `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list`.
8. В дереве разверните узел `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`.
9. В дереве разверните узел `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record`.
10. В дереве выберите узел `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`.

    Обратите внимание, что презентация обязательных и необязательных элементов формата отличается в предопределенном компоненте источника данных "формат".  
11. В дереве разверните "Проводки: Список записей= формат.сопоставление.'$enumerated'".

    Обратите внимание, что элементы формата, который определяет структуру импортированного файла, привязаны к элементам модели пользовательских данных. На основании этих привязок содержимое импортированного XML-файла будет храниться во время выполнения в существующей модели данных. Обратите внимание на привязку элемента страны. Для любого элемента проводки во входящем файле, не имеющего такой элемент, в модели данных будет заполнен код страны по умолчанию "США".  

12. Перейдите на вкладку "Проверки".

    Это сопоставление формата может содержать пользовательскую логику для проверки точности импортируемых данных с точки зрения бизнеса. Например, на основе параметра для любой проводки в импортируемом файле без определенного кода страны будет создаваться предупреждающее сообщение в Infolog, информирующее пользователя об этом и указывающее порядковый номер проводки.  

13. Закройте страницу.

## <a name="run-the-format-mapping-to-the-data-model"></a>Выполнение сопоставления формата с моделью данных
Выполните это сопоставление формата в целях тестирования. Используйте файл 1099entries.xml, загруженный ранее. Этот файл можно экспортировать из книги 1099entries.xlsx, используемой для управления проводками по поставщику. Созданные выходные данные будут импортированы из выбранного XML-файла и заполнят модель пользовательских данных в реальном импорте.  

1. Щелкните "Выполнить".

    Нажмите кнопку "Обзор" и перейдите к ранее загруженному файлу 1099entries.xml.  

2. Нажмите кнопку "OК".

    Обратите внимание на предупреждающее сообщение об отсутствующем коде страны для проводки в импортированном файле.  
    
    Просмотрите выходные данные в формате XML, представляющем данные, которые были импортированы из выбранного файла, а затем перенесены в модель данных.   

3. Закройте страницу.
4. Закройте страницу.

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a>Проверка параметров сопоставления модели с местами назначения
1. В дереве выберите "Модель платежей по форме 1099".
2. Выберите Конструктор.
3. Щелкните "Сопоставить модель с источником данных".

    Сопоставление для импорта проводок вручную по форме 1099 было определено с типом направления "В место назначения". Это означает, что оно было введено для поддержки импорта данных и содержит настройку правил, определяющих, как импортированный внешний файл и сохраненные как данные абстрактной модели данные будут использоваться для обновления таблиц в приложении.  

4. Выберите Конструктор.
5. В дереве разверните "модель: Модель данных Модель платежей по форме 1099".
6. В дереве разверните "модель: Модель данных Модель платежей по форме 1099\Проводки: Список записей".

    Обратите внимание, что созданная модель представляется как элемент источника данных. Во время выполнения она будет содержать данные, импортируемые из внешнего файла. Несколько таблиц были добавлены в качестве элементов источника данных для обеспечения того, что импортируемые данные соответствуют данным текущего приложения, включая доступность импортируемого счета поставщика для проводки в системе, существование комбинации кодов страны и государства импорта и т. д.  

7. В дереве выберите "модель: Модель данных Модель платежей по форме 1099\Проводки: Список записей\$failed: Вычисляемое поле = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean".
8. Щелкните "Изменить".
9. Щелкните "Изменить формулу".

    Если хотя бы одна проверка завершится с ошибкой для отдельной импортированной проводки, эта проводка будет помечена как не прошедшая проверку с помощью атрибута источника данных "$failed".  

10. Закройте страницу.
11. Щелкните "Отмена".
12. В дереве выберите "tax1099trans: Таблица 'VendSettlementTax1099' записи= модель.Проверено".
13. Щелкните "Изменить назначение".

    Место назначения ER было добавлено для указания того, как импортированные данные будут обновлять таблицы приложения. В этом случае выбрана таблица данных VendSettlementTax1099. Поскольку было выбрано действие "Вставить" действия записи, импортированные проводки будут вставлены в таблицу VendSettlementTax1099. Обратите внимание, что одно сопоставление модели может содержать несколько мест назначения. Это означает, что импортируемые данные можно использовать для одновременного обновления нескольких таблиц приложения. Таблицы, представления и объекты данных можно использовать как места назначения ER.   

    Если сопоставление будет вызываться с точки в приложении (например, кнопка или пункт меню), которая была специально предназначена для этого действия, место назначения ER должно быть помечено как точка интеграции. В данном примере это точка ERTableDestination#VendSettlementTax1099.  

14. Щелкните "Отмена".
15. Щелкните "Показать все".
16. Щелкните "Показать только сопоставленные".
17. В дереве разверните "tax1099trans: Таблица 'VendSettlementTax1099' записи= модель.Проверено".

    Обратите внимание, что элемента источника данных, который содержит только проверенные проводки, привязан к созданному месту назначения. Можно выполнить фильтрацию импортированных проводок, чтобы пропустить те, которые несовместимы с данными приложений.  

18. В дереве выберите "сбой: Таблица 'VendSettlementTax1099Entity' записи= модель.Сбой".
19. Перейдите на вкладку "Проверки".

    Это сопоставление модели может содержать пользовательскую логику для проверки правильности импортируемых данных из существующих данных приложения. Например, на основе текущего параметра для любой проводки в импортированном файле со счетом поставщика, отсутствующим в системе, будет создаваться предупреждающее сообщение, информирующее пользователя об этом и указывающее неверный код счета поставщика.  

    Обратите внимание, что параметр "Действие после проверки" может использоваться для каждой проверки для указания того, следует ли продолжать процесс импорта, а также следует ли сохранить или отменить уже выполненные операции вставки и обновления.  

20. Щелкните "Показать только сопоставленные".
21. Щелкните "Показать все".
22. Закройте страницу.

    Выполните это сопоставление модели для тестирования сопоставлений созданного формата и модели. Используйте файл 1099entries.xml. Данные из выбранного файла будут импортированы в систему.  

23. Щелкните "Выполнить".

    Обратите внимание, что диалоговое окно не содержит дополнительные вопросы о сопоставлении формата, который необходимо использовать для анализа импортируемого файла и последующего переноса данных в модель данных. Это происходит потому, что в данный момент существует только один формат, который использует эту модель и который будет помечен как формат, созданный для поддержки импорта данных.  
    
    Определите код ваучера для отличия импортированных проводок от других проводок, которые могли быть уже введены вручную или импортированы.  

24. В поле "Введите код ваучера" введите "IMPORT-001".

    Найдите файл "1099entries.xml".  

25. Нажмите кнопку "OК".

    Список созданных предупреждений предоставляет сведения о неверных счетах поставщиков, неверном коде налога по форме 1099, отсутствующих кодах стран и т. д. Сравните этот список предупреждений с содержимым, включенным в исполняемый XML-файл.  

26. Закройте страницу.
27. Закройте страницу.
28. Закройте страницу.
29. Закройте страницу.
30. Перейдите в раздел "Расчеты с поставщиками" > "Периодические задачи" > "Налог по форме 1099" > "Сопоставление поставщика для формы 1099".

    Эта форма показывает кумулятивные проводки в таблице Tax1099Summary, которые были созданы на основе импортированных проводок.  

31. В поле "Начальная дата" установите для даты значение "01.01.2000".
32. Щелкните "Проводки по форме 1099 вручную".

    Эта форма содержит список проводок, которые были добавлены вручную и которые были только что импортированы.  

33. Откройте фильтр столбца "Ваучер".
34. Введите значение фильтра "IMPORT-001" в поле "Ваучер" с помощью оператора фильтра "начинается с".

## <a name="review-the-relationship-between-model-and-format-mappings"></a>Проверка связи между моделью и сопоставлениями формата
1. Закройте страницу.
2. Закройте страницу.
3. Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".
4. Щелкните "Конфигурации отчетности".
5. В дереве выберите "Модель платежей по форме 1099".

    Предположим, что вам требуется поддерживать импорт тех же данных, но из формата файла TXT.   

6. Щелкните "Создать конфигурацию", чтобы открыть диалоговое окно. 
7. В поле "Создать" введите «Формат, основанный на модели данных "Модель платежей по форме 1099"».
8. В поле "Имя" введите "Импорт данных из TXT-файла".
9. Выберите "Да" в поле "Поддерживает импорт данных".
10. Нажмите Создать конфигурацию.
11. Выберите Конструктор.
12. Щелкните "Сопоставить формат модели".
13. Щелкните "Создать".
14. В поле "Определение" введите или выберите значение.

    Выберите параметр "1099-MISC".  

15. В поле "Имя" введите "Импорт данных из TXT-файла".
16. В поле "Описание" введите "Импорт данных из TXT-файла".
17. Нажмите кнопку "Сохранить".
18. Закройте страницу.
19. Закройте страницу.
20. Выберите Изменить.

    Если вы установили исправление "KB 4012871 Поддержка сопоставлений модели GER в отдельных конфигурациях с возможностью указать различные виды предварительных условий для их развертывания в различных версиях Dynamics 365 Finance" ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)), выполните следующий шаг «Включить флаг "По умолчанию для сопоставления модели"» для введенной конфигурации формата. В противном случае пропустите следующий шаг.  

21. Выберите "Да" в поле "По умолчанию для сопоставления модели".
22. В дереве выберите "Модель платежей по форме 1099".
23. Выберите Конструктор.
24. Щелкните "Сопоставить модель с источником данных".
25. Щелкните "Выполнить".

    Если на компьютере установлено исправление "KB 4012871 Поддержка немецкой модели сопоставления в отдельных конфигурациях с возможностью указать различные виды предварительных условий для развертывания их в различных версиях ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)), выберите предпочтительное сопоставление модели в поле поиска. Если вы еще не установили исправление, перейдите к следующему шагу, поскольку сопоставление уже выбрано определением конфигурации формата по умолчанию.  
    
    Если вы еще не установите исправление КБ 4012871, обратите внимание, что диалоговое окно содержит дополнительный вопрос сопоставления модели, который используется для анализа импортируемого файла. Данные затем переносятся из диалогового окна в модель данных. В настоящее время можно выбрать, какое сопоставление формата необходимо использовать в зависимости от типа файла, который планируется импортировать.  
    
    Если планируется вызывать это сопоставление модели с точки в приложении, специально предназначенной для этого действия, место назначения ER и сопоставление формата должны быть помечены как часть интеграции.  

26. Щелкните "Отмена".
27. Закройте страницу.
28. Закройте страницу.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
