---
title: Настройка анализа новизны, частоты и денежных средств (RFM)
description: В этой статье описывается, как настроить анализ RFM (новизна, частота и денежные средства) клиентов.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRRFMDefinition
audience: Application User
ms.reviewer: josaw
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 153759ac6b70235b79c080e934819536c2861371
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850179"
---
# <a name="set-up-recency-frequency-and-monetary-rfm-analysis"></a>Настройка анализа новизны, частоты и денежных средств (RFM)

[!include [banner](includes/banner.md)]

В этой статье описывается, как настроить анализ RFM (новизна, частота и денежные средства) клиентов.

Анализ RFM (давность, частота, деньги) — это маркетинговый инструмент, который организация может использовать для оценки данных по покупкам клиентов. После настройки анализа RFM клиенты назначаются рассчитанному баллу RFM по мере совершения покупок. Балл RFM может быть трехзначной оценкой или общим числом в зависимости от настроек анализа RFM в организации. Ниже указано, как работает оценка, если ваша организация использует трехзначную оценку для балла:

- Первая цифра — это оценка давности клиента, т. е. как давно клиент делал покупку у вашей организации.
- Вторая цифра — это частота клиента, т. е. как часто клиент делает покупки у вашей организации.
- Третья цифра — это денежный рейтинг клиента, т. е. сколько тратит клиент, делая покупки у вашей организации.

Например, ваша организация установила рейтинги по шкале от 1 до 5, где 5 — наивысший рейтинг. В этом случае рейтинг клиента 535 говорит вам о клиенте следующее:

- **Рейтинг давности 5** — клиент сделал покупку недавно.
- **Рейтинг частоты 3** — клиент приобретает продукты в организации достаточно часто.
- **Денежный рейтинг 5** — когда клиент совершает покупку, клиент тратит на нее значительные денежные средства.

Если в вашей организации используется совокупный балл, отдельные рейтинги складываются. В примере выше у клиента будет рейтинг 13 (5 + 3 + 5).

## <a name="set-up-rfm-analysis-for-the-customers-in-your-organization"></a>Настройка анализа RFM для клиентов в вашей организации

1. Выберите **Центр обработки вызовов** \> **Периодические операции** \> **RFM-анализ**.
2. На странице **RFM-анализ** выберите **Создать**. В поле **Определение RFM** введите имя определения RFM. Например, можно использовать определение RFM-A.
3. Введите дату начала и окончания срока действия определения RFM.
4. На экспресс-вкладке **Общие** выполните следующие действия:

    - Если в каждом разделе балла RFM должно быть одинаковое количество клиентов, установите флажок **Равномерное распределение**.
    - Установите флажок **Добавить оценки** для использования суммы трех баллов. Например, в этом случае клиент с баллом RFM 535 имел бы балл 13.
    - Установите флажок **Сохранить историю**, чтобы система сохраняло статистические данные по клиентам, чтобы их можно было использовать для расчета балла RFM.

5. На экспресс-вкладке **Новизна** выполните следующие действия:

    - В поле **Подразделения** введите количество подразделений или групп, которые будут использоваться для расчета балла новизны для клиентов. Например, если имеется 100 клиентов, подразделение 5 означает, что для каждого балла предусмотрено 20 клиентов. 20 клиентов, которые сделали покупки последними, имеют балл давности 5. Следующие 20 клиентов имеют балл давности 4 и т. д. При наличии 50 клиентов балл новизны 10 клиентов будет равен 5, следующих 10 клиентов — 4 и т. д.
    - В поле **Приоритет** выберите приоритет параметра новизны по отношению к другим параметрам при расчете балла RFM для клиента. Например, баллу новизны можно назначить более высокий приоритет по сравнению с баллом денежных средств.
    - В поле **Множитель** введите значение, на которое необходимо умножить балл новизны. Если значение не введено, балл не будет умножаться.
    - В поле **Период** введите период времени, за который рассчитывается балл новизны. Например, за неделю или за месяц.

6. На экспресс-вкладке **Частота** выполните следующие действия:

    - В поле **Подразделения** введите количество подразделений или групп, которые будут использоваться для расчета балла частоты для клиентов.
    - В поле **Приоритет** выберите приоритет параметра частоты по отношению к другим параметрам при расчете балла RFM для клиента.
    - В поле **Множитель** введите значение, на которое необходимо умножить балл частоты. Если значение не введено, балл не будет умножаться.

7. На экспресс-вкладке **Денежный** выполните следующие действия:

    - В поле **Подразделения** введите количество подразделений или групп, которые будут использоваться для расчета денежного балла для клиентов.
    - В поле **Приоритет** выберите приоритет денежного параметра по отношению к другим параметрам при расчете балла RFM для клиента.
    - В поле **Множитель** введите значение, на которое необходимо умножить денежный балл. Если значение не введено, балл не будет умножаться.
    - В поле **Брутто/нетто** выберите, следует ли рассчитывать балл денежных средств клиента с помощью валовой или чистой суммы.
    - Если суммы возврата клиента следует вычитать из общего расчета по накладной клиента, установите флажок **Вычесть возвраты**.

## <a name="view-a-customers-rfm-score"></a>Просмотр балла RFM клиента

Эта процедура используется для просмотра балла RFM клиента.

1. Выберите **Центр обработки вызовов** \> **Журналы** \> **Обслуживание клиентов**.
2. На странице **Обслуживание клиентов** в области **Обслуживание клиентов** в полях поиска выберите тип ключевого слова для поиска и введите искомый текст.
3. Выберите **Поиск**.
4. На странице **Поиск клиента** выберите требуемую запись клиента, затем щелкните **Выбрать клиента**.

Балл RFM отобразится в группе **История заказов** в правой части страницы **Обслуживание клиентов**.

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a>Просмотр или очистка журнала записей анализа RFM

Эта процедура используется для просмотра или очистки журнала записей анализа RFM.

1. Выберите **Центр обработки вызовов** \> **Периодические операции** \> **RFM-анализ**.
2. На странице **RFM-анализ** выберите запись, которую требуется просмотреть.
3. Чтобы просмотреть журнал записей, выберите экспресс-вкладку **История**.
4. Чтобы очистить журнал записей, выберите **Очистить историю**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]