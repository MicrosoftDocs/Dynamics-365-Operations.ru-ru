---
title: Налоговые регистры для задолженности расчетов с поставщиками и списание задолженностей
description: В этой статье приводятся сведения о налоговых регистрах для задолженности по расчетам с поставщиками и о списании задолженностей.
author: AdamTrukawka
ms.date: 04/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: atrukawk
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b8f696b73bcb85c00d0356d7391300473ea05725
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292209"
---
# <a name="accounts-payable-debt-tax-registers-and-debt-write-offs"></a>Налоговые регистры для задолженности расчетов с поставщиками и списание задолженностей

[!include [banner](../includes/banner.md)]


В этой статье приводятся сведения о сомнительных долгах в рамках расчетов с поставщиками, списании задолженностей по ним и о следующих налоговых регистрах:
-   Кред. задолженность - инвентаризация
-   Движение модуля "Расчеты с поставщиками"

Расчеты с поставщиками формируются на основе неоплаченных накладных для покупок товаров и услуг, а при авансовых платежах, полученных от клиентов.

Суммы по расчетам с поставщиками, списанные в связи с истечением периода ограничения, считаются доходами от неосновной деятельности.

## <a name="setup"></a>Настройка

### <a name="set-up-accounts-payable-parameters"></a>Настройте параметры "Расчетов с поставщиками"

