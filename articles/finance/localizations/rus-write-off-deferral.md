---
title: Списание РБП (Россия)
description: Этот раздел объясняет, как списать РБП и как реверсировать списание РБП.
author: anasyash
ms.date: 06/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 9e3774de9cd7d84223d646f91ed8aa01ec89a8f5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818202"
---
# <a name="write-off-deferrals-russia"></a>Списание РБП (Россия)

[!include [banner](../includes/banner.md)]

## <a name="write-off-deferrals"></a>Списание РБП

1. Перейдите к **Главная книга** \> **Записи в журнале** \> **Журнал расходов будущих периодов**.
2. В области действий выберите **Создать**.
3. В поле **Имя** выберите имя журнала.
4. В области действий выберите **Строки**, чтобы открыть страницу **Ваучер журнала**.
5. На панели операций выберите **Групповые операции** \> **Списание**, чтобы открыть диалоговое окно **Списание РБП**.
6. Выберите дату проводки в поле **Дата проводки**.
7. На экспресс-вкладке **Включаемые записи** выберите **Фильтр**, чтобы открыть диалоговое окно **Запрос**, в котором можно задать критерии выбора.
8. Выберите **OK**, чтобы вернуться к странице **Ваучер журнала**. Подробные сведения по ваучерам списания РБП со статусом **В работе** показаны, на основе параметров фильтра, настроенных в диалоговом окне **Запрос**.

    ![Страница Ваучера журнала](media/rus-write-off-deferral-01.png)

9. На панели операций выберите **Функции** \> **Редактировать строку**, чтобы отредактировать журнал РБП перед разноской.
10. На панели операций выберите **Разности** \> **Разнести**, чтобы разнести данные ваучера списания РБП.

Можно создать строку журнала для одного списания.

1. Перейдите к **Главная книга** \> **Записи в журнале** \> **Журнал расходов будущих периодов**.
2. В области действий выберите **Создать**.
3. В поле **Имя** выберите имя журнала.
4. В области действий выберите **Строки**, чтобы открыть страницу **Ваучер журнала**.
5. На вкладке **Обзор** выберите **Создать**, чтобы создать новую строку.
6. В поле **Тип проводки** выберите **Списание**.
7. В поле **Идентификатор РБП** выберите РБП, чтобы создать проводку поступления для него.

    Поля в разделе **Корректировка** диалогового окна **Создание новой строки** используются для создания корректирующей проводки для закрытого периода.

    ![Диалоговое окно создания новой строки](media/rus-write-off-deferral-02.png)

8. Нажмите **ОК**. Строки ваучера создаются для выбранного РБП на странице **Ваучер журнала**.
9. На панели операций выберите **Функции** \> **Редактировать строку**, чтобы отредактировать журнал РБП перед разноской.
10. На панели операций выберите **Разности** \> **Разнести**, чтобы разнести данные ваучера списания РБП.

## <a name="reverse-the-writing-off-of-deferrals"></a>Реверсировать списание РБП

1. Перейдите к **Главная книга** \> **Записи в журнале** \> **Журнал расходов будущих периодов**.
2. В области действий выберите **Создать**.
3. В поле **Имя** выберите имя журнала.
4. В области действий выберите **Строки**, чтобы открыть страницу **Ваучер журнала**.
5. На панели операций выберите **Групповые операции** \> **Реверсировать списание**, чтобы открыть диалоговое окно **Реверсировать списание**.
6. В поле **Дата реверсирования** выберите дату проводки.
7. На экспресс-вкладке **Включаемые записи** выберите **Фильтр**, чтобы открыть диалоговое окно **Запрос**, в котором можно задать критерии выбора.
8. Выберите **OK**, чтобы вернуться к странице **Ваучер журнала**.
9. В области действий выберите **Разнести** \> **Разнести**, чтобы разнести реверсивный ваучер. РБП и проводки ГК, указанные в профиле разноски, будут созданы.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]