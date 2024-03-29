---
title: Создание налоговых регистров и журнала налоговых регистров
description: В этой статье приводятся сведения о создании налоговых регистров и журнала налоговых регистров.
author: AdamTrukawka
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: atrukawk
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: fc88029123e86f24386aee51f7d931a9818193f4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272937"
---
# <a name="create-tax-registers-and-the-tax-register-journal"></a>Создание налоговых регистров и журнала налоговых регистров

[!include [banner](../includes/banner.md)] 

Для организации учета прибыли для организации в России рекомендуется система, состоящая из списка налоговых регистров. Налоговые регистры отслеживают типы доходов и расходов для организации, начиная с момента расчета основных документов (накладных и фактур) до того момента, когда рассчитываются затраты на себестоимость готовой продукции. Данные в налоговых регистрах используются для подтверждения объявленной суммы прибыли организации.

Следующие модули являются источниками данных для налоговых регистров:

- **Основные средства (Россия)**
- **Управление запасами**
- **Управление производством**
- **Главная книга**
- **Расчеты с поставщиками**
- **Расчеты с клиентами**

Существуют следующие типы налоговых регистров:

- **Налоговые регистры первого уровня или налоговые регистры "операции"**: эти регистры создаются на основе операций (проводок) в системе.
- **Налоговые регистры второго уровня**: эти регистры используют результаты налоговых регистров ("операции") первого уровня.
- **Результирующие налоговые регистры**: эти регистры используют данные из налоговых регистров второго уровня.

Структура данных каждого налогового регистра почти уникальна.

Результаты расчета регистров связаны со значением **Код расходов и доходов**.

В системе налоговые регистры группируются в соответствии со сведениями, указанными в них:

- **Налоговые регистры промежуточных расчетов**: эти налоговые регистры отображают и сохраняют результаты промежуточных расчетов. Данные из этих налоговых регистров не имеют соответствующих строк в налоговой декларации. Результаты используются для результирующих налоговых регистров.
- **Налоговые регистры статуса объекта налогового учета**: эти налоговые регистры отображают сведения о статусе объектов налогового учета для каждой даты отчетности и изменения этого статуса.
- **Налоговые регистры для создания данных отчетности**: эти налоговые регистры отображают значения, которые могут быть перенесены в отдельные строки налоговой декларации.

## <a name="available-tax-registers"></a>Доступные налоговые регистры

В следующей таблице показан полный список доступных налоговых регистров, сгруппированных по типу налоговых регистров.

**Налоговые регистры промежуточных расчетов**