1. Перейдите в раздел **Расчеты с поставщиками** > **Настройка** > **Параметры расчетов с поставщиками**.
2. На вкладке **Главная книга и налог** на экспресс-вкладке **Кредиторская задолженность** в поле **Код дохода** укажите код дохода, который необходимо назначить проводкам для списания сомнительной задолженности по расчетам с поставщиками.
3. В поле **счет ГК** укажите счет для доходов от неосновной деятельности.

    ![Параметры модуля ""Расчеты с поставщиками", вкладка "Главная книга и налог".](media/1-AP_tax.png)

4. На вкладке **Номерные серии** в поле **Код номерной серии** выберите код номерной серии для ссылки **Ваучер ГК для амортизации задолженностей**.

### <a name="set-up-the-debt-interval-for-hopeless-debts"></a>Настройка интервала задолженности для безнадежных долгов

1. Перейти к **Расчеты с поставщиками** > **Настройка** > **Интервал задолженности**.
2. В поле **С** введите нижний предел интервала задолженности, в днях. Например, введите **240**.
3. В поле **По** введите верхний предел интервала задолженности, в днях. Например, введите **0**, если верхний предел отсутствует.
4. В поле **Описание** введите подробное описание интервала задолженности.

    ![Интервалы кредиторской задолженности.](media/2-AP_tax.png)

## <a name="tax-registers"></a>Регистры налогового учета

Необходимо создать и настроить налоговые регистры. Дополнительные сведения см. в разделе [Создание налоговых регистров и журнала налоговых регистров](rus-profit-tax-registers.md#create-a-tax-register). В следующих разделах приведены дополнительные сведения о каждом из налоговых регистров.

### <a name="accounts-payable-inventory-act-tax-register"></a>Налоговый регистр акта учета запасов для расчетов с поставщиками

Налоговый регистр **акта запасов для расчетов с поставщиками** основан на запасах счетов по состоянию на дату отчета. Он отражает существование сумм расчетов с поставщиками.

Регистр требуется для учета доходов от неосновной деятельности и расходов для отчетного (налогового) периода.

   ![Страница акта учета запасов для расчетов с поставщиками.](media/3-AP_tax.png)

Строки регистра также отображают следующую информацию:

- **Объект учета**: номер накладной поставщика или номер полученного авансового платежа клиента.
- **Дата проводки**: дата накладной или авансового платежа.
- **Крайний срок**: дата выполнения платежа в соответствии с условиями оплаты.
- **Задолженность**: неоплаченная сумма по накладной или авансовый платеж, который был получен на дату запасов, если период распределения по срокам оплаты находится в пределах интервала задолженности, настроенного ранее.
- **Сумма НДС для задолженности**: сумма налога на добавленную стоимость (НДС) по неоплаченным расчетам с поставщиками на дату запасов.
- **Закрытая сумма**: общая сумма расчетов с поставщиками, которая была списана в течение отчетного (налогового) периода.
- **Закрытая сумма НДС**: общая сумма НДС для расчетов с поставщиками, которая была списана в течение отчетного (налогового) периода.
- **Не подтвержденная задолженность**: введите сумму неподтвержденной задолженности по поставщику.

### <a name="accounts-payable-movement-tax-register"></a>Налоговый регистр движения средств при расчетах с поставщиками

Налоговый регистр **Движение средств при расчетах с поставщиками** сформирован для суммирования информации об операциях по движению средств при расчетах с поставщиками.

В регистр вносятся записи о всех вхождениях расчетов с поставщиками, и все возвраты денежных средств (полные или частичные) и их списание по налогоплательщику между началом налогового периода и датой отчетности.

Этот регистр не соответствует суммам расчетов с поставщиками налогоплательщика в бюджетах других уровней.

В целях отчетности записи по проводкам в иностранной валюте также создаются для каждого факта о переоценке задолженности.

   ![Страница Движение средств при расчете с поставщиками.](media/4-AP_tax.png)

Строки регистра также отображают следующую информацию:

- **Объект учета**: номер накладной поставщика или номер полученного авансового платежа клиента.
- **Дата проводки**: дата накладной или авансового платежа.
- **Описание проводки**: описание документа.
- **Крайний срок**: дата выполнения платежа в соответствии с условиями оплаты.
- **Порядок учета**: условия оплаты накладной.
- **Задолженность**: неоплаченная сумма по накладной или авансовый платеж, который был получен на дату запасов, если период распределения по срокам оплаты находится в пределах интервала задолженности, настроенного ранее.
- **Сумма НДС для задолженности**: сумма НДС по неоплаченным расчетам с поставщиками.
- **Дата закрытия**: дата закрытия накладной, списания или проводки платежа.
- **Причина закрытия**: описание проводки для списания или выплаты задолженности.
- **Сумма закрытия**: общая сумма списанных расчетов с поставщиками для отчетного (налогового) периода.
- **Закрытая сумма НДС**: общая сумма НДС для расчетов с поставщиками, которая была списана для отчетного (налогового) периода.
- **Сумма непогашенной задолженности**: общая сумма неоплаченных расчетов с поставщиками после движения средств.
- **Сумма НДС по непогашенной задолженности**: общая сумма НДС по неоплаченным расчетам с поставщиками после движения средств.

## <a name="write-off-hopeless-debts"></a>Списание безнадежных задолженностей

Прежде чем можно будет списать безнадежные задолженности, необходимо создать журнал регистров для того же периода, что и списание, и рассчитать регистры.

В журнале следует утвердить регистр **акт учета запасов для расчетов с поставщиками**.

> [!NOTE]
> Не утверждайте регистр **Движение средств при расчете с поставщиками**.

### <a name="recognize-and-write-off-hopeless-debt"></a>Распознавание и списание безнадежной задолженности

1. Расчет и утверждение журнала налоговых регистров для предыдущего периода. Дополнительные сведения см. в разделе [Создание налоговых регистров и журнала налоговых регистров](rus-profit-tax-registers.md#create-and-work-with-a-tax-register-journal).
2. Переход к **Расчеты с поставщиками** > **Периодические задачи** > **Амортизация** > **Амортизация кредиторской задолженности**.
3. В поле **Дата расчета** выберите дату, которая указывает необходимый расчетный период.

    На странице отображаются задолженности, срок действия которых истек на указанную дату отчета:

    -   На вкладке **Клиенты** отображается список предоплат клиентов.
    -   На вкладке **Поставщики** отображается список накладных поставщиков.

4. Для просмотра исходных проводок клиента или поставщика выберите **проводки** на соответствующей вкладке.
5. Выбор долгов для списания. В поле **Итого** в разделе **Отмечено** отображается общая сумма проводок, помеченных для дебета.

    ![Страница журнала отмены задолженностей кредиторов, Поле "Итого".](media/5-AP_tax.png)

6. На панели операций выберите **Обновление**. Помеченные проводки больше не отображаются. В разделе **Списано** суммы увеличиваются до значения, которое отображалось в поле **Итого** в разделе **Отмечено** до того, как было выбрано **Обновление**. Создаются проводки для клиентов/поставщиков. Кроме того, в главной книге создаются проводки для списания каждой задолженности. Дата операций списания соответствует дате, выбранной в поле **Дата расчета**.

    ![Страница журнала отмены задолженностей кредиторов, Поле "Дата расчета".](media/6-AP_tax.png)

### <a name="cancel-the-write-off-of-hopeless-debt"></a>Отмена списания безнадежной задолженности

Чтобы отменить списание безнадежной задолженности, выполните следующие действия.

1. Переход к **Расчеты с поставщиками** > **Периодические задачи** > **Амортизация** > **Отмена амортизации кредиторской задолженности**.
2. В поле **Дата расчета** выберите дату, которая указывает необходимый расчетный период.

    На странице отображаются списанные задолженности, срок действия которых истек на указанную дату отчета:

    - На вкладке **Клиенты** отображается список списанных предоплат клиентов.
    - На вкладке **Поставщики** отображается список списанных накладных поставщиков.

3. Для просмотра исходных проводок клиента или поставщика выберите **проводки** на соответствующей вкладке.
4. Выбрать списанные задолженности для отмены. В поле **Итого** в разделе **Отмечено** отображается общая сумма проводок, помеченных для дебета.

    ![Страница журнала отмены амортизации кредиторской задолженности.](media/7-AP_tax.png)

5. На панели операций выберите **Обновление**. Помеченные проводки больше не отображаются. В разделе **Списано** суммы уменьшаются до значения, которое отображалось в поле **Итого** в разделе **Отмечено** до того, как было выбрано **Обновление**. Создаются проводки, отменяющие списание расчетов с поставщиками.
