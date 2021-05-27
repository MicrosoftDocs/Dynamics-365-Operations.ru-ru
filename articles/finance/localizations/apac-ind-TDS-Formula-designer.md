---
title: Конструктор формул для вычислений TDS
description: В этой теме представлен пример того, как рассчитывается налог, удержанный в источнике (TDS), на основе формулы, определенной для каждого налогового кода TDS в группе TDS, прикрепленной к проводке.
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
ms.openlocfilehash: d0f644da640b56761a52baec9ff01c898e895d19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023529"
---
# <a name="formula-designer-for-tds-calculations"></a>Конструктор формул для вычислений TDS

[!include [banner](../includes/banner.md)]

В этой теме представлен пример расчета налога, удержанного в источнике (TDS), на основе формулы, определенной для каждого налогового кода TDS. Налоговые коды TDS определяются в группе TDS, прикрепленной к проводке. Перед созданием формул TDS выполните базовые настройки, необходимые для TDS, как указано в следующих шагах. 

- Настройте группы компонентов TDS на странице **Группы компонентов подоходного налога**. 
- Настройте компоненты TDS и свяжите группу компонентов TDS с компонентами TDS на странице **Компоненты подоходного налога**. 
- Настройте налоговые коды TDS и свяжите компоненты TDS с налоговыми кодами на странице **Коды подоходного налога**. 
- Настройте налоговые группы TDS на странице **Группы компонентов подоходного налога**. Затем свяжите налоговые коды TDS с налоговой группой и определите формулу, используя страницу **Конструктор формул**. 

**Пример формулы**

В этом примере группа TDS "Аренда" присоединяется к накладной по покупке, созданной для поставщика "А". Сумма накладной 100 000 долларов США. См. следующую таблицу для просмотра расчета TDS по накладной.

| Группа TDS                                                   | Налоговые коды TDS, присоединенные к группе TDS | значение              | Налогооблагаемая база (конструктор формул) | Выражение для расчета (конструктор формул) | Базовая сумма | Рассчитанная сумма TDS |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| Аренда                                                         | TDS (компонент TDS-TDS)                | 10%                | Валовая сумма                      |                                            | 100,000      | 10,000                 |
| Надбавка (компонент TDS-надбавка)                         | 10%                                     | Без валовой суммы | +TDS                              |                   10000                    | 1000        |                       |
| PE-Cess (компонент TDS- PE-Cess)                            | 2%                                      | Без валовой суммы | +TDS+Надбавка                    |                   11000                    | 220         |                       |
| SHE Cess (компонент TDS- SHE Cess)                          | 1%                                      | Без валовой суммы | +TDS+Надбавка                    |                   11000                    | 110         |                       |
| **Итоговый** **TDS**, **рассчитанный** **для** **данной** **накладной** | **11,330**                               |                    |                                   |                                            |             |                       |

Записи ваучера создаются следующим образом:

| Счет           | по дебету  | Кредитование |
| ----------------- | ------ | ------ |
| Аренда              | 100,000 |        |
| Поставщик "А"          |        | 100,000 |
| Поставщик "А"          | 11,330  |        |
| Подлежащий уплате TDS       |        | 10,000  |
| Надбавка, подлежащая оплате |        | 1000   |
| PE-Cess, подлежащий оплате   |        | 220    |
| SHE-Cess, подлежащий оплате  |        | 110    |