| Тип налогового регистра | Комментарий |
|-------------------------|-------------------------|
| - Расчет по временным налоговым разницам</br>- Расчет по временным налоговым разницам по методу остатка | Эти налоговые регистры рассчитывают временные налоговые разницы. |
| - Расчет по постоянным налоговым разницам</br>- Расчет по постоянным налоговым разницам по методу остатка | Эти налоговые регистры рассчитывают постоянные налоговые разницы. |
| - Акт инвентаризации дебиторской задолженности</br>- Деб. задолженность — инвентаризация (бухгалтерский учет) | Эти налоговые регистры соответствуют сальдо расчетов с клиентами в конце отчетного периода. |
| - Деб. задолженность — проводка</br>- Деб. задолженность — движение (бухгалтерский учет) | Эти налоговые регистры обобщают сведения об операциях для перемещения дебиторской задолженности. |
| - Деб. задолженность — проводка резервов</br>- Деб. задолженность — движение резерва (бухгалтерский учет)</br>- Деб. задолженность — детальное движение резерва</br>- Деб. задолженность — детальное движение резерва</br>(бухгалтерский учет) | Эти налоговые регистры обобщают сведения о перемещении и использовании резерва для сомнительных долгов. |
| - Деб. задолженность — резервы</br>- Деб. задолженность - резервы (бухгалтерский учет)</br>- Деб. задолженность - детальный расчет резервов</br>- Деб. задолженность - детальный расчет резервов (бухгалтерский учет) | Эти налоговые регистры соответствуют сумме резерва, рассчитанной для текущего отчетного периода. Этот резерв будет использоваться для списания безнадежных задолженностей позже. |
| Денежные средства - поступление | Этот налоговый регистр поступления денежных средств консолидирует информацию о поступлении денежных средств для определения дохода, который связан с текущими и будущими периодами, или проводок, определяющих будущие расходы. |
| Денежные средства - расход | Этот налоговый регистр расхода денежных средств консолидирует информацию о расходе денежных средств для определения расходов, которые связаны с текущими и будущими периодами, или проводок, определяющих будущие доходы. |
| Движение модуля "Расчеты с поставщиками" | Этот налоговый регистр обобщает сведения об операциях для перемещения расчетов с поставщиками.</br>В регистр вносятся записи о всех фактах появления расчетов с поставщиками, и все возвраты денежных средств (полные или частичные) и их списание по налогоплательщику между началом налогового периода и датой отчетности. |
| Кред. задолженность - инвентаризация | Этот налоговый регистр основан на запасах счетов по состоянию на дату отчета. Оно отражает существование сумм расчетов с поставщиками, которые могут быть списанными. Например, суммы могут быть списаны, так как срок действия законодательных ограничений истек. |
| НМА - амортизация | Этот налоговый регистр определяет сумму амортизации для нематериальных активов. Сумма амортизации включена в косвенные затраты, которые распознаются в текущем налоговом периоде для целей налогообложения. |
| НМА - амортизация (нелинейный метод) | Этот налоговый регистр рассчитывает амортизацию нематериальных активов с помощью нелинейного метода налога. |
| Нормируемые расходы - коэфф. буд. периодов | Этот налоговый регистр содержит результаты расчетов норм в отложенных периодах. |
| Нормируемые расходы - коэфф. тек. периода | Этот налоговый регистр содержит результаты расчетов норм в текущем периоде. |
| Нормируемые расходы тек. периода | В этом налоговом регистре отображается сумма амортизации для каждого объекта. Здесь также отображается общая сумма амортизации, включенная в прямые или косвенные затраты. |
| Доходы и расходы, не влияющие на налоговую базу | Это налоговый регистр содержит информацию о доходах и расходах, которые не влияют на базу налога. Эти сведения используются, когда рассчитываются регистры постоянных налоговых разниц. |
| ОС и НМА - реализация | Этот налоговый регистр используется для следующих целей:</br><ul></br><li>Общая информация о продажах амортизируемого имущества.</li></br><li>Создание суммы убытков, вызываемой при продаже амортизируемого имущества и признанных РБП для целей налогообложения.</li></br></ul> |
| Восстановление амортизационной премии | В этом налоговом регистре отображаются данные о проводках восстановления амортизационной премии для основных средств, если выполняются следующие условия:</br><ul></br><li>Основное средство было помещено в эксплуатацию после 1 января 2008.</li></br><li>Операция выбытия (продажи) была выполнена для основного средства.</li></br><li>Между датой ввода в эксплуатацию и датой выбытия основного средства прошло менее пяти лет.</li></br><li>Основное средство было продано аффилированному клиенту.</li></br></ul> |
| ОС - амортизация | Этот налоговый регистр определяет сумму амортизации для основных средств. Сумма амортизации требуется для создания прямых расходов и других расходов, которые распознаются в текущем налоговом периоде для целей налогообложения. В регистре отображается сумма амортизации для каждого объекта. Здесь также отображается общая сумма амортизации, включенная в прямые или косвенные затраты. |
| ОС - амортизация (нелинейный метод) | Этот налоговый регистр рассчитывает амортизацию основных средств с помощью нелинейного метода налога. |
| Расходы по налогам | Этот налоговый регистр содержит все налоги и пошлины, сгруппированные по типу налогов. |
| Формир. стоимости объекта учета | Этот налоговый регистр создает затраты на объект учета (то есть, основное средство или нематериальный актив). |
| Оценка НЗП и ГП в налоговом учете | Этот налоговый регистр используется для оценки сальдо незавершенного производства (НЗП) и готовой продукции. |
| Распределение прибыли по отдельным подразделениям | Этот налоговый регистр рассчитывает сумму распределения прибыли для отдельных подразделений. |
| Курсовая разница в бухгалтерском учете | Этот налоговый регистр устарел. |
| Курсовая разница в налоговом учете | Этот налоговый регистр устарел. |
| Суммовая разница в налоговом учете | Этот налоговый регистр устарел. |

