---
title: Функция зависимости между сопоставлением книги учета после закрытия года
description: В этой статье объясняется, как использовать функцию зависимости между сопоставлениями ГК после выполнения закрытия главной книги в конце года.
author: kweekley
ms.date: 12/02/2022
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
ms.openlocfilehash: 7efa9d652d74bd836f51b5b1c5f6bfaf8934ea40
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832171"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close"></a>Функция зависимости между сопоставлением книги учета после закрытия года

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-after-year-end-close"></a>Подготовка для функции зависимости сопоставления книги учета после закрытия года

Важное изменение функции **Зависимость между сопоставлением книги учета и закрытием года** (функция **Зависимость**) заключается в том, что сопоставление книги учета не может выполняться по несколькими финансовым годам. Это ограничение по нескольким годам относится только к сопоставлению ГК, но не к сопоставлениям расчетов с клиентами или расчетов с поставщиками.

Перед включением функции **Зависимость** финансовый год, который будет подвергнут закрытию года, не должен иметь каких-либо проводок ГК, сопоставленных в других финансовых годах. В частности, для всех проводок, разнесенных в финансовый год, для которого выполняется закрытие года, должны быть отменены сопоставления из проводок, разнесенных в другой финансовый год. Эти проводки можно затем заново сопоставить с проводками в рамках того же финансового года.

В этой статье описаны шаги, необходимые для выявления, отмены сопоставления и повторного сопоставления проводок ГК, которые сопоставлены с другими финансовыми годами. В приведенном примере финансовый год 2022 был закрыт. Основное внимание в этом случае уделяется хорошей подготовке проводок сопоставления ГК до того, как будет выполнено закрытие на конец 2023 года.

## <a name="example-setup"></a>Пример настройки

На следующем рисунке показаны проводки, разнесенные на счет ГК 110190. Зеленые проводки книги учета сопоставлены в том же финансовом году и не должны изменяться. Красные проводки сопоставлены ГК, но они имеют даты проводок в других финансовых годах. Эти проводки должны быть выявлены, а сопоставление ГК, возможно, необходимо реверсировать.

![Проводки ГК.](./media/afterYEC1.png)

## <a name="example"></a>пример

Выполните следующие действия, если вашей организации требуется использовать функцию **Зависимость** после выполнения закрытия года на конец финансового года 2022 г.

> [!NOTE]
> Закрытие года для 2022 г. и более ранних финансовых годов должно быть заново выполнено только в том случае, если новые проводки разнесены в финансовый год 2022 или более ранний. После выполнения следующей процедуры новые проводки должны быть разнесены в 2022 год. Поэтому процесс закрытия на конец года не требуется выполнять заново.
>
> Проводки ГК, которые сопоставляются в других финансовых годах, могут остаться учтенными в ГК, если они не сопоставлены с проводкой, которая была разнесена в 2023 год или более поздний. Например, если вы сопоставили проводки между 2019 и 2020 годами, они могут остаться сопоставленными.

1. Выполните закрытие года для 2022 года без активированной функции **Зависимость**.
2. Необязательно: после завершения закрытия года для 2022 года включите функцию **Зависимость**. Закрытие года считается завершенным, когда все корректировки разнесены и процесс закрытия года не будет выполнен повторно.

    > [!IMPORTANT]
    > Функция **Зависимость** не должна быть включена, если закрытие года для 2022 года будет снова выполнено. Преимущество включения этой функции в данный момент состоит в том, что вы запрещаете пользователям сопоставлять проводки книги учета, которые были разнесены в другие финансовые годы.

    Если закрытие года не завершено, все равно можно выполнить следующие шаги без включения функции **Зависимость**. Эта функция включается на более позднем шаге, как отмечалось.

3. На странице **Сопоставление ГК** определите общую сумму всех проводок, сопоставленных между финансовыми годами 2022 и 2023. Обратите внимание, что проводки 2021 года, сопоставленные с проводками 2022 года, не являются релевантными, поскольку 2022 год уже был закрыт. Такие проводки могут оставаться сопоставленными.

    1. Укажите диапазон дат для всего финансового года 2022. Например, укажите с 1 января 2022 г. по 31 декабря 2022 г., если в качестве финансового года используется календарный год.
    2. В поле **Статус** выберите **Сопоставлено**.
    3. Фильтруйте по одному счету ГК за один раз.

        - Необходимо повторить эти шаги для каждого счета ГК, для которого выполняется сопоставление ГК.
        - Если другие счета ГК больше не настроены для сопоставления ГК, может потребоваться временно добавить их в настройку сопоставления ГК. Затем выполните эти шаги, если счета ГК имеют проводки в 2023 году, которые сопоставляются с проводками в 2022 году или ранее.

    4. Выберите и удерживайте (или щелкните правой кнопкой мыши) столбец **Статус**, затем выберите группировку по этому столбцу.
    5. Выберите и удерживайте (или щелкните правой кнопкой мыши) столбец **Сумма в валюте проводки**, затем выберите общую сумму по этому столбцу.

        - Если проводки сопоставлены только в 2022 году, итог будет равен 0 (нулю).
        - Если имеются проводки, сопоставленные с другими финансовыми годами, итог не будет равен 0 (нулю).

    6. Определите, какие проводки были сопоставлены между 2022 и 2023 гг., путем фильтрации по значению **Дата сопоставления**. При фильтрации по дате сопоставления с 1 января 2023 года по 31 декабря 2023 года вы получаете общую сумму 700 долларов США, которая представляет собой общую сумму проводок, которые были сопоставлены ГК в 2022 и 2023 годах.

    ![Итого по проводкам ГК 2022 года.](./media/afterYEC2.png)

