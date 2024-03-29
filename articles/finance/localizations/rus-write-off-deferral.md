---
title: Списание РБП (Россия)
description: Эта статья объясняет, как списать расходы будущих периодов (РБП) и как реверсировать списание РБП.
author: AdamTrukawka
ms.date: 06/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: atrukawk
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: 10.0.1
ms.search.form: ''
ms.openlocfilehash: 46fd26192ccca8eb28abcaad78050194e3eb947b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288501"
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

    ![Страница Ваучера журнала.](media/rus-write-off-deferral-01.png)

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

    ![Диалоговое окно создания новой строки.](media/rus-write-off-deferral-02.png)

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