**Налоговые регистры статуса объекта налогового учета**

| Тип налогового регистра | Комментарий |
|-------------------------|-------------------------|
| ОC — информация об объекте | Этот налоговый регистр используется для сбора сведений о существовании и перемещении собственности, принадлежащей организации и учитываемой для целей налогообложения как основных средств в качестве амортизируемого имущества. |
| НМА — информация об объекте | Этот налоговый регистр используется для сбора сведений о существовании и перемещении собственности, принадлежащей организации и учитываемой для целей налогообложения как нематериальных активов в качестве амортизируемого имущества. |
| РБП | Этот налоговый регистр суммирует информацию о расходах, которые могут быть включены в расходы для целей налогообложения в будущих периодах. Эти расходы называются расходами будущих периодов. |

**Налоговые регистры для создания данных отчетности**

| Тип налогового регистра | Комментарий |
|-------------------------|-------------------------|
| Имущество - выбытие | Этот налоговый регистр суммирует информацию о доходе от выбытия собственности налогоплательщика, продажи работ, услуг и прав и формирования сумм соответствующего дохода от продаж, включенных в налоговую базу. |
| Доходы текущего периода | Этот налоговый регистр содержит сведения об операциях выручки, которые используются для отслеживания выручки за указанный отчетный период. Отслеживаемая выручка включает нереализованную выручку. Регистр используется, когда рассчитываются налоги на объявленную прибыль. |
| Расходы прочие реализ. | Этот налоговый регистр показывает общую сумму других расходов, которые распознаются как другие расходы текущего периода, расходы будущих периодов, которые учитываются в налоговый период, и суммы соответствующих типов других расходов на основе данных аналитического учета соответствующих типов расходов. |
| Расходы внереализационные | Этот налоговый регистр используется для расчета нереализованных расходов, которые создаются в течение периода налоговой отчетности. Регистр рассчитывается в конце учетного периода на основе расходов, начисленных с начала налогового периода и до даты формирования отчетности. Записи, регистрируемые для каждой категории нереализованных расходов, получаются из данных налоговых регистров в конце отчетного периода. |
| Расходы прочие внереализационные | Этот налоговый регистр отображает сумму без налога и сумму налога на основе проводок главной книги или расходов, введенных вручную в регистр. |
| Имущество - не складируемое | Этот налоговый регистр отображает информацию о перемещении номенклатур, работ, услуг и прав, которые списаны при фактических затратах. Предполагается, что это свойство не связано с главной деятельностью компании. Вместо этого приобретение является общим экономическим расходом и принимается для налогового учета в период, когда были сделаны расходы. |
| Имущество - складируемое | Этот налоговый регистр содержит следующую информацию:</br><ul></br><li>Перемещение сырья и других материалов в производство</li></br><li>Накладные для продажи сырья и других материалов</li></br><li>Номенклатуры, возвращаемые поставщику</li></br><li>Списания номенклатур</li></br></ul> |
| Имущество - складируемое (итоги) | Этот налоговый регистр отображает общую сумму каждого типа дохода или расхода, основанную на чеках в регистре **Складируемое имущество**. |

Набор налоговых регистров, которые должны быть введены для отчетного периода, создается в журнале налоговых регистров. Каждый журнал налоговых регистров состоит из строк, которые соответствуют статусу расчета отдельных регистров для выбранного периода.

## <a name="create-a-tax-register"></a>Создание налогового регистра

1. Перейдите **Налог** > **Настройка** > **Налог на прибыль** > **Регистры**.
2. Выберите **создать**, чтобы создать налоговый регистр, и установите следующие поля:

    - **Тип регистра**: выберите тип налогового регистра.
    - **Код регистрации**: введите уникальный код налогового регистра.
    - **Типы периодов**: выберите частоту создания налоговых регистров.

