---
title: Функция зависимости между сопоставлением книги учета перед закрытием года с помощью страницы запроса
description: В этой статье объясняется, как использовать функцию зависимости между сопоставлениями ГК с помощью новой страницы запроса перед выполнением закрытия главной книги в конце года.
author: kweekley
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: b138d2d5e88ff7f2ca2240cf256a4938f55a5606
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853162"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close-using-the-inquiry-page"></a>Функция зависимости между сопоставлением книги учета перед закрытием года с помощью страницы запроса

Одно важное изменение функции **Зависимость между сопоставлением книги учета и закрытием года** (функция **Зависимость**) заключается в том, что сопоставление книги учета не может выполняться по несколькими финансовым годам. Это ограничение по нескольким годам относится только к сопоставлению ГК, но не к сопоставлениям расчетов с клиентами или расчетов с поставщиками.

Перед включением функции **Зависимость** финансовый год, который будет подвергнут закрытию года, не должен иметь каких-либо проводок ГК, сопоставленных в других финансовых годах. В частности, для всех проводок, разнесенных в финансовый год, для которого выполняется закрытие года, должны быть отменены сопоставления из проводок, разнесенных в другой финансовый год. Эти проводки можно затем заново сопоставить с проводками в рамках того же финансового года.

В этой статье описываются шаги, необходимые для выявления, отмены сопоставления и повторного сопоставления проводок ГК, которые сопоставлены с другими финансовыми годами. В приведенном выше примере финансовый год 2021 был закрыт и выполняется подготовка к выполнению закрытия года на конец финансового года 2022.

В Microsoft Dynamics 365 Finance выпуска 10.0.29 можно выявить, отменить сопоставление и повторно сопоставить проводки ГК, используя доступную новую страницу запроса. Если в настоящее время вы не используете Finance выпуска 10.0.29 или более поздней версии, можно найти шаги для выявления, отмены сопоставления и повторного сопоставления проводок ГК в следующих статьях:

- [Функция зависимости между сопоставлением книги учета до закрытия года](ledger-settle-yec.md)
- [Функция зависимости между сопоставлением книги учета после закрытия года](ledger-settle-yec-after.md)

Дополнительные сведения о новом окне запроса см. в разделе [Запрос сопоставления ГК](ledger-settlement-inquiry.md). 

## <a name="example-setup"></a>Пример настройки

На следующем рисунке показаны проводки, разнесенные на счет ГК 110200. Зеленые проводки были сопоставлены в ГК в том же финансовом году и не должны изменяться. Красные проводки были сопоставлены ГК, но они имеют даты проводок в других финансовых годах. Эти проводки должны быть выявлены, а сопоставление ГК, возможно, необходимо реверсировать.

![Разнесенные проводки ГК.](./media/ledgersettlement.png)

## <a name="example"></a>пример

Выполните следующие действия, если вашей организации требуется использовать функцию **Зависимость** перед выполнением закрытия года на конец финансового года 2022 г.

> [!NOTE]
> Закрытие года для 2021 г. и более ранних финансовых годов должно быть заново выполнено только в том случае, если новые проводки разнесены в финансовый год 2021 или более ранний. После выполнения следующей процедуры новые проводки не разносятся в 2021 год. Поэтому процесс закрытия на конец года не требуется выполнять заново.
>
> Проводки ГК, которые сопоставляются в других финансовых годах, могут остаться учтенными в ГК, если они не сопоставлены с проводкой, которая была разнесена в 2022 год (год, который закрывается) или более поздний. Например, если вы сопоставили проводки в 2019 и 2020 годах, они могут остаться сопоставленными.

