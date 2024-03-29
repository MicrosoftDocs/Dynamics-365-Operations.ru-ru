---
title: Отчеты по оборотно-сальдовой ведомости
description: В этой статье приводятся сведения об оборотно-сальдовых ведомостях для клиентов, поставщиков и подотчетных лиц.
author: AdamTrukawka
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: atrukawk
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 8c01ecc4bed50fb5347b933d969ff0c5413d06ea
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269325"
---
# <a name="turnover-balance-statement-reports"></a>Отчеты по оборотно-сальдовой ведомости
[!include [banner](../includes/banner.md)]


Оборотно-сальдовые ведомости для клиента, поставщика и подотчетного лица позволяют отобразить информацию в контексте клиентов, поставщиков и подотчетных лиц.

## <a name="customer-turnover-register"></a>Оборотно-сальдовая ведомость (клиенты)

1. Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Оборотно-сальдовая ведомость (клиенты)**.
2. На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.
3. В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.

    > [!NOTE] 
    > Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.

4. В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** или **Указанная валюта**.
5. В поле **Валюта** выберите валюту проводки.

    > [!NOTE]
    > Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.

6. В поле **Счет ГК** выберите счет, для которого требуется создать отчет.
7. Чтобы просмотреть дополнительные сведения о сопоставлении, выберите **Развернуть все**.
8. В разделе **Параметры детализации и сортировки** укажите поля, используемые для группировки, перемещая их из списка **Доступные поля** в список **Выбранные поля**. Можно также изменить группирование, если требуется.
9. В разделе **Финансовые аналитики** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.

    > [!NOTE]
    > Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.

10. Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.
11. Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.
12. Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.
13. Установите для параметра **Показать проводки** значение **Да**, чтобы отобразить проводки по подрядчикам.
14. Установите для параметра **детализировать сальдо** значение **Да**, чтобы отобразить подробное представление столбцов сальдо.
15. Установите для параметра **Рассчитать сальдо** значение **Да**, чтобы рассчитать и показать сальдо в отчете.

    ![Страница "Оборотно-сальдовая ведомость (клиенты)", вкладка "Общие".](media/01_Customer_turnover_register.jpg)

16.  Выберите **ОК**, чтобы создать отчет.

![Страница "Оборотно-сальдовая ведомость (клиенты)".](media/02_Customer_turnover_register.jpg)

>  [!NOTE]
>
>   - Выберите **Ваучер** для просмотра проводок ГК, создавших действие.
>   - Щелкните **Выбрать** для изменения параметров создания отчета.
>   - Выберите **Печать**, чтобы напечатать отчет в Microsoft SQL Server Reporting Services (SSRS).
>   - Выберите **Только итоги**, чтобы показывать только строки для первой выбранной аналитики.

## <a name="vendor-turnover-register"></a>Оборотно-сальдовая ведомость (поставщики)

1. Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Оборотно-сальдовая ведомость (поставщики)**.
2. На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.
3. В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.

    > [!NOTE]
    > Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.

4. В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** и **Указанная валюта**.
5. В поле **Валюта** выберите валюту проводки.

    > [!NOTE]
    > Это поле активно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.

6. В поле **Счет ГК** выберите счет, для которого требуется создать отчет.
7. Чтобы просмотреть дополнительные сведения о сопоставлении, выберите **Развернуть все**.
8. В разделе **Параметры детализации и сортировки** укажите поля, используемые для группировки, перемещая их из списка **Доступные поля** в список **Выбранные поля**. Можно также изменить группирование, если требуется.
9. В разделе **Финансовые аналитики** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.

    > [!NOTE] 
    > Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.

10. Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.
11. Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.
12. Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.
13. Установите для параметра **Показать проводки** значение **Да**, чтобы отобразить проводки по подрядчикам.
14. Установите для параметра **детализировать сальдо** значение **Да**, чтобы отобразить подробное представление столбцов сальдо.
15. Установите для параметра **Рассчитать сальдо** значение **Да**, чтобы рассчитать и показать сальдо в отчете.

    ![Страница "Оборотно-сальдовая ведомость (поставщики)", вкладка "Общие".](media/04_Vendor_turnover_register.jpg)

16. Выберите **ОК**, чтобы создать отчет.

![Страница "Оборотно-сальдовая ведомость (поставщики)".](media/05_Vendor_turnover_register.jpg)

>  [!NOTE]
>
> - Выберите **Ваучер** для просмотра проводок ГК, создавших действие.
> - Щелкните **Выбрать** для изменения параметров создания отчета.
> - Выберите **Печать**, чтобы напечатать отчет в SSRS.
> - Выберите **Только итоги**, чтобы показывать только строки для первой выбранной аналитики.

## <a name="advance-holder-turnover-register"></a>Регистр оборотно-сальдовой ведомости по подотчетным лицам

1. Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Регистр оборотно-сальдовой ведомости по подотчетным лицам**.
2. На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.
3. В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.

    > [!NOTE]
    > Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.

4. В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** или **Указанная валюта**.
5. В поле **Валюта** выберите валюту проводки.

    > [!NOTE]
    > Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.