3. На экспресс-вкладке **Скрыть** переместите поля, которые необходимо скрыть, из столбца **Доступные поля** в столбец **Выбранные поля**, а затем установите флажок **Скрыть** для этих полей.

    При создании новых строк в журналах налогового регистра скрытые поля автоматически исключаются из налогового реестра.
    Список полей, включенных в расчет строк регистра, для каждого налогового регистра можно изменить в строках налогового регистра.
    При изменении списка скрытых полей эти поля будут сохранены для всех данных, созданных до внесения этих изменений.

4. На экспресс-вкладке **Параметры** можно настроить дополнительные параметры для налогового регистра. В строке для каждого параметра укажите значение в поле **Значение**. Параметры для каждого регистра отличаются. Дополнительные сведения о параметрах см. в статье для каждого налогового регистра.

    ![Регистры налогового учета](media/rus-profit-tax-1.png)

### <a name="set-up-expense-and-income-codes-for-the-tax-register"></a>Настройка кодов расходов и доходов для налогового регистра

Для некоторых налоговых регистров необходимо определить, какие коды расходов и доходов формируют информацию в налоговом регистре.

1. На странице **Налоговые регистры** в левой области выберите налоговый регистр. Затем в области действий выберите **Коды расходов**, чтобы настроить коды расходов и коды доходов для налогового регистра.
2. На странице **Настройка кода расходов** в левой области выберите код расхода или дохода или создайте новую строку.
3. В поле **Код расхода** выберите код расхода или дохода, используемый для записей по счету, которые должны быть перенесены в налоговый регистр.
4. В поле **Имя условия** введите имя кода расхода.
5. На экспресс-вкладке **Настройка** настройте параметр **Тип** и поле **Тип основных средств**. Дополнительные сведения см. в разделе [Регистры основных средств и нематериальных активов](rus-assets-tax-registers.md).
6.  На экспресс-вкладках **Исключения** и **Аналитика исключений** укажите счета ГК, аналитики и записи, которые должны быть исключены при расчете налогового регистра.

    ![Настройка кодов расходов](media/rus-profit-tax-2.png)

### <a name="view-the-tax-registers-tree"></a>Просмотр дерева налоговых регистров

1. На странице **Налоговые регистры** в левой области выберите налоговый регистр. 
2. В области действий выберите **Дерево** для просмотра структуры дерева налоговых регистров.

    Ниже приводится пример древовидной структуры для налоговых регистров:
    
    - Денежные средства - поступление
    - Денежные средства - расход
    - **Формир. стоимости объекта учета**
        - **Имущество - складируемое (итоги)**
            - Имущество - складируемое
        - **ОС и НМА - реализация**
            - ОC — информация об объекте

Древовидная структура показывает, что некоторые налоговые регистры рассчитываются с помощью данных из других налоговых регистров. Полужирный текст указывает налоговые регистры, которые существуют в системе и настраиваются на странице **Налоговые регистры**. Обычный текст указывает налоговые регистры, которые существуют в системе, но не настраиваются для расчета на странице **Налоговые регистры**.

## <a name="create-and-work-with-a-tax-register-journal"></a>Создание и работа с журналом налоговых регистров

### <a name="create-a-tax-register-journal"></a>Создание новый журнала налогового регистра

Можно создать новый журнал регистров налогового учета, только если были утверждены все журналы за предыдущие периоды.

1. Перейдите **Налог** > **Записи журнала** > **Журналу налогового регистра**. На странице отображается список уже созданных журналов налоговых регистров.
2. В области действий выберите **Создать**.
3. В диалоговом окне **Новый журнал регистров** в разделе **Период отчетности** настройте следующие поля:

    - Типы периодов
    - Номер периода
    - Годы

    ![Новый журнал налоговых регистров](media/rus-profit-tax-3.png)

4. В области действий выберите **Строки**, а затем выберите **Да**, чтобы утвердить создание строк журнала налоговых регистров. Откроется страница **Строки журнала регистра**.

