---
title: Настройка сборов по платежам для платежей налоговому органу TDS
description: В этой статье объясняется, как настроить сборы по платежам, взимаемые для платежей органу по налогу, удерживаемому у источника (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 598d4c07d9f96fb5ae58c3929bab353a6d57615f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845229"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a>Настройка сборов по платежам для платежей налоговому органу TDS

[!include [banner](../includes/banner.md)]

В этой статье объясняется, как настроить сборы по платежам, взимаемые для платежей органу по налогу, удерживаемому у источника (TDS).

1. Перейдите в раздел **Расчеты с поставщиками \> Настройка платежей \> Сборы по платежам**.

    [![Страница сборов по платежам.](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)

2. Выберите **Создать**, чтобы создать сборы по платежам, затем введите нужные сведения.
3. В поле **Тип сбора** выберите тип сбора по платежу:

    - **Не допускается**
    - **Процент** — процент начисляется на просроченные платежи, сделанные поставщику налогового органа TDS.
    - **Прочие** — прочие расходы начисляются на просроченные платежи, сделанные поставщику налогового органа TDS.

    Если выбрано значение **Процент** или **Прочие**, поле **Расходы** автоматически устанавливается как **Главная книга**.

4. Если был выбран **Процент** или **Прочие** в поле **Тип поля**, в поле **Счет ГК** выберите счет главной книги, куда разносятся расходы по проценту или другие накладные расходы.
5. Введите другие необходимые сведения.
6. На панели операций выберите **Настройка сборов по платежам**, чтобы открыть страницу **Настройка сборов по платежам**, на которой можно настроить сборы по платежам для различных комбинаций банков, способов оплаты, спецификаций оплаты, валют и интервалов дат.

    [![Страница настройки сборов по платежам.](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)

7. На вкладке **Обзор** в поле **Группировки** укажите, для каких банков выполняется настройка сборов по платежам:

    - **Таблица** — сбор является действительным для конкретного банковского счета.
    - **Группа** — сбор является действительным для конкретной банковской группы.
    - **Все** — сбор является действительным для всех банковских счетов.

8. Если выбрана **Таблица** или **Группа** в поле **Группировки**, в поле **Связь с банком** выберите специальный банковский счет или банковскую группу, для которой выполняется настройка сбора по платежам.
9. В поле **Способ оплаты** выберите способ оплаты сборов.
10. В поле **Спецификация оплаты** выберите или введите код спецификации оплаты, созданный на странице **Спецификация оплаты**.
    - Спецификация оплаты используется при использовании электронного платежа как способа оплаты.
12. В поле **Валюта оплаты** выберите валюту, которая активирует сбор. Активация сбора возможна только для проводок, использующих выбранную валюту. Если вы оставляете это поле пустым, все валюты активизируют сборы.
13. В поле **Процент/сумма** выберите метод расчета. Возможные варианты — **Сумма**, **Процент** и **Интервал**.
14. В поле **Сумма сбора** укажите сумму сбора как процент от платежа или сумму для одного платежа.
15. В поле **Валюта сбора** укажите код валюты сбора.
16. Перейдите на вкладку **Общее**, чтобы просмотреть или изменить сведения о выбранном банковском счете.

    [![Вкладка "Общие".](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)

16. В поле **Минимум** введите минимальную сумму проводки, которая активирует сбор.
17. В поле **Максимум** введите максимальную сумму проводки, которая активирует сбор.
18. В полях **Начальная дата** и **Конечная дата** укажите диапазон дат для расчета сборов.
19. В поле **Минимальный сбор** укажите сумму сбора как процент от платежа или сумму для одного платежа.
20. В поле **Налоговая группа** выберите налоговую группу, которая будет использоваться для расчета налога для суммы сбора.
21. В поле **Налоговая группа номенклатур** выберите налоговую группу номенклатур, которая будет использоваться для расчета налога номенклатуры для суммы сбора.
22. Выберите вкладку **Интервал**. 

    [![Вкладка «Интервал».](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)

23. В поле **Дни** введите количество дней между датой разноски (датой скидки) оплаты и датой выполнения простого векселя.
24. В поле **Процент/сумма** выберите, является ли спецификация процентом или установленной суммой.
25. В поле **Сумма сбора** введите сумму сбора как процент от платежа или сумму для одного платежа.
26. Закройте страницу **Настройка сборов по платежам**.
27. Закройте страницу **Сборы по платежам**.