6. В поле **Счет ГК** выберите счет, для которого требуется создать отчет.
7. Чтобы просмотреть дополнительные сведения о сопоставлении, выберите **Развернуть все**.
8. В разделе **Параметры детализации и сортировки** укажите поля, используемые для группировки, перемещая их из списка **Доступные поля** в список **Выбранные поля**. Можно также изменить группирование, если требуется.
9. В разделе **Финансовые аналитики** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.

    > [!NOTE]
    > Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.

10. Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.
11. Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.
12. Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.
13. Установите для параметра **Показать проводки** значение **Да**, чтобы отобразить проводки по подрядчикам.
14. Установите для параметра **детализировать сальдо** значение **Да**, чтобы отобразить подробное представление столбцов сальдо.
15. Установите для параметра **Рассчитать сальдо** значение **Да**, чтобы рассчитать и показать сальдо в отчете.

16. Выберите **ОК**, чтобы создать отчет.

> [!NOTE]
>
> - Выберите **Ваучер** для просмотра проводок ГК, создавших действие.
> - Щелкните **Выбрать** для изменения параметров создания отчета.
> - Выберите **Печать**, чтобы напечатать отчет.
> - Выберите **Только итоги**, чтобы показывать только строки для первой выбранной аналитики.

## <a name="general-ledger-report"></a>Отчет по главной книге

Отчет **Главная книга** предназначен для создания оборота по указанному счету, который используется в корреспонденции с другими счетами.

1. Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Главная книга**.
2. На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.
3. В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.

    > [!NOTE]
    > Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.

4. В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** или **Указанная валюта**.
5. В поле **Валюта** выберите валюту проводки.

    > [!NOTE]
    > Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.

6. В поле **Счет ГК** выберите счет, для которого требуется создать отчет.
7. В поле **Корр. счет** выберите корр. счет, для которого требуется создать отчет.
8. Чтобы просмотреть дополнительные сведения о сопоставлении, выберите **Развернуть все**.
9. В разделе **Параметры детализации и сортировки** можно указать поля, используемые для группировки, перемещая их из списка **Доступные поля** в список **Выбранные поля**. Можно также изменить группирование, если требуется.
10. В разделе **Финансовые аналитики** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.

    > [!NOTE]
    > Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.

11. Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.
12. Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.
13. Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.
14. Установите для параметра **Показать проводки** значение **Да**, чтобы отобразить проводки по подотчетным лицам.
15. Установите для параметра **Рассчитать сальдо** значение **Да**, чтобы рассчитать и показать сальдо в отчете.

    ![Страница оборотно-сальдовой ведомости главной книги, вкладка "Общие".](media/7_General_ledger_turnover_balance_sheet.jpg)

16. Выберите **ОК**, чтобы создать отчет.

![Страница оборотно-сальдовой ведомости главной книги.](media/8_General_ledger.jpg)

> [!NOTE]
>
> - Выберите **Ваучер** для просмотра проводок ГК, создавших действие.
> - Щелкните **Выбрать** для изменения параметров создания отчета.
> - Выберите **Печать**, чтобы напечатать отчет в SSRS.
> - Выберите **Только итоги**, чтобы показывать только строки для первой выбранной аналитики.

## <a name="turnover-balance-statement-report-archive"></a>Архив отчета по оборотно-сальдовой ведомости

На странице **Архив отчетов** можно просматривать отчеты и загружать их в формате Excel.

1. Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Архив отчетов**.
2. На странице **Архив отчетов по оборотно-сальдовой ведомости** в поле **Тип отчета** укажите тип отчета.
3. Выберите отчет.

    ![Страница архива отчета по оборотно-сальдовой ведомости.](media/10_Turnover_and_balance_statement_report_archive.jpg)

4. Выбор **Создать отчет** для создания нового отчета с теми же параметрами, что и выбранный отчет.
5. Выберите **Вывод отчета**, чтобы напечатать отчет.
6. Выберите **Экспорт в Microsoft Excel**, чтобы открыть страницу **Экспорт в Excel**, а затем нажмите кнопку **Загрузить**, чтобы загрузить отчет в формате Excel.
7. Выберите **Просмотр** для просмотра отчета.

## <a name="pre-calculate-transactional-data"></a>Предварительный расчет данных проводок

Предварительно рассчитать данные проводок, можно повысить производительность.

1. Перейдите в раздел **Главная книга** \> **Настройка главной книги** \> **Параметры главной книги**.
2. На вкладке **Главная книга** в разделе **Оборотно-сальдовая ведомость** установите для параметра **Использовать предварительно рассчитанные данные** значение **Да**.
3. Выберите **Главная книга** \> **Периодические задачи** \> **Предварительно рассчитать данные проводок**.
4. В диалоговом окне **Предварительный расчет данных проводок** на экспресс-вкладке **Параметры** в поле **Тип отчета** выберите тип отчета:

    - Оборотно-сальдовая ведомость (клиенты)
    - Оборотно-сальдовая ведомость (поставщики)
    - Главная книга
    - Регистр оборотно-сальдовой ведомости по подотчетным лицам

    ![Диалоговое окно предварительного расчета данных проводок.](media/11_Pre-calculate_transactional_data.jpg)

5. Выберите **ОК** для предварительного расчета данных проводок.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
