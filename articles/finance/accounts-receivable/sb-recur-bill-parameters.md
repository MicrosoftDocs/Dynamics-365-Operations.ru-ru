---
title: Параметры повторяющегося выставления счетов по контракту
description: В этой статье объясняется, как настроить значения по умолчанию для графиков выставления счетов, созданных в повторяющемся выставлении счетов по контракту. Здесь также объясняется создание групп графиков выставления счетов.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 64d6e21c2d8c588a64f0f4cf8b7a0bafc853bcab
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644012"
---
# <a name="recurring-contract-billing-parameters"></a>Параметры повторяющегося выставления счетов по контракту

Страница **Параметры повторяющегося выставления счетов по контракту** используется для настройки значений по умолчанию для графиков выставления счетов, созданных в повторяющемся выставлении счетов по контракту. Все создаваемые графики выставления счетов изначально будут использовать эти значения по умолчанию. Однако значения для каждого графика выставления счетов можно изменить по мере необходимости.

## <a name="general-tab"></a>Вкладка "Общие"

1. На странице **Параметры повторяющегося выставления счетов по контракту** на вкладке **Общие** в поле **Группа графиков выставления счетов** выберите группу графиков выставления счетов. Сведения о том, как настроить группы графиков выставления счетов, см. в разделе [Группы графиков выставления счетов](#set-up-billing-schedule-groups) далее в этой статье.
2. В поле **Тип завершения** выберите способ расчета окончательной накладной при завершении графика выставления счетов:

    - **Изменить план** — обрезать график выставления счетов на дату завершения, изменить статус графика на **Последнее выставление счета** и настроить связанный график отсрочки, сторнировав сумму, которая больше не должна быть признана. Если дата начала выставления счетов позже даты завершения, оставшиеся периоды выставления счетов удаляются.
    - **Остаток по счету** — добавление любых оставшихся сумм в график выставления счетов до периода завершения, изменение статуса графика на **Последнее выставление счета** и обновление графика отсрочки. Если дата начала выставления счетов позже даты завершения, общая сумма всех оставшихся периодов выставления счетов добавляется в платежный период, а оставшиеся периоды выставления счетов удаляются.
    - **Нет корректировки** — закрытие графика выставления счетов на дату завершения. В график выставления счетов не вносятся никакие корректировки.

3. В поле **Уникальный тип графика** выберите **Нет**, чтобы указать, что клиенты будут ограничиваться одним графиком выставления счетов. Выберите **На клиента** или **На конечного пользователя**, чтобы указать, что клиенты ограничены уникальным графиком.
4. Установите для параметра **Выровнять по месяцам** значение **Да**, чтобы выровнять строки со сведениями графика выставления счетов с окончанием месяца при создании или обновлении графика выставления счетов. Для использования инкрементных дат установите значение **Нет**.
5. Установите для параметра **Распределять пропорционально по частичным периодам** значение **Да**, чтобы распределить суммы для выставления счетов на основе количества дней в периоде. Установите значение **Нет**, чтобы иметь одинаковые суммы в каждом периоде выставления счетов, независимо от количества дней.
6. Если для параметра **Распределять пропорционально по частичным периодам** задано значение **Да**, установите для поля **Пропорциональный метод** значение **Ежедневно**, чтобы распределить суммы на основе количества дней в периоде. Установите значение **Ежемесячно**, чтобы иметь равную сумму каждый месяц.
7. Укажите, следует ли по умолчанию блокировать только что созданные графики выставления счетов.

    > [!NOTE]
    > Чтобы снять блокировку графика выставления счетов, пользователь должен быть участником группы пользователей. Выберите **Переопределение группы пользователей снятия блокировки**, чтобы настроить группу пользователей, для которой включен параметр **Разрешить снятие блокировки**.

8. В поле **Тип проводки по накладной** выберите тип проводки по накладной по умолчанию для новых графиков выставления счетов.
9. Установите для параметра **Сопоставить отсрочку с выставлением счетов** значение **Да**, чтобы выровнять соответствующий график отсрочки, используя те же даты, что и для графика выставления счетов. Для использования разных дат установите значение **Нет**.
10. При использовании функции разделения выручки задайте для параметра **Автоматически создать разделение выручки** значение **Да** при добавлении номенклатур в график выставления счетов. Если номенклатура настроена как номенклатура с разделением выручки, флажок **Разделение выручки** будет автоматически установлен в строке графика выставления счетов. Установите для этого параметра значение **Нет**, если требуется вручную установить флажок **Разделение выручки**.
11. Задайте для параметра **Разбиение клиента** значение **Да**, чтобы график выставления счетов применялся для различных клиентов. Если задано значение **Да** параметр **Разбиение клиента** доступен для заголовка графика выставления счетов и строки графика выставления счетов. 
12. Задайте поля для создания заказов на продажу:

    - Накладные можно консолидировать по периодам, клиентам или номенклатурам. Можно задать любое сочетание значений **Да** и **Нет**. Накладные также можно разбивать по номенклатурным группам.
    - Для накладных предусмотрены следующие параметры разноски:

        - **Создать заказ на продажу** — создание только заказа на продажу.
        - **Показать накладную на разноску** — выставление накладной по заказу на продажу и открытие страницы, где можно разнести накладную вручную.
        - **Создать накладную с произвольным текстом** — выберите этот параметр, если используются накладные с произвольным текстом.
        - **Автоматическая разноска накладной** — выставление накладной по заказу на продажу и ее автоматическая разноска.

    - Установите для параметра **Добавить даты выставления счетов в описание номенклатуры** значение **Да**, чтобы добавить описание, которое включает в себя начальную и конечную даты выставления счетов.
    - Установите для параметра **Исключить нулевое потребление** значение **Да**, чтобы исключить строки графика выставления счетов без потребления. Установите значение **Нет**, чтобы включить эти строки в заказ на продажу.
    - Установите для параметра **Не печатать дочерние номенклатуры** значение **Да**, если не нужно печатать дочерние номенклатуры для разделения выручки по заказу на продажу. В накладной будет отображаться только родительская номенклатура. Если чистая сумма (скрытых) дочерних номенклатур равна ненулевой сумме, чистая сумма родительской строки показывает сводку дочерних строк. Установите для этого параметра значение **Нет**, чтобы напечатать все дочерние номенклатуры, расположенные под родительской номенклатурой в накладной заказа на продажу.

12. Задайте поля для поддержки и возобновлений:

    - Установите для параметра **Автоматически включать поддержку и возобновление** значение **Да**, чтобы в заказе на продажу автоматически использовалась функция поддержки и возобновления.
    - В поле **Уровень поддержки и возобновления** выберите уровень поддержки и возобновления по умолчанию.
    - В поле **Количество поддержки и возобновления** укажите количество поддержки и возобновления.
    - В поле **Дата начала поддержки и возобновления по умолчанию** укажите дату, которая будет использоваться по умолчанию в качестве начальной даты для поддержки и возобновления:

        - **Дата проводки** — используйте дату проводки как дату начала.
        - **Начало текущего месяца** — используется первое число текущего месяца в качестве начальной даты.
        - **Начало следующего месяца** — используется первое число следующего месяца в качестве начальной даты. Если дата проводки приходится на первое число, используется первое число текущего месяца.
        - **Правило 15** — используется первое число текущего месяца в качестве начальной даты, если дата проводки находится между первым и пятнадцатым числом. Если дата проводки является шестнадцатым числом или позже, используется первое число следующего месяца в качестве начальной даты.

    - Установите для параметра **Включить скидку в расчет** значение **Да**, чтобы включить сумму скидки в сумму поддержки или возобновления. Установите для него значение **Нет**, чтобы исключить сумму скидки.
    - В полях **Периодичность поддержки** и **Периодичность возобновления** выберите частоту, которая будет использоваться при добавлении номенклатур поддержки и возобновления к графику выставления счетов: **Ежедневно**, **Ежемесячно**, **Ежеквартально**, **Раз в полгода** или **Ежегодно**.
    - Установите для параметра **Сопоставить по номенклатурной группе** значение **Да**, чтобы выровнять даты начала и окончания новых номенклатур по существующим номенклатурам на основе этой номенклатурной группы.
    - Установите для параметра **Сопоставить со следующим периодом, по которому не выставлен счет** значение **Да**, чтобы определить дату выравнивания для номенклатуры возобновления на основе даты следующего периода, по которому не выставлены счета после начала возобновления.
    - Установите для параметра **Копировать серийный номер** значение **Да**, чтобы скопировать серийный номер номенклатуры из строки исходного заказа на продажу в соответствующую строку графика оплаты.

13. Если в графике выставления счетов используется эскалация, выберите метод, используемый для расчета индекса потребительских цен.
14. Установите для параметра **Отслеживать изменение цены** значение **Да**, если требуется записать изменения цены по строкам графика выставления счетов. Если строка графика выставления счетов вручную изменена со стандартной на плоскую и введена новая цена, сведения аудита отслеживаются в строке графика выставления счетов. Установите для этого параметра значение **Нет**, если не требуется отслеживать эти изменения.
15. Укажите, следует ли по умолчанию фильтровать записи по дате начала или по дате окончания на странице **Создать накладную**.
16. Если используется функция **Выручка по невыставленным счетам**, укажите используемые параметры:

    - Установите для параметра **Разнести общие журналы автоматически** значение **Да**, если общий журнал требуется создать и одновременно разнести. Установите значение **Нет**, если требуется создать общий журнал, а затем вручную разнести его.
    - В поле **Наименование журнала по умолчанию** выберите имя журнала по умолчанию, которое будет использоваться при создании общего журнала.
    - В поле **Метод "Краткосрочно без выставления счетов"** выберите краткосрочный метод без выставления счетов, если он используется. Если выбрано значение **Нет**, краткосрочные функции не будут использоваться для выручки по невыставленным счетам. Выберите **Скользящие периоды**, чтобы всегда использовать 12 месяцев или **Фиксированный год** для использования оставшегося финансового года.

17. Укажите параметры, которые используются при завершении графика выставления счетов и его строк:

    - **Выдать кредит** — создание кредит-ноты при завершении графика выставления счетов или строки графика выставления счетов.
    - **Корректировка кредита** — создание корректировки кредита для графика выставления счетов при завершении строки. Корректировка кредита отображается в будущем периоде выставления счетов для графика выставления счетов. Корректировка кредита будет обновлять сумму накладной для следующего периода выставления счетов до окончания применения кредита к графику выставления счетов.
    - **Без кредита** — не создавать корректировку кредита или кредит-ноту при завершении графика выставления счетов или строки графика выставления счетов. Этот параметр доступен только в том случае, если для завершения графика выставления счетов используется параметр **Без корректировки**.
18. Когда для параметра **Разовый может быть прерван с возвратом денежных средств** задано значение **Нет**, а для графика выставления счетов установлена периодичность **Один раз**, статус строки графика выставления счетов меняется на **Прекращено** после выставления счетов согласно графику. График выставления счетов нельзя отменить, и невозможно выдать кредит. Когда для параметра **Разовый может быть прерван с возвратом денежных средств** задано значение **Да**, график выставления счетов с периодичностью **Один раз**, получит статус **Активен** после выставления счетов согласно графику. Строку графика выставления счетов нельзя отменить, и невозможно обработать возврат денежных средств. 
19. Параметр **Распределять пропорционально ежедневно**, заданный в наборе параметров по умолчанию, приведет к вызову страницы массовой отмены и диалогового окна отмены строки и заголовка графика выставления счетов. Можно изменить в процессе отмены. Если задано значение **Да**, сумма возврата будет рассчитана с использованием суточной ставки. Если задано значение **Нет**, будет начислено с учетом дня отмены и согласно периодичности выставления счетов. Например, если используется периодичность за месяц, а сумма счетов за месяц составляет 100 долл. США, сумма кредита увеличится на 100 долл. США. Если задана периодичность выставления счетов "Один раз", то сумма кредита составит 0 долл. США. Вы должны задать значение "Да" для параметра "Распределять пропорционально ежедневно", чтобы получить возврат для периодичности выставления счетов "Один раз". 
20. Задайте для параметра **Создать отсрочку по кредиту** значение **Да**, чтобы создать новый график отсрочки при кредитовании по существующему графику отсрочки. Установите для параметра значение **Нет**, чтобы создать кредит для существующего графика отсрочки.

## <a name="sequence-number-tab"></a>Вкладка "Порядковый номер"

Вкладка **Порядковый номер** на странице **Параметры повторяющегося выставления счетов по контракту** предназначена для задания значения по умолчанию для номеров графиков выставления счетов. Значения по умолчанию настраиваются на странице **Номерные серии** (**Администрирование организации \> Номерные серии \> Номерные серии**).

## <a name="set-up-billing-schedule-groups"></a>Настройка групп графиков выставления счетов

Страница **Группа графиков выставления счетов** предназначена для создания группы графиков выставления счетов для повторяющегося выставления счета по контракту. Когда создается новый график выставления счетов и к ней применяется группа графиков выставления счетов, значения, определенные на странице **Группа графиков выставления счетов** вводятся как значения по умолчанию для графика выставления счетов. Можно изменить любые значения по умолчанию для конкретного графика выставления счетов, который вы создаете. Можно настроить несколько групп графиков выставления счетов, а затем назначить одну из них в качестве группы графиков выставления счетов по умолчанию на странице **Параметры повторяющегося выставления счетов по контракту**.

Чтобы создать группу графиков выставления счетов для повторяющегося выставления счетов по контракту, выполните следующие действия.

1. На странице **Группа графиков выставления счетов** выберите **Создать**, чтобы создать группу графиков выставления счетов.
2. В поле **Группа графиков выставления счетов** введите уникальный идентификатор.
3. В поле **Описание** введите описание.
4. В поле **Периодичность выставления счетов** укажите, как часто должны выставляться счета для клиента по графику выставления счетов: **Однократно**, **Ежедневно**, **Ежемесячно**, **Ежеквартально**, **Раз в полгода** или **Ежегодно**.
5. В поле **Интервал выставления счетов** введите интервал выставления счетов. Например, установите в поле **Периодичность выставления счетов** значение **Ежемесячно**, а в поле **Интервал выставления счетов** — значение **2**, чтобы выставлять счета каждый второй месяц.
6. В поле **Метод ценообразования** выберите метод ценообразования по умолчанию для номенклатур в графике выставления счетов:

    - **Стандартный** — расчет цены за единицу на основе общего количества, которое введено, и использование стандартной цены со страницы **Выпущенные продукты** в управлении сведениями о продукте.
    - **Фиксированная** — применяется фиксированная цена, введенная в строке графика выставления счетов.
    - **Уровень** — расчет цены за единицу с использованием фиксированного количества в разных ценовых диапазонах. Каждый уровень должен быть заполнен до перехода к следующему диапазону ценообразования.
    - **Плоский уровень** — расчет цены за единицу с использованием фиксированного количества и сумм цены без учета скидок и наценок для разных ценовых диапазонов. Цена, которая начисляется в период выставления счетов, использует цену без учета скидок и наценок, соответствующую уровню, на котором существует количество для выставления счета.

7. В поле **Тип номенклатуры** выберите тип номенклатуры для группы выставления счетов:

    - **Стандартный** — выберите это значение, если количество является статическим.
    - **Использование** — выберите это значение для номенклатур с типом "лимитные" или "потребление". Если выбрано это значение, установите в поле **Параметр показаний использования** значение **Показания**, чтобы ввести значение (показания) для периода выставления счетов на измерительном приборе или устройстве. Потребленное значение будет рассчитываться на основе предыдущего периода выставления счетов и текущего введенного значения показаний.
    - **Этап** — выберите это значение, чтобы использовать функцию выставления счетов по этапам. Если выбрано это значение, в поле **Шаблон этапа** выберите шаблон этапа, если он используется.
    - **Потребление** — выберите это значение, чтобы ввести значение, которое потреблено за период выставления счетов.

8. Установите для параметра **Выставить накладную отдельно** значение **Да**, чтобы создать комбинацию консолидированных накладных и отдельных накладных для одного и того же клиента. Например, у клиента пять графиков выставления счетов. Три из них будут консолидироваться в одной накладной, но для каждого из двух других требуется отдельная накладная. Установите для этого параметра значение **Нет**, чтобы создать только одну консолидированную накладную для клиента.
9. установите для параметра **Возобновлять автоматически** значение **Да**, чтобы автоматически возобновлять повторяющийся график выставления счетов для следующего периода выставления счетов при создании накладной. Установите значение **Нет**, чтобы возобновлять график выставления счетов вручную. В поле **Строки для добавления по возобновлению** укажите количество строк, которое необходимо добавить для каждого возобновления.
10. Установите для параметра **Эскалация** значение **Да**, чтобы применить *эскалации* (повышение цен) к графикам выставления счетов, связанным с данной группой графиков выставления счетов.