1. **Не** активируйте функцию **Зависимость**.
2. На странице **Сопоставления книги учета** выберите **Проверка сопоставлений между годами**.
3. Выявите все проводки, разнесенные в другие финансовые годы, но сопоставленные проводкам, разнесенным в 2022 г.

    1. Выберите финансовый год 2022, финансовый год, для которого требуется запустить процесс закрытия года.
    2. Выберите значение в поле **Набор финансовых аналитик** для отображения финансовых аналитик, которые необходимо просмотреть для счета ГК. Счет ГК всегда отображается, даже если выбранный набор аналитик не содержит счета ГК.
    3. Выберите **Показать проводки**.

    На странице запроса отобразятся все проводки, для всех счетов ГК (даже если они больше не входят в настройку сопоставления ГК), из всех финансовых годов, сопоставленные с проводками, которые были разнесены в 2022 году. Отображаются три различных счета ГК.

    ![Сопоставления между годами в 2022 году.](./media/review-cross-year.png)

3. Выберите и удерживайте (или щелкните правой кнопкой мыши) в сетке, затем выберите **Экспорт всех строк**. Эти строки являются всеми проводками, для которых нужно отменить сопоставления из проводок в 2022 году, до того, как можно будет выполнить закрытие года. Вы хотите подробный список проводок, чтобы можно было правильно повторно сопоставить проводки позже.
4. Отметьте финансовые года, для которых были разнесены проводки. В этом примере имеются проводки в 2021 и 2023 годах.
5. На странице запроса измените финансовый год на 2021, первый финансовый год, содержащий проводки, сопоставленные с проводками в 2022 году.
6. Выполните фильтрацию по столбцу **Дата проводки**, чтобы включить только проводки, разнесенные в 2022 году. Эти проводки представляют собой подробные проводки из 2022 года, которые были сопоставлены с проводками в 2021 году.
7. Выберите и удерживайте (или щелкните правой кнопкой мыши) в сетке, затем выберите **Экспорт всех строк**.

    > [!IMPORTANT]
    > В следующих шагах будет отменено сопоставление этих проводок, а затем они будут заново сопоставлены с проводками в 2022 году. Очень важно сохранить эту информацию в Excel.

    ![Сопоставления между годами в 2021 году.](./media/review-cross-year.png)

8. На странице запроса измените финансовый год на 2023, следующий финансовый год, содержащий проводки, сопоставленные с проводками в 2022 году. 
9. Выполните фильтрацию по столбцу **Дата проводки**, чтобы включить только проводки, разнесенные в 2022 году. Эти проводки представляют собой подробные проводки из 2023 года, которые были сопоставлены с проводками в 2022 году. 
10. Выберите и удерживайте (или щелкните правой кнопкой мыши) в сетке, затем выберите **Экспорт всех строк**.

    > [!IMPORTANT]
    > В следующих шагах будет отменено сопоставление этих проводок, а затем они будут заново сопоставлены с проводками в 2022 году. Очень важно сохранить эту информацию в Excel.

    ![Сопоставления между годами в 2023 году.](./media/filter-transactions.png)

11. Повторите предыдущие шаги для каждого финансового года, в котором имеются проводки, сопоставленные проводкам в 2022 году. Обязательно экспортируйте подробные проводки в Excel.

    После того как все подробные проводки из 2021 и 2023 годов экспортированы в Excel, можно отменять сопоставление проводок с помощью новой страницы запроса.

12. Измените финансовый год на 2022.
13. Выберите все записи в сетке, затем выберите **Отменить сопоставление отмеченных записей**. Для всех выбранных проводок в сетке будет отменено сопоставление.

    Отображаются два предупредительных сообщения для обеспечения того, чтобы сведения о проводках были экспортированы в Excel до отмены сопоставления проводок. Если вы случайно отменили сопоставление проводок ГК перед отправкой данных в Excel, отменить отмену сопоставления невозможно.

    ![Отменяется сопоставление проводок между годами.](./media/revert-unsettle.png)