4. Повторите шаг 3 для финансового года 2023. Итог должен соответствовать 700 долларам США с 2022 года, поскольку никакие проводки 2023 годе не были сопоставлены с проводками 2024 года.

    ![Итого по проводкам ГК 2023 года.](./media/afterYEC3.png)

5. Если на шаге 2 была включена функция **Зависимость**, отключите ее перед переходом к шагу 6. В следующих шагах будет отменено сопоставление ГК между разными финансовыми годами. Если функция **Зависимость** активирована, сопоставление ГК не может быть отменено для финансового года 2022. Поэтому необходимо отключить эту функцию, прежде чем продолжить.
6. После отключения функции **Зависимость** используйте те же фильтры на странице **Сопоставление главной книги** для реверсирования сопоставления ГК с подробными проводками.

    1. Вернитесь на страницу **Сопоставление ГК** и отфильтруйте даты проводок для 2023 г. Затем найдите подробные проводки, которые составляют общую сумму 700 долларов США. Фильтрация по этим данным может быть непростой. Возможно, потребуется отправить данные в Microsoft Excel, чтобы их оценить.
    2. После создания списка проводок выберите проводки ГК на странице **Сопоставление ГК** и установите флажок **Отметить выбранное**. Вам не нужно видеть обе стороны проводок ГК, которые были сопоставлены. При пометке дебета или кредита все с одним значением **Кода сопоставления** будет отменено, даже если значение **Выбранная сумма** не равно **0** (нулю).
    3. Выберите **Реверсировать отмеченные проводки**, чтобы отменить сопоставление проводок.

    ![Реверсировать проводки.](./media/afterYEC4.png)

7. Разнесите корректирующий общий журнал, чтобы разделить открытое сальдо для 2023 года на две суммы: часть, которая была сопоставлена с проводками в 2022 финансовом году, и часть, еще не сопоставленная в 2023 году.

    - **Часть открытого сальдо, которая сопоставлена с предыдущим годом:** первая сумма 700 долларов США на основе общей суммы, которые сопоставлены между 2022 и 2023 годами.
    - **Часть открытого сальдо, которая не сопоставлена с предыдущим годом:** вторая сумма — это разница между открывающим сальдо и первой суммой 525 долларов США. Оставшаяся сумма равна 1 700 –700 = 1000 долларов США.

    Таким образом проводки 2023 года можно сопоставить с 700 долларами США, которые изначально были сопоставлены с проводкой 2022 года. Этот шаг является обязательным, поскольку сопоставление ГК не допускает частичного сопоставления.

    1. Перейдите к общему журналу и выполните корректировку. Ваша организация должна решить, какую дату проводки использовать, на основе открытых периодов в 2023 году.
    2. Возможно, потребуется временно отключить параметр **Не разрешать ввод вручную** на странице **Счет ГК**. Эта корректировка не будет разнесена, если для основного счета не разрешен ввод вручную.

    ![Корректировка не разносится.](./media/afterYEC5.png)

8. Теперь можно повторно сопоставить несопоставленные проводки. Вернитесь на страницу **Сопоставление ГК** и ограничьте диапазон дат с 1 января 2022 года по 31 декабря 2022 года. Следующая иллюстрация показывает несопоставленные проводки, которые теперь существуют.

    ![Несопоставленные проводки.](./media/afterYEC6.png)

    - Входящее сальдо 1 700 долларов США может быть сопоставлено с корректировкой на -1 700 долларов США.
    - Подробные проводки, для которых было отменено сопоставление, на -700 долларов США, могут быть сопоставлены с корректировкой на 700,00 долларов США.

9. Заново включите функцию **Зависимость**.
10. После включения функции **Зависимость** сопоставление ГК не может быть выполнено между разными финансовыми годами. Возможно, потребуется еще более разделить остаток сальдо 1 000 долларов США на меньшие суммы, прежде чем можно будет выполнить сопоставление с новыми проводками в 2023 году. Некоторые клиенты выбирают разноску этих данных на шаге 8, где 1 000 долларов США дальше разделяются, чтобы представить несопоставленные проводки из 2022 года. Этот подход по сути имитирует то, что делает функция **Зависимость** только для текущего года. На следующий год это будет автоматически выполнено с помощью параметра **Сохранить подробности** в настройке сопоставления ГК.