Строки журнала содержат налоговые регистры, в которых расчетный период совпадает с типом периода журнала или меньше него. Налоговые регистры, в которых расчетный период больше типа периода журнала, исключается из расчета. Например, если период журнала регистров — **Квартал**, строки журнала будут содержать налоговые регистры, имеющие периоды **Месяц** и **Квартал**. Однако он не будет содержать налоговые регистры с периодом **Ежегодно**.

### <a name="change-the-register-fields"></a>Изменение полей регистра

Параметры отображения полей загружаются из настроек регистра, но список скрытых полей можно настроить в журнале налоговых регистров.

Чтобы скрыть поле, выполните следующие действия.

1. На странице **Строки журнала регистров** выберите строку регистра.
2. На вкладке **Скрыть** выберите **добавить**, чтобы добавить строку.
3. В поле **Поле регистра** выберите поле, которое требуется скрыть, а затем установите флажок **Скрыть**. Для выбора доступны только поля, выбранные в соответствующих параметрах регистра.
4. Нажмите **Сохранить**.

    ![Изменение полей](media/rus-profit-tax-4.png)

Чтобы добавить поле, выполните следующие действия.

1. На странице **Строки журнала регистров** выберите заголовок столбца, а затем выберите **Вставить столбцы**.
2. В диалоговом окне **Вставка столбцов** в столбце **Выбор** выберите поля, которые требуется добавить.
3. Выберите **Обновить**.

### <a name="update-the-tax-register-journal"></a>Обновление журнала налогового регистра

Если состав журнала регистров налогового учета изменен, выполните следующие шаги, чтобы обновить его строки. Состав может измениться, если, например, создается новый регистр после того, как журнал уже был создан.

1. Перейдите **Налог** > **Записи журнала** > **Журналу налогового регистра**.
2. На панели действий выберите **Строки**.
3. На панели операций выберите **Удалит строки**, затем выберите **Да**.

    > [!NOTE] 
    > Невозможно удалить строки журнала регистров, если существуют утвержденные регистры. Чтобы удалить строки, необходимо сначала отменить утверждение регистров.

4. Закройте страницу **Строки журнала регистра**.
5. На панели операций выберите **Строки** для создания нового набора строк.

### <a name="calculate-and-print-tax-registers"></a>Расчет и печать налоговых регистров

1. Перейдите **Налог** > **Записи журнала** > **Журналу налогового регистра**.
2. На панели действий выберите **Строки**.
3. Чтобы рассчитать все регистры, на панели действий выберите **Рассчитать все**.

    Или, чтобы рассчитать только один налоговый регистр, выберите строку для регистра, а затем на панели операций выберите **Рассчитать текущий**. Если регистр использует данные из других регистров, сначала следует рассчитать эти регистры.

4. Нажмите **ОК**. По окончании расчета создаются строки регистра.
5. На странице **Строки журнала регистров** выберите строку регистра.
6. В области действий выберите **Печать**. Затем в появившемся диалоговом окне выберите **ОК**. Регистр печатается в формате Microsoft Excel.

    Здесь пример налогового регистра, который напечатан.

    ![Пример Excel](media/rus-profit-tax-5.png)

### <a name="recalculate-tax-registers"></a>Перерасчет налоговых регистров

Для пересчета налоговых регистров выполните следующие действия.

1. Перейдите **Налог** > **Записи журнала** > **Журналу налогового регистра**.
2. На панели действий выберите **Строки**.
3. На панели операций выберите **Сбросить статус**, чтобы сбросить все налоговые регистры, а затем нажмите кнопку **ОК**.

    Или, чтобы сбросить только один регистр, выберите строку для регистра, а затем на панели операций выберите **Изменить**. В поле **Статус** выберите **Не рассчитано**. Если данные из регистра используются в других регистрах, эти регистры также сбрасываются.

4. Рассчитайте налоговые регистры, как описано в предыдущем разделе.

### <a name="view-and-print-the-register-lines"></a>Просмотр и печать строк регистра