14. Данные Excel используются для того, чтобы найти общую сумму проводок в 2021 и 2023 годах, сопоставленных проводкам в 2022 году. В этом примере проводки для 2021 года имеют общую сумму 525 долларов США, и проводки за 2023 год имеют общую сумму 700 долларов США.
15. Разнесите корректирующий общий журнал, чтобы разделить открытое сальдо для 2022 года на две суммы: часть, которая была сопоставлена с финансовым годом 2021, и часть, еще не сопоставленная с 2022 годом.

    - **Часть открытого сальдо, которая была сопоставлена с предыдущим годом:** первая сумма 525 долларов США на основе общей суммы, которые были сопоставлены между 2021 и 2022 годами.
    - **Часть открытого сальдо, которая не была сопоставлена с предыдущим годом:** вторая сумма — это разница между открывающим сальдо и сопоставленной суммой 525 долларов США. Оставшаяся сумма равна 1 025 –525 = 500 долларов США.

    Таким образом проводки 2022 года можно сопоставить с 525 долларами США, которые изначально были сопоставлены с проводкой 2021 года. Этот шаг является обязательным, поскольку сопоставление ГК не допускает частичного сопоставления.

    1. Перейдите к общему журналу и выполните корректировку. Ваша организация должна решить, какую дату проводки использовать, на основе открытых периодов. Эти проводки могли быть сопоставлены с использованием даты сопоставления "Январь" или "Февраль" 2022 года, но возможно, что корректировку придется разнести в декабре, если это единственный открытый период.
    2. Возможно, потребуется временно отключить параметр **Не разрешать ввод вручную** для счета 110200 на странице **Счет ГК**. Эта корректировка не будет разнесена, если для основного счета не разрешен ввод вручную.

    ![Разноска корректирующего общего журнала.](./media/not-post.png)

16. Теперь можно повторно сопоставить несопоставленные проводки. Вернитесь на страницу **Сопоставления книги учета**, укажите диапазон дат с 1 января по 31 декабря 2022 года и выполните фильтрацию по счету ГК 110200. Затем используйте подробные проводки, экспортированные в Excel, чтобы найти отдельные проводки, которые должны быть повторно сопоставлены. Следующая иллюстрация показывает несопоставленные проводки, которые теперь существуют.

    ![Несопоставленные проводки.](./media/updated-unsettled.png)

    - Входящее сальдо 1 025 долларов США может быть сопоставлено с корректировкой на -1 025 долларов США.
    - Подробные проводки, для которых было отменено сопоставление, на -400, -50 и -75 долларов США, могут быть сопоставлены с корректировкой на 25 долларов США.

17. Включите функцию **Зависимость**. Теперь вы готовы к выполнению закрытия года.

    - Перед выполнением закрытия года следует установить флажок **Сохранить сведения** для всех счетов балансового отчета в настройке сопоставления ГК. Дополнительные сведения см. в разделе [Зависимость между сопоставлением книги учета и закрытием года](awareness-between-ledger-settlement-year-end-close.md).
    - Когда начато закрытие года для 2022 года, если по-прежнему имеются проводки, которые были сопоставлены другим финансовым годам, процесс закрытия года немедленно сообщит об этом. Эта ситуация может возникнуть, если пользователи сопоставляли проводки между разными финансовыми годами после выполнения предыдущих шагов.
    - Если проводки 2021 и 2022 годов все еще сопоставляются, необходимо снова отключить функцию **Зависимости**, а затем повторить предыдущие шаги, чтобы отменить сопоставление этих проводок. Этот подход требуется потому, что 2021 год закрыт, и в закрытом финансовом году отмена сопоставления проводок невозможна.
    - Если проводки 2022 и 2023 годов все еще сопоставлены нет необходимости отключать функцию **Зависимость**. Поскольку ни 2022, ни 2023 года не закрыты, можно использовать предыдущие шаги для отмены сопоставления проводок.

18. Можно сопоставить проводку на 700 долларов США из 2023 года с подробными проводками, которые были перенесены в качестве начальных сальдо в 2023 год. Эта проводка не будет сопоставлена с исходной проводкой в 2022 году.

После успешного выполнения закрытия года для 2022 года можно оставить функцию **Зависимость** включенной после этого.
