---
title: Настройка периодов сопоставления подоходного налога для налогов типа TDS
description: В этой теме объясняется, как настроить периоды сопоставления для периодов сопоставления по налогу, который удерживается в источнике (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023525"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a>Настройка периодов сопоставления подоходного налога для налогов типа TDS

[!include [banner](../includes/banner.md)]

В этой теме объясняется, как настроить периоды сопоставления для периодов сопоставления по налогу, который удерживается в источнике (TDS).

1. Перейдите в раздел **Налог \> Косвенные налоги \> Подоходный налог \> Периоды сопоставления подоходного налога**.

    [![Страница периодов сопоставления подоходного налога](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)

2. В поле **Тип налога** выберите **TDS**, чтобы настроить периоды сопоставления подоходного налога для типа налога TDS.
3. Выберите **Создать**, чтобы создать строку.
4. В поле **Период сопоставления** введите имя периода сопоставления TDS.
5. В поле **Описание** введите описание.
6. В поле **Налоговый орган по подоходному налогу** выберите орган TDS, для которого определяется период сопоставления TDS.
7. На экспресс-вкладке **Общие** в поле **Интервал периода** выберите тип интервала периода для периода сопоставления TDS.
8. В поле **Число единиц** укажите число единиц измерения для типа интервала периодов.
9. На экспресс-вкладке **Периоды** в поле **Начальная дата** выберите начальную дату для периода сопоставления TDS. В поле **Конечная дата** выберите дату окончания.
10. Чтобы создать последующий период сопоставления TDS для существующего периода на основе интервала периода и единиц периода, выберите **Создать период**.
11. Для просмотра подробных сведений о периодическом выполнении сопоставления TDS, который запускается для определенного периода сопоставления, выберите **Платежи подоходного налога**, чтобы открыть страницу **Платеж по подоходному налогу**.

    > [!NOTE]
    > Чтобы выполнить периодическое сопоставление TDS, перейдите **Главная книга \> Периодически \> Подоходный налог \> Платеж подоходного налога**.

    [![Страница платежа подоходного налога](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)

12. Закройте страницу.