1. На странице **Строки журнала регистров** выберите строку регистра, а затем на панели операций выберите **Строки регистра**, чтобы просмотреть строки налогового регистра. Содержимое и список столбцов различаются для каждого налогового регистра. Для получения дополнительных сведений см. статью для каждого регистра.
2. Чтобы просмотреть все строки или только последнюю строку, выберите **Развернуть/свернуть узел**.
3. Перейдите на вкладку **Общие**, чтобы просмотреть следующие сведения о выбранной строке:

    - **Код расхода** – код расхода строки, к которому относится строка регистра.
    - **Тип строки** — это поле может содержать следующие значения:

         - **Заголовок**: строка заголовка.
         - **Текст**: строка регистра.
         - **Нижний колонтитул**: строка "общее".

    - **Номер строки**
    - **Описание** – описание строки регистра. Для типов строк **Заголовок** и **Нижний колонтитул** это поле устанавливается автоматически. Для типа строки **Текст** поле доступно для редактирования.
    - **Ввод данных вручную**: этот параметр устанавливается в значение **Да**, если строка была создана вручную. Этот параметр не может редактироваться.
    - **Исправлено**: для этого параметра устанавливается значение **Да**, если строка была изменена вручную. Этот параметр не может редактироваться.

    ![Строки регистра](media/rus-profit-tax-6.png)

4. На панели операций выберите **Источник**, чтобы перейти к первичному документу, на котором была основана строка при ее создании. В зависимости от налогового регистра первичный документ может быть, например, карточкой ОС или разнесенной накладной поставщика или клиента. Кнопка **Источник** недоступна, если строка регистра была создана путем суммирования проводок.
5. Для печати налогового регистра на панели действий выберите **Печать**. Регистр печатается в формате Excel.

### <a name="manually-adjust-the-tax-register-lines"></a>Вручную скорректируйте строки налоговых регистров

Автоматически созданные строки регистра можно изменить или удалить вручную. Строки также могут быть добавлены вручную в регистр. Однако строки могут быть добавлены или изменены только для рассчитанных налоговых регистров.

#### <a name="edit-the-register-lines"></a>Редактирование строк регистра

- На странице **Строки регистра** в области действий выберите **Правка**.
- Измените требуемые строки, а затем на панели операций выберите **Сохранить**.
- На вкладке **Общие** обратите внимание, что параметр **Исправлено** имеет значение **Да**.

#### <a name="delete-a-register-line"></a>Удаление строки регистра

- На странице **Строки регистра** выберите строку, а затем на панели операций выберите **Удалить**.

Чтобы восстановить строку после ее удаления, необходимо пересчитать налоговый регистр.

#### <a name="manually-add-a-line-to-the-tax-register"></a>Вручную добавьте строку в налоговый регистр

1. На странице **Строки регистра** в области действий выберите **Создать**.
2. Задайте поля для новой строки и затем на панели операций выберите **Сохранить**.
3. На вкладке **Общие** обратите внимание, что параметр **Ввод данных вручную** имеет значение **Да**.

### <a name="approve-the-tax-registers"></a>Утверждение налоговых регистров

После расчета всех налоговых регистров и просмотра данных регистры должны быть утверждены. При утверждении всех рассчитанных налоговых регистров журнал налогового регистра автоматически устанавливает флажок **Утверждено**. Журнал налоговых регистров утверждается автоматически, если все включенные в него налоговые регистры утверждены.

1. Чтобы утвердить налоговый регистр, на странице **Строки журнала регистров** на панели операций выберите **Изменить**.
2. Установите флажок **Утверждено**, а затем в поле **Работник** выберите пользователя, утвердившего регистр.

Чтобы отменить утверждение регистра, снимите флажок **Утверждено**. Поле **Работник** автоматически очищается.

### <a name="print-the-tax-register-by-using-the-register-lines-report"></a>Печать налогового регистра с помощью отчета строк регистра

1. Перейдите **Налог** > **Запросы и отчеты** > **Налоговые отчеты** > **Строки регистра**.
2. В диалоговом окне **Строки регистра** в разделе **По умолчанию** определите критерии для выбора налогового регистра для отчета. Значения должны соответствовать друг другу. В противном случае регистр печататься не будет.
3. Нажмите **ОК**. Налоговый регистр печатается в формате Excel.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
